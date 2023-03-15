# 使用自动 Odexer 轻松执行 Odex

> 原文：<https://www.xda-developers.com/odex-with-ease-using-auto-odexer/>

定制 ROM 时，必须做出决定。要做的一个更有趣的决定是[是否 odex](http://www.xda-developers.com/xda-tv-2/pro-tip-number-5-why-you-should-odex-and-deodex-xda-tv/ "Pro Tip Number 5: Why You Should Odex and Deodex – XDA TV") 。在 odexing 中，会创建一个 ODEX 文件，并将其放在相应的 APK 旁边，这样就可以将相关信息快速加载到 Dalvik VM 中。这样做的缺点是，应用程序主题化的能力大大降低了。虽然默认情况下，系统 apk 在出厂时就已经过解码，但其他应用程序则不然。对于那些对主题化不感兴趣并且想要 odex 一个单一的、特定的文件的人来说，这个过程可能会令人望而生畏。

多亏了 XDA 论坛成员阿尔哈法夫，开发者现在可以轻松地使用他的 Auto Odexer 脚本进行 odex。使用它很简单。将下载的文件解压缩到一个文件夹中，然后:

> 1.首先将原始 odex 和 apk(或 jar)文件放在“original”文件夹中。
> 
> 2.把你的修改过的解压后的 apk 文件放在“mod”文件夹中
> 
> 3.如果您修改了去索引的 apk(或 jar)的(res)文件夹中的任何文件，或者您对 xml 文件进行了任何编辑，然后拖动
> 
> 将这些文件从去索引的 apk(或 jar)中放入原始的 apk(或 jar)中(如果您对 xml 文件进行了更改，那么将 resources.arsc 拖到原始的 apk(或 jar)文件中)。使用 7zip 进行此操作。
> 
> 4.用 usb 连接手机，确保 adb 工作正常。(并且不要忘记在你的设备的设置中检查 USB 调试)。
> 
> 5.最好是在恢复模式下启动，尤其是在对框架文件进行编码的时候。
> 
> 6.现在运行脚本，根据您想要 odex 的文件选择 apk 或 jar。
> 
> 7.脚本打开后，写下 apk(或 jar)文件的名称，不带。apk(或者。罐子)
> 
> 8.奥德兴......完成了。

对于最终用户来说，这个过程非常简单直观。所以那些想做些 odexing 的人，去看看[原始线程](http://forum.xda-developers.com/showthread.php?t=1879128)，给这个坏小子一个旋转。