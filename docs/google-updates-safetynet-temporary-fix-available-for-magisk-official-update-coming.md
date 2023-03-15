# 谷歌更新安全网，Magisk 的临时补丁可用，正式更新即将到来

> 原文：<https://www.xda-developers.com/google-updates-safetynet-temporary-fix-available-for-magisk-official-update-coming/>

众所周知，安全网绕过是谷歌和社区之间的猫鼠游戏。就在上个月[谷歌还更新了 SafetyNet](https://www.xda-developers.com/magisk-developer-assures-next-magisk-beta-will-pass-safetynet-again/) ，以防止我们试图绕过 Magisk 等应用。XDA 公认的贡献者和开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 能够[迅速在他们的 Magisk beta](https://www.xda-developers.com/new-build-of-magisk-beta-13-is-now-available-and-it-can-bypass-safetynet/) 频道中进行修复，这[导致上周开始时应用程序](https://www.xda-developers.com/magisk-13-stable-branch/)的稳定更新。

谷歌在周末对 SafetyNet 进行了新的更新，多亏了 XDA 会员 collinjames 引起了我们的注意。谷歌和社区之间的这种来回博弈可能不会停止，除非谷歌重组其执行这些检查的方式。 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 之前写了这个，说[因为 Magisk 是以 root 身份运行的，而 SafetyNet 检查不是](https://forum.xda-developers.com/showpost.php?p=72666791&postcount=529)，所以社区在这里将继续有优势。

这让许多人猜测谷歌在未来的某个时候确实会转而使用一种更困难的方法。无论是哪种情况，最新的更新打破了 Magisk 当前的绕过方法，因为它已经更新为检查 Magisk 使用的许多属性。昨晚，XDA 资深成员[鸢@s](https://forum.xda-developers.com/member.php?u=3246955) 解释了谷歌方面的变化，并对这些属性为什么会存在做了一些调查。

你可以[在我们的 Magisk 论坛](https://forum.xda-developers.com/apps/magisk/safetynet-fix-pass-safetynet-2017-07-17-t3637801)阅读更多关于这个解释的内容。因此，作为临时解决方案，您需要在智能手机上使用终端模拟器应用程序，或者通过 ADB 执行以下命令...

1.  ```
    su
    ```

2.  ```
    resetprop --delete init.svc.magisk_pfs
    ```

3.  ```
    resetprop --delete init.svc.magisk_pfsd
    ```

4.  ```
    resetprop --delete init.svc.magisk_service
    ```

5.  ```
    resetprop --delete persist.magisk.hide
    ```

或者，如果您正在使用 Magisk 的核心模式特性，那么您也需要执行这个命令。。。

1.  ```
    resetprop --delete ro.magisk.disable
    ```

每次重启智能手机或平板电脑时，都需要执行这些命令，或者您可以将所有这些命令添加到/magisk/中的. sh 文件中。core/service.d/鸢@s 说他们并不清楚这到底是如何干扰 Magisk 的行为的，所以这样做风险自担。谢天谢地， [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 说他们[已经意识到了这个问题，官方修复程序将在未来](https://twitter.com/topjohnwu/status/886738183274192896)发布。

* * *