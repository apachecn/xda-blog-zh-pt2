# Magisk v13.3 现在绕过了谷歌最新的安全网检查

> 原文：<https://www.xda-developers.com/magisk-v13-3-is-now-available-bypasses-googles-latest-safetynet-protections/>

# Magisk v13.3 现已推出，绕过了谷歌最新的安全网保护

谷歌本周早些时候更新了 SafetyNet，但现在 Magisk 的新版本已经推出，可以绕过最近的这些检查。

和往常一样，SafetyNet 游戏继续与 Magisk 开发商的最新活动进行互动。就在几天前，[我们报道了新的安全网更新，该更新阻止 Magisk v13.2](https://www.xda-developers.com/google-updates-safetynet-temporary-fix-available-for-magisk-official-update-coming/) 和更低版本绕过其检查。当时，多亏了 XDA 资深成员[鸢@s](https://forum.xda-developers.com/member.php?u=3246955) ，才有了一个临时补丁。这对那些尝试过的人来说是有效的，但是每次你启动手机或平板电脑时都必须应用它。

XDA 公认的贡献者和开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 告诉我们，他们正在对 Magisk 进行更新，它将能够绕过最新的安全网更新。所以昨天下午 Magisk 和 Magisk Manager 都有了新的更新，应用了这些新的变化。 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 告诉我们，谷歌现在针对安全网的最新更新系统道具，所以这一次的解决方案是 Resetprop。

通过这一改变，Magisk 现在能够解析所有的系统属性，然后删除 Google 不喜欢的属性。这也意味着 Magisk 卸载程序已经更新，因为它删除了以前版本的 Magisk 留下的所有 persist 系统属性。说他们已经研究了许多方法来使 Magisk 隐藏在新的安全网检查之外。因此，除非谷歌做一些激进的事情，那么开发者应该在安全网更新后很快就会有修复程序。

昨天发生的另一个变化是 Magisk Manager 更新到 5.1.0 版本。我们被告知，它已经大规模重写了许多代码，其中大部分是在引擎盖下更改的。一个新的视觉变化是，当应用程序自我更新时，你会看到一个滚动的日志屏幕，看看安装程序对你的设备做了什么。你可以看看下面的视频。

[**魔法论坛**](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445/post73079059#post73079059)