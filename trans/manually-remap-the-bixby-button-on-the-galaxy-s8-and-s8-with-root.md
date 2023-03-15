# 用 Root 手动重新映射 Galaxy S8 和 S8+上的 Bixby 按钮

> 原文：<https://www.xda-developers.com/manually-remap-the-bixby-button-on-the-galaxy-s8-and-s8-with-root/>

# 用 Root 手动重新映射 Galaxy S8 和 S8+上的 Bixby 按钮

按照这些说明，使用设备上的 Root 访问权限手动重新映射三星 Galaxy S8 和 S8+上的 Bixby 按钮。

当三星首次透露他们将在 [Galaxy S8](https://forum.xda-developers.com/galaxy-s8) 和 [Galaxy S8+](https://forum.xda-developers.com/galaxy-s8+) 的侧面为他们的新个人助理设置一个专用按钮时，许多人都感到惊讶。索尼在他们的许多智能手机上都有一个专用按钮，但它是用来用相机拍照的。这已经是一个被很多发烧友重新映射过的按钮，按钮重新映射本身从一开始就在 Android 上完成。因此，即使你不介意使用三星旗舰机上的 Bixby 按钮，那么至少你希望有一个重新映射它的选项。

这正是用户开始做的。这是在 YouTube 视频中首次演示的[,用户只需安装](https://www.xda-developers.com/how-to-remap-the-bixby-button-on-the-galaxy-s8-s8-to-launch-google-assistant/)[一体化手势](https://play.google.com/store/apps/details?id=com.phoenixstudios.aiogestures&hl=en)应用程序来重新映射按钮。这使你能够启动谷歌助手，而不是三星的 Bixby 助手。三星最初的限制是缺乏选项，这意味着如果你想将它用于 Bixby 按钮，那么你可以正常使用它。但是如果你想把它用在别的地方，你就需要安装一个应用程序来重新映射它。

然而，这场派对并没有持续多久，因为三星几乎立即[开始推出 OTA 更新](https://www.xda-developers.com/samsung-has-removed-the-ability-to-remap-the-bixby-button-on-the-galaxy-s8s8/)来禁用这一重新映射功能。这在技术上仍然是可能的，但在这次 OTA 更新后出现的大多数解决方案只是在 Bixby 服务启动后将其杀死，然后启动一个你选择的应用程序。[上周我们发现了三个这样的例子](https://www.xda-developers.com/3-applications-bypass-bixby-restriction/)，它们都可以在没有 root 权限访问你的智能手机的情况下工作，并且取得了不同程度的成功。

但是，如果您拥有 root 访问权限，则可以手动将此按钮重新映射到许多其他选项。XDA 资深会员 [redplate](https://forum.xda-developers.com/member.php?u=1553263) 最近[在我们的 Galaxy S8+ guides 论坛](https://forum.xda-developers.com/galaxy-s8+/how-to/root-remap-bixby-button-o-app-t3601061)上写了一篇教程，详细介绍了如何操作。mod 的工作原理是编辑位于 **/system/usr/keylayout** 目录下的 **Generic.kl** 文件。其他用户也提出了一些建议，包括谷歌助手、启动相机、启动音乐播放器、音量按钮、home 按钮、电源按钮等等。

**前往[论坛主题](https://forum.xda-developers.com/galaxy-s8+/how-to/root-remap-bixby-button-o-app-t3601061)获取完整的指令集！**