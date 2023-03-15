# APKTool 反编译和重新编译指南

> 原文：<https://www.xda-developers.com/guide-to-decompiling-and-recompiling-with-apktool/>

几天前，[我们报道了一个工具](http://www.xda-developers.com/android/simplify-your-modifications-with-backsmali-smali-manager/ "Simplify Your Modifications with Backsmali/Smali Manager")，旨在使使用 Baksmali/Smali 更容易，这是一个用于 Android 中 Dalvik 虚拟机使用的 Dex 文件的反汇编器/汇编器。另一个非常有用的工具是 [APKTool](http://www.xda-developers.com/android/apktool-v0-9-2-re-engineer-apk-files/ "APKTool v0.9.2 – Re-engineer apk files") ，它最初由 XDA 公认的开发者 [Brut.all](http://forum.xda-developers.com/member.php?u=1922851) 开发，并由 XDA 资深成员 [iBotPeaches](http://forum.xda-developers.com/member.php?u=3924617) 延续至今[。](http://www.xda-developers.com/android/apktool-to-receive-updates-once-again/ "APKTool to Receive Updates Once Again")

虽然 APKTool 非常强大，但它也可能让新的主题和修改者望而生畏。然而，多亏了 XDA 公认的贡献者和主题者 [PulseDroid](http://forum.xda-developers.com/member.php?u=4425071) 创建的指南，这应该不再是一个大问题。

入门指南涵盖了您需要什么文件、您的开发环境，以及如何实际使用该工具进行反编译和重新编译。这可以通过四个简单的步骤来完成:安装框架、反编译(并应用您的修改)、重新编译，以及将新内容插入旧的 APK 以保留旧的签名。

指南步骤附有丰富的截图和大量的解释。总而言之，这份非常简单易懂的指南将带你上路，不管你一开始的经验有多少。

如果你刚刚开始，请前往[原始线程](http://forum.xda-developers.com/showthread.php?t=1989533)查看指南。当你使用它的时候，去 [APKTool 线程](http://forum.xda-developers.com/showthread.php?t=1755243)那里了解一下这个工具本身。