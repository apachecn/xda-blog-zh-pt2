# 【更新:时钟插件】谷歌正在 Android Q 中进行锁屏时钟定制

> 原文：<https://www.xda-developers.com/android-q-lock-screen-clock-customization/>

**更新 1(美国东部时间 9/4/19 @上午 10:54):**Android 10 源代码日前发布，证实了时钟插件确实是个东西。可悲的是，流行类型的钟面已被删除。

两天前，第一个 Android Q 测试版公开了。如果你有谷歌 Pixel 智能手机，现在就可以下载测试版。Q 中最大的新功能是全系统的[黑暗模式](https://www.xda-developers.com/android-q-dark-mode-overview/)(它已经莫名其妙地对用户隐藏了[)，隐私和权限改造(尽管泄露的](https://www.xda-developers.com/android-q-toggle-dark-theme/)[权限概览界面](https://www.xda-developers.com/android-q-privacy-permission-controls/)也被隐藏了)，以及[桌面模式](https://www.xda-developers.com/android-q-desktop-mode/)。我们一直在使用我们信任的 [APKTool](https://www.xda-developers.com/apktool-2-4-release/) 和 [JEB 反编译器](https://www.pnfsoftware.com/?aid=xdadev)来挖掘该版本，以找到所有隐藏的功能，如[新手势](https://www.xda-developers.com/android-q-navigation-gesture-controls/)和[活动边缘重新映射](https://www.xda-developers.com/android-q-google-pixel-2-pixel-3-remap-active-edge/)，它们可能会在[最终 Q 版本](https://www.xda-developers.com/android-q-beta-release-schedule/)中出现。我们发现的另一个功能是锁屏时钟定制。

如下图所示，谷歌正致力于让你自定义锁屏时钟的外观。他们已经创建了 3 种不同的自定义时钟预设，可以通过更改隐藏设置的值立即启用。预设时钟包括文本时钟、气泡时钟和拉伸模拟时钟。所有这些定制时钟都是不完整的，因为它们缺少日期和天气，但它们确实可以与 Pixel 2 和 Pixel 3 的始终显示一起工作。气泡时钟和拉伸时钟也显示了标准的数字时钟，如果这个功能进入最终的 Android Q 版本，可能就不是这样了。

要在 Android Q 上启用这些自定义时钟，请遵循以下说明。

**要求:**

*   运行 Android Q beta 的谷歌 Pixel、Pixel XL、Pixel 2、Pixel 2 XL、Pixel 3 或 Pixel 3 XL
*   在 Windows、Linux 或 macOS PC 上设置的 Android 调试桥(ADB)。说明可以在[这里找到](https://www.xda-developers.com/install-adb-windows-macos-linux/)。

运行以下命令之一来更改锁屏时钟。该命令立即生效:

**泡泡时钟:**

```
 adb shell settings put secure lock_screen_custom_clock_face "com.android.keyguard.clock.BubbleClockController" 
```

**拉伸模拟时钟:**

```
 adb shell settings put secure lock_screen_custom_clock_face "com.android.keyguard.clock.StretchAnalogClockController" 
```

**文字时钟:**

```
 adb shell settings put secure lock_screen_custom_clock_face "com.android.keyguard.clock.TypeClockController" 
```

**正常时钟:**

```
 adb shell settings delete secure lock_screen_custom_clock_face 
```

对于任何感兴趣的开发人员，下面是 SystemUIGoogle 的 ClockManager 类中的相关方法:

### 锁定屏幕上自定义钟面的代码

```
 private void register() {
String str = "lock_screen_custom_clock_face";
this.mContentResolver.registerContentObserver(Secure.getUriFor(str), false, this.mContentObserver);
ExtensionBuilder newExtension = this.mExtensionController.newExtension(ClockPlugin.class);
newExtension.withPlugin(ClockPlugin.class);
newExtension.withCallback(this.mClockPluginConsumer);
newExtension.withDefault(new SettingsGattedSupplier(this.mContentResolver, str, BubbleClockController.class.getName(), new C0386-$$Lambda$ClockManager$LL3RUa19AVegk9Mkg8eS_BmuG7o(this)));
newExtension.withDefault(new SettingsGattedSupplier(this.mContentResolver, str, StretchAnalogClockController.class.getName(), new C0387-$$Lambda$ClockManager$aVyrwGQVcB_VpjAEn9xTWGKpSj8(this)));
newExtension.withDefault(new SettingsGattedSupplier(this.mContentResolver, str, TypeClockController.class.getName(), new C0384-$$Lambda$ClockManager$0RLVFJyrdkzcA8PsTIu0AOgpy1E(this)));
this.mClockExtension = newExtension.build();
} 
```

这些定制时钟是作为 SystemUI 的插件开发的。我们可能会在未来 Android Q 版本的 SystemUI 调谐器中看到它们，或者我们可能永远不会以任何用户可访问的方式看到它们。谷歌一直在开发类似的新功能，遗憾的是，其中许多功能从未出现在设置应用中。其中一个最显著的例子就是 Android 7 Nougat 中的[隐藏导航栏调谐器](https://www.xda-developers.com/nav-bar-customization-was-hidden-in-stock-nougat-all-along-and-it-never-needed-root/)。如果锁屏时钟定制确实在未来的 Android Q beta 版本中发布，我们会让你们都知道。

[**更多安卓 Q 新闻、小技巧、小窍门**](https://xda-developers.com/tag/android-q)

* * *

**更新 1(美国东部时间 2019 年 7 月 18 日晚 7 点):**谷歌在 Q beta 4 中移除了 TypeClockController，他们还更改了 Stretch 模拟时钟。要启用拉伸模拟时钟，请输入:

`adb shell settings put secure lock_screen_custom_clock_face "com.android.keyguard.clock.AnalogClockController"`

气泡时钟命令保持不变。

* * *

## 更新 Android 10 中的时钟插件

正如在 AOSP 的 [readme 页面](https://android.googlesource.com/platform/frameworks/base/+/android10-release/packages/SystemUI/docs/clock-plugins.md)上详细描述的，谷歌增加了一个 ClockPlugin 插件接口，允许定制出现在锁定屏幕和永远显示屏幕上的时钟。因为时钟是“电池消耗和屏幕老化的高风险”，所以建议 OEM 厂商将目标设定为“最大开像素比(OPR)为 5%。”此外，谷歌建议时钟“不应该由大的实心色块组成，时钟应该在屏幕上移动，以将 on 像素分布在大量像素上。”在实现时钟之后，谷歌建议进行老化测试。

谷歌目前在 AOSP Android 10 中支持两种自定义钟面:拉伸模拟和气泡。该公司[移除了](https://android.googlesource.com/platform/frameworks/base/+/583067c4e4799b0a633d8e861698c8fc2a5c7a6f%5E%21/#F2)对钟面类型的支持，尽管没有解释原因。