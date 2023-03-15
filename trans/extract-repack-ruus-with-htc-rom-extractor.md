# 用 HTC ROM 提取器提取并重新打包 ruu

> 原文：<https://www.xda-developers.com/extract-repack-ruus-with-htc-rom-extractor/>

如果你是 HTC 用户，你很可能熟悉 RUUs 或 ROM 更新工具，HTC 以这种格式向提供他们的库存 ROM 和更新。对于那些不熟悉的人来说，它们基本上是一个特定设备的只读存储器，封装在一个可从个人电脑上运行的可执行文件中的。虽然它们确实为人们提供了一种安全而简单的方式来更新他们的设备，但是对于那些希望在刷新固件之前修改固件的人来说，它们有些不灵活。还有一个问题是。对于没有运行 Windows 的人来说，exe 文件并没有多大用处。

HTC ROM 提取器由 XDA 资深会员 [as i9000](http://forum.xda-developers.com/member.php?u=2976903) 然而，可以帮助解决这些问题。这是一个基于 Linux 的工具，允许您执行各种不同的功能，以更好地利用 RUU 的原始形式。一些功能包括:

*   从 RUU 中提取 rom.zip，
*   挂载系统。 img 到文件系统，
*   能力 到解压稀疏图像系统。 img 并挂载到文件系统中，
*   再压缩系统。 img

你需要安装一个可以正常工作的 libunshield v0 。 7 或更高才能继续。线程中提供了有关如何安装的说明。因此，如果你想在 Linux 上修补一些 ruu，查看[原始线程](http://forum.xda-developers.com/showthread.php?t=2199655)以获取更多信息。