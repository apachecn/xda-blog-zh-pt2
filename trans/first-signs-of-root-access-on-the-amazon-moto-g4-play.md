# 亚马逊 Moto G4 Play 首次出现 Root 访问迹象

> 原文：<https://www.xda-developers.com/first-signs-of-root-access-on-the-amazon-moto-g4-play/>

自从亚马逊开始以折扣价销售精选的 Android 智能手机以换取广告以来，开发者一直在试图找出释放这些设备全部潜力的方法。[我们 Moto G4 Play 论坛](https://forum.xda-developers.com/g4-play/help/unlocking-amazon-g4-play-bootloader-t3629834)的一个帖子是由 XDA 初级会员 [A.Fitz](https://forum.xda-developers.com/member.php?u=7780160) 发起的，希望能让解锁 bootloader 的工作顺利进行。这个讨论主题尚未发现解锁引导加载程序的方法，但 XDA 成员[莱多西斯](https://forum.xda-developers.com/member.php?u=7838117)能够在 Moto G4 Play Amazon 变种上获得一个拴系根解决方案。这种拴系的方法需要/init 打补丁，sepolicy 和/sbin/adbd 取自 athene-m 镜像，/xbin/su 取自 android arm 模拟器，/init.mmi.usb.rc 两处将“echo 1”改为“echo 0”。

[**在我们的 Moto G4 Play 论坛**](https://forum.xda-developers.com/g4-play/help/unlocking-amazon-g4-play-bootloader-t3629834/post72922302#post72922302) 跟随这一进程