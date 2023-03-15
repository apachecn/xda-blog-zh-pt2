# 开发者为 Moto G5 Plus 带来 64 位 ROM 支持

> 原文：<https://www.xda-developers.com/developer-brings-64-bit-rom-support-moto-g5-plus/>

摩托罗拉的软件可以被认为是一个大杂烩。一方面，这是一个非常接近股票的 Android 体验，带来很少或没有臃肿的软件，只是增加了有用的，非侵入性的功能超过 AOSP Android，还在时机成熟时释放[内核源代码](https://www.xda-developers.com/motorola-kernel-sources-moto-x4/)。

另一方面，更新支持充其量是平庸的，最差的是荒谬的，软件本身也是一些问题的受害者...奇怪的决定。尽管自 Moto E 2015 推出 Snapdragon 410 以来一直使用 64 位处理器，但摩托罗拉自己一直拒绝在他们的设备上使用 64 位软件，而是在他们的手机阵容中选择传统的 32 位软件，即使是在 2017 年的手机上，如 Moto G5 Plus。然而，这个决定背后的原因仍然不清楚，这可能是开发懒惰的结果。由于缺乏驱动程序，将 32 位设备转换为 64 位也是一项几乎不可能完成的任务。

然而，这个壮举现在已经由 XDA 公认的开发者 [vache](https://forum.xda-developers.com/member.php?u=1829889) 实现了，他成功地编写了一份指南，以在 Moto G5 Plus 上构建和运行 64 位 rom 和 TWRP。这仍然是一项正在进行中的工作，但如果正确完成，这将是 Moto G5 Plus 软件开发社区的一个巨大进步，在不久的将来，其他设备也可能如此，比如使用相同 SoC 和 32 位软件的 Moto Z Play。

这在很多层面上都很重要。举一个 64 位的优势，你可以使用谷歌摄像头 HDR+端口，这在过去已经被证明可以大大提高很多性能不佳的手机的拍照质量。

但是，由于它仍然是一项正在进行的工作，这里那里都有权衡。例如，系统服务器(app_process)需要在 32 位模式下运行，许多专有服务也是如此。然而，最后，手机现在可以运行 64 位软件这一事实本身就是一个壮举，我们真的很期待很快看到这个项目的更多信息。

* * *

[**查看 Moto G5 Plus 的 64 位 rom！**](https://forum.xda-developers.com/g5-plus/development/dev-64bits-t3708091)