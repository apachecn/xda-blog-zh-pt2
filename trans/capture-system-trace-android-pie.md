# 如何在 Android Pie 上本地捕获系统跟踪

> 原文：<https://www.xda-developers.com/capture-system-trace-android-pie/>

跟踪是一个非常有价值的工具，它使开发人员能够理解各种变化对系统的影响，并且可以提供线索来确定问题的根本原因。

systrace 就是这样一个强大的跟踪工具，它从运行在 Android 设备上的进程中收集时间信息。 *systrace* 被谷歌的 [Android 性能团队](https://www.youtube.com/watch?v=Qfo5fdoXrTU)广泛用于优化谷歌 Pixel 手机的性能。例如，我已经使用了 *systrace* 来检查内核调度器的变化对 CPU 上的任务放置的影响，并识别 janks 的可能原因。 *systrace* 可以捕获各种各样的数据，包括 CPU 调度、CPU 频率、磁盘 I/O、图形、活页夹活动等等。这些信息被整合成一份报告，可以在谷歌浏览器中进行分析。

在 Android Pie 出现之前，用 *systrace* 捕获踪迹的唯一方法是将一个 Android 设备连接到一台计算机上，然后从那里运行 systrace——通常是从一个终端。然而，并不是每个人都能经常接触电脑，或者拥有运行 systrace 的知识和信心。

随着 Android Pie 的发布，这种不便通过引入 [Traceur 包得到了解决，这是一种直接在 Android 手机上捕获原始跟踪数据](https://android.googlesource.com/platform/packages/apps/Traceur/)的工具。Traceur 在设置应用程序的开发者选项中作为“系统跟踪”选项提供，Traceur 在设备上捕获的原始跟踪数据可以在稍后由 *systrace* 转换为 HTML 报告进行分析。

新的“系统跟踪”选项允许用户轻松捕获并与开发人员共享跟踪，而无需实际知道如何在计算机上运行 *systrace* 。开发人员受益于无需计算机就能捕获轨迹并在以后方便时进行分析的能力。“系统跟踪”收集的完整的原始跟踪数据在大小上也明显小于由 *systrace* 生成的 HTML 报告，因此这使得原始跟踪数据更适合于存储和与他人共享。

## 指南:收集系统和分析系统跟踪

首先，确保你有一台运行 Android Pie 的设备和一台安装了 Python 2 的计算机。以下说明是在运行最新 OxygenOS Android Pie 测试版的 OnePlus 6 上执行的。

1.  [在设置应用中启用开发者选项，然后进入开发者选项“调试”部分的“系统跟踪”选项](https://developer.android.com/studio/debug/dev-options)。[](https://static1.xdaimages.com/wordpress/wp-content/uploads/2018/09/System-Tracing-on-Android-Pie9.png)
2.  打开系统跟踪时，您将看到一个启用系统跟踪的开关，以及定制跟踪类别和跟踪缓冲区大小的能力。对于本演示，使用默认类别，这对于大多数情况来说已经足够了。“显示快速设置磁贴”开关允许通过快速设置启动/停止跟踪。我已经为本指南启用了此功能。[](https://static1.xdaimages.com/wordpress/wp-content/uploads/2018/09/System-Tracing-on-Android-Pie8.png)
3.  要开始捕捉轨迹，请点击最近添加的“记录轨迹”快速设置磁贴。
4.  当您完成跟踪一个测试用例时，您可以从通知阴影中停止跟踪。
5.  太好了！您成功捕获了一条原始痕迹。通知将提示您共享原始跟踪文件。你应该能够把它保存到你的设备上，上传到网上存储器，用电子邮件发给别人，等等。或者，您可以使用 ADB 直接将跟踪从您的设备中提取到您的计算机中(`adb pull /data/local/traces/`)。继续将跟踪文件保存到您的计算机上。
6.  原始跟踪文件具有虚构的[。ctrace 格式](https://android.googlesource.com/platform/packages/apps/Traceur/+/32fac6ad6592389fb887830af49d41b8e40a6a7f)。它不能以其原始的形式被解释。我们可以使用 *systrace* 从我们的原始跟踪文件中生成一个更有用、更容易理解的交互式 HTML 报告。
7.  我们将使用来自[弹射项目报告](https://github.com/catapult-project/catapult/)的*系统*的最新版本。在终端应用程序中，克隆 repo(确保安装了 git):

    ```
     git clone https: 
    ```

8.  要使用 *systrace* 从我们的原始跟踪文件生成 HTML 报告，请输入以下命令:

    ```
     python2 catapult/systrace/bin/systrace --from-file=<path to raw trace file> 
    ```

    将生成一个与原始跟踪文件同名的 HTML 文件。*注意:撰写本文时，systrace 仅支持 Python 2。*
9.  要查看 HTML 报告，请启动 Google Chrome 浏览器并访问“Chrome://tracing”URL。不要直接在谷歌浏览器中打开 HTML 报告，因为它会显示为空白。
10.  点击“加载”,从弹出的对话框中打开 HTML 报告文件。瞧啊。你的追踪报告现在可供检查。

### 下一步是什么？

既然您已经能够捕获跟踪并生成一个 *systrace* 报告，那么理解如何读取和解释报告中显示的数据就很重要了。首先，我推荐阅读“[了解 *Systrace*](https://source.android.com/devices/tech/debug/systrace) ”，并观看“ [Android 性能:概述(Google I/O '17)](https://www.youtube.com/watch?v=Qfo5fdoXrTU) ”和“[*Systrace*for Games](https://www.youtube.com/watch?v=4oAlB-3tkqc)”，以了解 *systrace* 的实际操作。

*这是一篇客座博文，作者是乔希·乔(Josh Choo)，也被称为 XDA 知名开发者[乔舒斯](https://forum.xda-developers.com/member.php?u=6745491)。这篇文章在格式上稍加编辑。*