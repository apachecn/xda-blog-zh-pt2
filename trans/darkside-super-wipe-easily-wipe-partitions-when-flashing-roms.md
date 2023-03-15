# 黑暗面。超级擦除:在刷新 rom 时轻松擦除分区

> 原文：<https://www.xda-developers.com/darkside-super-wipe-easily-wipe-partitions-when-flashing-roms/>

如果你经常把定制的 rom 闪存到你的 Android 设备上，你可能会厌倦每次都要手动擦除数据、缓存、dalvik 缓存，在某些情况下，还要擦除系统分区。更糟糕的是，有时因为一些奇怪的原因，擦拭一次并不完全奏效，你必须多次擦拭以确保一切顺利。如果你能在刷新 ROM 之前刷新一个很小的 zip 文件，那会怎样？它会自动安全地为你擦除所有的分区。XDA 知名开发商[the drekjay](http://forum.xda-developers.com/member.php?u=3187759)发布了一款名为[的工具 DARKSIDE。超级擦](http://forum.xda-developers.com/showthread.php?t=1477955)自动、安全、放心的为你做以上事情。

请注意，它最初是为 [T-Mobile 三星 Galaxy S II SGH-T989](http://forum.xda-developers.com/forumdisplay.php?f=1329) 编写和测试的。然而，它可以与其他几个设备一起工作，只要它们具有相同的分区结构。包含在 flashable zip 文件中的脚本可以很容易地针对那些使用不同分区结构的设备进行修改。该工具的论坛线程有更多关于如何发现你的设备的分区结构是否相同的信息。

使用该工具很简单——只需从恢复中刷新它，就像刷新任何其他 zip 文件一样，然后刷新您选择的 rom。它会用 EXT4 文件系统格式化/system、/data 和/cache，擦除这些分区上的所有东西。

请注意，如果您想在升级到同一 ROM 的新版本时保留现有数据，请不要使用此工具。仅当您确定要进行完整的数据擦除、从头开始，或者您已经备份了数据以供以后手动恢复时，才使用它。