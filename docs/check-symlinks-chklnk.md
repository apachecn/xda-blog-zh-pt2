# 使用 Chklnk 检查项目中的符号链接

> 原文：<https://www.xda-developers.com/check-symlinks-chklnk/>

# 使用 Chklnk 检查项目中的符号链接

这个方便的脚本会给你一个在你的 ROM 中使用的符号链接的列表，这样你可以确保它们是有效的，不会给你的用户带来问题！

和所有基于 Unix 的操作系统一样，Android 使用符号链接。符号链接是一种特殊类型的文件，它以绝对或相对路径的形式包含对另一个文件或目录的引用，这会影响路径名解析。在 Android 中，它们主要用在 */bin* 和 */xbin* 文件夹中，所有正在执行的二进制文件都保存在那里。

如果你想创建自己的符号链接，或者想知道哪些文件是工具箱或 Busybox 的一部分，你可以通过在终端中输入一些命令来手动查找。你也可以用 XDA 资深成员 [LENAROX](http://forum.xda-developers.com/member.php?u=4629194) 写的剧本。Chklnk 只不过是 [BASH 脚本](http://www.xda-developers.com/android/bash-patched-shellshock-vulnerability/ "Protect Yourself from Shellshock Vulnerability with Patched BASH")，它只需一个命令就可以轻松识别符号链接。在推到选定的系统文件夹并使其可执行后，该脚本可用于增强您的开发项目。

要使用这个脚本，您的设备必须是根设备，因为您需要将脚本文件推送到您的 */system* 分区。您还应该安装 Busybox 1.19.4 或更高版本。用法非常简单，因为您只需要输入 chklnk [file]命令来获取连接列表。

Chklnk 是使您的开发项目更好的好方法。可以通过访问 [chklnk.sh 脚本论坛线程](http://forum.xda-developers.com/android/software-hacking/script-checking-symlinks-fast-t2902774)了解更多。