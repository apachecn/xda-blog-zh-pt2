# 编辑您的版本。使用 BuildProp 编辑器轻松支撑

> 原文：<https://www.xda-developers.com/edit-your-build-prop-the-easy-way-with-buildprop-editor/>

我们中的大多数人，在某个时候，已经深入到我们的 *build.prop* 文件中，寻找一些难以捉摸的领域来调整，以优化我们的移动设备。对于许多人来说，这意味着简单地改变 *LCD.density* 标志，以在每个屏幕上显示更多或更少的信息，但对于其他人来说，这可以采取更加面向性能的参数的形式，如 *dalvik.vm.heapsize* 。

以前，编辑 *build.prop* 并不完全是对用户友好的事情。人们必须使用 adb 命令来修改文件，或者通过启用 root 的文件管理器[来访问文件，比如我们在过去](http://www.xda-developers.com/android/miui-file-explorer-ported-to-other-roms-acquires-root/)[中介绍过的](http://www.xda-developers.com/android/android-file-expert-with-enhanced-networking-support/)。然而，除了比专用编辑器麻烦一点之外，这些潜在的风险更大一点，因为错误的设置或意外的删除可能会被证明是不利的。

为了缓解这一问题，XDA 论坛成员 [android_owl](http://forum.xda-developers.com/member.php?u=3022988) 开发了一个 *build.prop* 编辑器，可以消除你调整移动设备时的所有猜测。BuildProp Editor 提供了一个可编辑字段的列表，并对它们的功能做了清晰的解释，即使是新手也能轻松上手。现在，我们已经在过去的门户网站上报道了一个专门的 [*build.prop* editor](http://www.xda-developers.com/android/app-build-prop-editor-v1-0/) ，但是这个版本通过提供一个字段一个字段的解释建立在以前的产品之上。

用开发商的话说:

> 这个工具是用来做什么的？
> 
> 此工具允许您在设备上轻松修改 build.prop 文件。它使编辑变得容易，你不必关心重新安装东西或读/写权限。此外，它还提供了包含物业信息的描述。对初学者和高级用户都是一个很好的工具。它可以用来测试你的设备的各种属性，甚至调整它，但要注意:你必须知道你在做什么！如果手机重启后无法启动，您的设备的初始备份可在以下位置找到:**/data/data/de . bwulfert . buildpropedit/build . prop**

如果你还没有兴奋到想要尝试一下，你可能需要检查一下你的脉搏。对于[我们这些还活着的人](http://www.xda-developers.com/android/are-they-dead-are-they-alive-wonder-no-longer/)，请前往[申请线程](http://forum.xda-developers.com/showthread.php?t=1542949)。