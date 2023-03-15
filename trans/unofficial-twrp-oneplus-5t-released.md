# OnePlus 5T 发布的非官方 TWRP——制作备份和手机 Root

> 原文：<https://www.xda-developers.com/unofficial-twrp-oneplus-5t-released/>

OnePlus 5T 今天刚刚[公布。除了显示屏，它与 OnePlus 5 相比并没有太大的不同。我们还不能确定 OnePlus 5/5T 是否可能实现统一构建，但感谢内核源代码发布，我们知道](https://www.xda-developers.com/oneplus-5t-official-launch/)[果冻滚动问题很可能已经消失](https://www.xda-developers.com/oneplus-5t-no-jelly-scrolling/)。尽管这款手机本身还没有到达任何消费者手中(它将于 11 月 21 日发布)，但我们已经为这款手机在 TWRP 制造了。

由于 OnePlus 5 的 TWRP 版本无法启动，我们只是用 OnePlus 5T 的内核重新打包了 OnePlus 5 的 TWRP 版本。它的工作方式与您预期的一样——您可以擦除分区、制作备份和闪存 zip 文件。当然，还没有任何 rom，内核，或其他修改实际上可用于手机，但这是很好的已经提供给那些你第一天的闪存爱好者。

[**下载一加 5T 的 TWRP**](https://www.androidfilehost.com/?fid=745849072291689244)

你可以通过上面的链接下载我们制作的 TWRP 版本。解锁 OnePlus 5T 的引导加载程序后，您可以通过发送以下命令之一来引导或刷新它。

**开机**:

```
 fastboot boot o5ttwrp.img 
```

**闪光**:

```
 fastboot flash recovery o5ttwrp.img 
```

请记住，这是一个**非官方版本**，我们是为了自己的测试目的而制作的。现在这个设备的[内核源代码](https://github.com/OnePlusOSS/android_kernel_oneplus_msm8998/commit/bed1ab9e043f7b182e7b352fbe827ccab9efb389)已经发布，开发者可以创建一个合适的 TWRP 版本了。我们的 OnePlus 5T 论坛将很快开放，因此一旦论坛上线，您可以在那里关注未来的发展。

我们希望能够很快确定是否有可能进行统一构建。这样的开发将大大提高 OnePlus 5T 的可定制性，因为开发工作将不必分散在我们已经很受欢迎的 OnePlus 5 论坛和新的 OnePlus 5T 论坛上。