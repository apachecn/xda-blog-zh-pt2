# 如何使用 Samloader 为三星 Galaxy 下载更新

> 原文：<https://www.xda-developers.com/samloader-download-updates-samsung-galaxy/>

# 如何使用 Samloader 为您的三星 Galaxy 设备下载更新

Samloader 为您的 Samsung Galaxy 设备提供了一种轻松下载最新固件的方式。它也可以在 Linux 和 macOS 上运行。

尽管三星每年都会发布大量设备，但该公司并没有为其 Galaxy 品牌的智能手机和平板电脑提供官方的用户友好的固件下载门户。你可以在设置中用内置的更新检查器试试运气，或者你可以使用[三星智能开关](https://shop-links.co/1723585510879381223)应用程序——这两个选项都不会满足渴望立即获得最新更新*的超级用户*。因此，三星爱好者经常转向第三方服务下载更新，这些更新被方便地打包，并准备好通过 Odin 发送给[。像](https://www.xda-developers.com/update-firmware-any-samsung-phone/) [SamFirm](https://www.xda-developers.com/download-stock-odin-firmware-samfirm/) 和 [Frija](https://forum.xda-developers.com/s10-plus/how-to/tool-frija-samsung-firmware-downloader-t3910594) 这样的工具也被社区广泛使用，因为人们可以很容易地查询三星 FUS(固件更新服务器)并使用这些工具下载其模型的最新版本。

然而，上述固件下载器都不是开源的。这些工具利用 Smart Switch 分发版中的特定库向更新服务器进行身份验证。使用 [Themida](https://oreans.com/themida.php) 对库本身进行模糊处理，这也是这些实用程序难以移植到微软 Windows 以外的操作系统的原因之一。尽管如此，XDA 少年成员 [nn000](https://forum.xda-developers.com/member.php?u=10841033) 还是设法跨越了这些障碍。

在仔细逆向工程下载协议后，开发人员决定用 Python 编写下载器，这意味着最终的工具可以在几乎任何操作系统上执行。结果就是 **Samloader** ，一个跨平台的 CLI 应用程序，可以在不使用任何专有 DLL 的情况下获取三星固件包。这个极其微小的脚本(不到 100KB)也可以解密 OTA 工件，并创建一个标准的 flash 包。

* * *

## 如何使用 Samloader 为您的三星 Galaxy 设备下载固件

1.  确保您安装了 Python 3 和 pip。
2.  使用[此链接](https://github.com/nlscc/samloader/archive/master.zip)下载 Samloader 的代码库，或者使用 git:

    ```
     git clone https: 
    ```

    克隆存储库
3.  使用 pip 安装:

    ```
     cd samloader
    pip3 install . 
    ```

4.  检查您的型号的最新固件版本:

    ```
     samloader checkupdate [model] [region] 
    ```

5.  将指定手机和地区的指定固件版本下载到指定文件或目录:

    ```
     samloader download [version] [model] [region] [out] 
    ```

6.  解密加密的固件工件:

* * *

值得一提的是，Samloader 并不支持所有的三星更新渠道。一些运营商(如 AT & T 和威瑞森)不通过三星的 OTA 服务器提供更新。此外，你不能使用这个脚本下载[测试版固件](https://www.xda-developers.com/changelog-samsungs-one-ui-3-0-update-based-android-11/)。

**Sam loader:[GitHub Repo](https://github.com/nlscc/samloader)| | |[XDA 讨论线程](https://forum.xda-developers.com/s10-plus/how-to/tool-samloader-samfirm-frija-replacement-t4105929)**