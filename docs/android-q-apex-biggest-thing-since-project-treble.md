# Android 中的 APEX Q:自 Project Treble 以来最大的事？

> 原文：<https://www.xda-developers.com/android-q-apex-biggest-thing-since-project-treble/>

实现 APEX 可能是谷歌自推出 Project Treble 以来面临的最头痛的问题。APEX 是什么，它的推出将如何改变 Android？

APEX 本身背后的思想在日常 GNU/Linux 发行版中相当普遍:针对 Linux 库集的特定部分的包更新。但这是谷歌从未尝试过的事情，因为 Android 使用了一个 RO(只读)分区来存储所有的系统库和框架，而不是大多数 Linux 发行版中通常使用的 RW(读写)分区，这使得标准升级过程不合适。

库是可以在其他程序中使用的预编译代码。常用的方法可以制成供 Android 应用程序调用的库，减少 apk 的大小，因为相同的代码不需要在多个应用程序之间重复实现。您可以在/system/lib 和/system/lib64 目录中找到许多预安装的系统库。Android 系统库通常不会单独更新，而是通过 OTA 更新作为 Android 平台升级的一部分进行更新。另一方面，Linux 发行版中的库可以单独更新。随着 APEX 的引入，Android 中的系统库可以像 Android 应用程序一样单独更新。这样做的主要好处是，应用程序开发人员将能够利用更新的库，而不必等待 OEM 推出完整的系统升级。让我们深入了解 APEX 工作原理的更多技术细节。

## APEX 将如何改变库的更新方式？

APEX 是一个迫使(或者说，正在迫使)谷歌重新考虑 Android 从不同于/system 的非标准分区加载所有库和文件的方式的生态系统。

首先，我们必须明确共享库和静态库的区别。共享库是一个库(通常是一个名为 libkind.so 的文件),它本身不包含运行所需的所有代码，但“链接”到实际提供代码的其他库，而静态库是一个不依赖于任何其他库的库，所有内容都静态地包含在文件中。

Android 在历史上使用一个名为 ld.config.txt [0]的文件来配置库路径(在 Linux 世界中称为 LD_LIBRARY_PATH ),以便为二进制文件或另一个库所需的共享库配置允许的搜索路径。这些路径在配置中是硬编码的，不可扩展。这种布局，包括只读系统分区，导致不可更新的库，除非用户安装 OTA Android 更新。Google 修复了此问题，允许扩展搜索路径，方法是让单个 APEX 包提供自己的 ld.config.txt，其中包含额外的(和更新的)库路径。

虽然这一举措解决了一个主要问题，但仍有一些严重的问题需要解决。首先:ABI(应用二进制接口)稳定性。库应该总是导出一组稳定的接口，以允许其他应用程序和库继续使用相同的协议，即使是升级后的库。Google 正在积极努力，试图在 APEXed 库之间创建一个稳定的 C 接口。

但是 APEX 不仅限于库和二进制文件。事实上，它可以包含配置文件、时区更新和一些 Java 框架(在撰写本文时是 conscrypt)。

以下是 AOSP 目前提供的 APEX 软件包的几个示例:

*   ART 和仿生运行时(二进制和库)
*   com.android.tzdata:时区和 ICU 数据(库和配置数据)
*   android 用来解析网络相关请求的库(库)
*   com . Android . con crypt:一个 Java 安全提供者(Java 框架)

## 如何安装和构建 APEX 软件包？

APEX 包是一个简单的 zip 存档(就像一个 APK ),可以由我们方便的 ADB 安装(在开发的这一点上),然后由用户自己通过包管理器安装(像 Google Play 或通过 Android 包安装程序手动安装)。

邮政编码布局如下:

让我们深入研究一下。

apex_manifest.json 指定软件包名称和版本。

apex_payload.img 是一个微文件系统映像(格式为 EXT4)。

其他文件是用于安装包的验证过程的一部分。让我们看一看。

AndroidManifest.xml 的存在，即使它主要用于应用程序中，也帮助我们理解用于标准 APK 安装的大部分实现甚至在这些包中也被重用。事实上，只检查扩展名来区分它们。

**META-INF/** 目录拥有包证书，并使用与普通 apk 相同的机制。因此，在允许用户安装更新之前，这些包在运行时由私钥/公钥对进行验证。但这对谷歌来说还不够，所以他们增加了两层安全措施。他们使用 dm-verity 来检查图像的完整性，并使用 AVB (Android 验证启动)验证来确保图像来自可信的来源。在最坏的情况下，APEX 包将被拒绝。

如果所有验证步骤都成功，映像将被标记为有效，并将在下次重新启动时替换系统变体。

## 如何在启动时安装映像？

让我们先来看看目前安装在我的设备(一个模拟器)上的顶点

如您所见，预安装的软件包存储在/system/apex/中，它们目前的版本号都是 1。但是当顶点被激活时会发生什么呢？我们将再次使用 com.android.tzdata 作为示例。

让我们重新启动设备并分析 logcat。

前两行提供了足够的信息来理解软件包的来源和安装位置:/apex/，这是 Android Q 中引入的一个新目录，将用于存储激活的软件包。

在用 AVB 成功验证了包并且公钥匹配之后，使用循环设备将 APEX 挂载到/dev/block/loop0，使得系统可以访问 EXT4 文件系统。循环设备是一种伪设备，它使文件可以作为块设备访问，使该文件的内容可以作为挂载点访问。

此时，APEX 仍然没有被使用，因为有@1 后缀(表示包的版本)。为了最终让系统知道我们的包已经被成功激活，它将被绑定到/apex/com.android.tzdata，android 积极地期望 tzdata 驻留在那里。绑定装载会覆盖不同点下的现有目录或文件。[1]

APEX 实现完全包含在 AOSP 下的一个存储库中。[2]apexd(APEX 守护程序)目录包含运行在 Android 上的代码。apexer 目录包含构建系统用来创建 APEX 包的代码。

## 目的是什么？

在这一点上，我所能做的就是推测。我的最佳猜测是，谷歌正试图创建一个核心的 APEX 包集，可以由谷歌更新，以可能创建一个统一的供应商之间共享的 Android 基础核心，使“系统”更新成为可能，但使用单个包更新。

## 所有设备都将支持 APEX 吗？

不会。例如，apexd 要求/data/apex 在启动后立即可用，以更新所有 Android 模块。使用 FDE(全磁盘加密)，/data/apex 会一直加密，直到用户解锁设备，导致 apex 基本上没有用，因为只有系统 APEX 变体会在引导时加载。除此之外，所有设备都应该支持 APEX，但它们需要一些内核补丁(其中许多是谷歌在玩循环设备时发现的修复程序)。[3] [4]

* * *

来源[ [0](https://android.googlesource.com/platform/system/core/+/master/rootdir/etc/ld.config.txt) ，[ [1](https://android.googlesource.com/platform/bionic/+/master/libc/tzcode/bionic.cpp#213) ，[ [2](https://android.googlesource.com/platform/system/apex/+/master) ，[ [3](https://git.kernel.org/pub/scm/linux/kernel/git/axboe/linux-block.git/commit/?h=for-linus&id=5db470e229e22b7eda6e23b5566e532c96fb5bc3) ，[ [4](https://android-review.googlesource.com/q/Ic35cd2782a646435689f5bedfa1f218fe4ab8254) ]