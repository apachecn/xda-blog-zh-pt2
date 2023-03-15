# 手动修复你的欧洲安卓 GPS 锁

> 原文：<https://www.xda-developers.com/fix-your-european-android-gps-lock-manually/>

你是欧洲安卓用户吗？如果是这样，你可能已经注意到你的 GPS 锁定性能经常低于标准。上个月，[我们写了关于 XDA 论坛成员](http://www.xda-developers.com/android/speed-up-your-gps-fix-with-fasterfix/)[的](http://forum.xda-developers.com/member.php?u=2566115)一个[奇妙的应用](http://forum.xda-developers.com/showthread.php?t=825717)，它通过编辑你的 */system/etc/gps.conf* 文件为你修复了这个问题。

然而，有些用户有点守旧，宁愿自己动手修改。为此，XDA 论坛成员[clause 72](http://forum.xda-developers.com/member.php?u=319971)写了一个简单的一步指南来帮助你做到这一点。显然，要执行修复，您需要对您的设备拥有完全的根访问权限。

虽然最初是为 HTC HD2 编写的，但它应该可以在所有欧洲 Android 设备上运行。

> 我有一个 gps 定位的问题，它花了大约 90 秒来修复卫星。
> 
> 我在欲望部分找到了一个解决这个问题的线索。
> 
> 现在，我的全球定位系统需要 15-30 秒才能显示出来。卫星。
> 
> **此修复仅针对欧洲用户，需要拥有 root 权限。**
> 
> 您必须编辑位于/system/etc 的文件 gps.conf。我已经使用了根资源管理器来编辑文件。

如果你对使用你的 *gps.conf* 文件感兴趣，点击[原始线程](http://forum.xda-developers.com/showthread.php?t=906576)。为了安全起见，请务必备份您原来的 *gps.conf* 。

如果你想用简单的方法来做这件事，回头参考前面提到的 [FasterFix](http://forum.xda-developers.com/showthread.php?t=825717) 。