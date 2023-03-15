# 使用引导 Shell 在引导时执行 Shell 命令

> 原文：<https://www.xda-developers.com/execute-shell-commands-at-boot-with-boot-shell/>

Android 是一个类似 Unix 的操作系统。它使用自己的工具箱和/或 BusyBox 解释 Linux 命令。利用这种能力，在某些情况下，您需要在启动时运行 shell 命令。如果你不想弄乱 *init.d* 或其他系统文件夹，你可以找到在启动时为你运行命令的应用程序——像 Boot Shell 这样的应用程序。

Boot Shell 是由 XDA 资深成员 [gh0stslayer](http://forum.xda-developers.com/member.php?u=3137016) 创建的。使用这个应用程序，用户可以很容易地定义在引导时执行的 shell 命令。该应用程序可以执行简单的命令，如复制文件或在 */data/app/、*中列出已安装的应用程序，它还可以用于激活内核相关的功能，如超频、欠载、调控器和加载定制模块。它非常容易使用，因为所有你需要做的就是输入你想要执行的命令，并把它添加到引导或作为一个喜欢的命令。

如果你在一个没有 *init.d* 功能的根股票 ROM 上，或者只是想在启动时添加一些 shell 命令，那么就找到[应用程序线程](http://forum.xda-developers.com/showthread.php?t=2641227)并尝试一下。