# Android 11 的电源菜单可能变成家庭自动化的控制中心

> 原文：<https://www.xda-developers.com/google-android-11-power-menu-control-center-shortcuts/>

**更新 2(美国东部时间 2/20/2020 @ 7:00PM):**Kieron Quinn 向我们发送了一张截图，显示了更明确的证据，表明这个控制 API 旨在在 Android 11 电源菜单中显示家庭自动化控制。

**更新 1(美国东部时间 2/20/2020 @下午 5:30):**我们发现了可能解释谷歌为什么致力于这项功能的证据:提供家庭自动化控制的快速访问！更多信息如下。原文如下。

当谷歌昨天发布安卓 11 开发者预览版 1 时，我们在最初的动手操作中发现[主要是表层变化](https://www.xda-developers.com/android-11-developer-preview-changes/)。在谷歌 I/O 2020 发布公告[后，谷歌似乎将再次把大部分用户界面变化和新功能留给](https://www.xda-developers.com/google-i-o-2020-may-12-14/)[公共测试版](https://www.xda-developers.com/android-11-2-more-developer-previews-3-betas-before-stable/)。然而，我们发现了几个正在开发中的用户界面调整，表明 2020 年安卓操作系统将发生巨大的变化。我们发现谷歌可能在快速设置面板[中放置](https://www.xda-developers.com/custom-rom-throwback-android-11-tests-separating-quick-settings-panel-from-notification-shade/)[媒体播放器，将通知阴影](https://www.xda-developers.com/android-11-music-player-quick-settings-panel/)从快速设置面板中分离出来，现在，我们发现谷歌可能正在调整电源菜单，以适应用户选择的家庭自动化快捷方式。

在我运行 Android 11 DP1 的 Pixel 2 XL 上，我设法为长按电源菜单激活了一个新的 UI，如下所示。现有的电源菜单图标，包括紧急、截图、重启和关机，都转移到了屏幕的顶部，在下面留下了大量的空白空间。此外，图标上方会出现一个新的“主页”文本。图标向上移动表明谷歌计划添加*一些东西*来填补空白，我们最初认为这是为现在 Android 11 中的[新快速访问钱包功能](https://www.xda-developers.com/android-10-11-developer-preview-quick-access-wallet-google-pay/)做准备。然而,“Home”文本的出现提出了一个问题，为什么它会在那里——谷歌会不会正在为不同种类的操作在 power 菜单中创建类别？

深入研究代码，我们发现 SystemUIGoogle 中有多个类与一个名为“控件”的特性相关。该代码建议用户可以将快捷方式设置为“收藏夹”以显示在该菜单中，这些快捷方式由系统存储在一个 XML 文件中，其中包含快捷方式的 id、标题、类型和组件。SystemUIGoogle 中有与控件相关的新活动:ControlsFavoritingActivity 和 ControlsProviderSelectorActivity。启动前者会导致权限拒绝，因为它是未报告的活动，并且我们没有 root 访问权限，而启动后者会出现以下 UI:

不幸的是，这个用户界面目前是空的，所以我们不能添加我们自己喜欢的快捷方式到电源菜单。我们发现了对一个名为“android . permission . bind _ CONTROLS”的新权限和一个名为“Android . service . CONTROLS . CONTROLS providerservice”的新服务的引用，这表明第三方应用程序将能够创建一个 Android 系统可以绑定并显示在该列表中的“CONTROLS”服务，就像快速设置磁贴一样。没有支持“控件”API 的第三方应用程序可以解释为什么上面显示的活动目前是空的。

看起来谷歌正在从 iOS 控制中心获得线索，尽管我们不完全确定谷歌为什么首先要开发这个功能，因为快速设置面板已经存在，并且可以填充自定义快捷键。我们将跟踪这项功能的发展，以防在未来的 Android 11 开发者预览版中有任何变化。

**[安卓 11 XDA 新闻](https://xda-developers.com/tag/android-11)**

## 更新 1:可能用于家庭自动化控制

发表这篇文章后，XDA 认识到开发人员 Quinny899 向我们通报了他自己的发现。Android 11 中更新的 framework.jar 揭示了什么样的快捷方式可能会出现在电源菜单的“控制”菜单中。他发现了在控制服务中被接受为“有效设备类型”的设备类型列表。以下是完整列表:

### Android 11 控件 API 支持的家庭自动化设备类型

```
 private static final int NUM_CONCRETE_TYPES = 51;
private static final int NUM_GENERIC_TYPES = 7;
public static final int TYPE_AC_HEATER = 1;
public static final int TYPE_AC_UNIT = 2;
public static final int TYPE_AIR_FRESHENER = 3;
public static final int TYPE_AIR_PURIFIER = 4;
public static final int TYPE_AWNING = 33;
public static final int TYPE_BLINDS = 34;
public static final int TYPE_CAMERA = 50;
public static final int TYPE_CLOSET = 35;
public static final int TYPE_COFFEE_MAKER = 5;
public static final int TYPE_CURTAIN = 36;
public static final int TYPE_DEHUMIDIFIER = 6;
public static final int TYPE_DISHWASHER = 24;
public static final int TYPE_DISPLAY = 7;
public static final int TYPE_DOOR = 37;
public static final int TYPE_DOORBELL = 51;
public static final int TYPE_DRAWER = 38;
public static final int TYPE_DRYER = 25;
public static final int TYPE_FAN = 8;
public static final int TYPE_GARAGE = 39;
public static final int TYPE_GATE = 40;
public static final int TYPE_GENERIC_ARM_DISARM = -5;
public static final int TYPE_GENERIC_LOCK_UNLOCK = -4;
public static final int TYPE_GENERIC_ON_OFF = -1;
public static final int TYPE_GENERIC_OPEN_CLOSE = -3;
public static final int TYPE_GENERIC_START_STOP = -2;
public static final int TYPE_GENERIC_TEMP_SETTING = -6;
public static final int TYPE_GENERIC_VIEWSTREAM = -7;
public static final int TYPE_HEATER = 0x2F;
public static final int TYPE_HOOD = 10;
public static final int TYPE_HUMIDIFIER = 11;
public static final int TYPE_KETTLE = 12;
public static final int TYPE_LIGHT = 13;
public static final int TYPE_LOCK = 45;
public static final int TYPE_MICROWAVE = 14;
public static final int TYPE_MOP = 26;
public static final int TYPE_MOWER = 27;
public static final int TYPE_MULTICOOKER = 28;
public static final int TYPE_OUTLET = 15;
public static final int TYPE_PERGOLA = 41;
public static final int TYPE_RADIATOR = 16;
public static final int TYPE_REFRIGERATOR = 0x30;
public static final int TYPE_REMOTE_CONTROL = 17;
public static final int TYPE_SECURITY_SYSTEM = 46;
public static final int TYPE_SET_TOP = 18;
public static final int TYPE_SHOWER = 29;
public static final int TYPE_SHUTTER = 42;
public static final int TYPE_SPRINKLER = 30;
public static final int TYPE_STANDMIXER = 19;
public static final int TYPE_STYLER = 20;
public static final int TYPE_SWITCH = 21;
public static final int TYPE_THERMOSTAT = 49;
public static final int TYPE_TV = 22;
public static final int TYPE_UNKNOWN = 0;
public static final int TYPE_VACUUM = 0x20;
public static final int TYPE_VALVE = 44;
public static final int TYPE_WASHER = 0x1F;
public static final int TYPE_WATER_HEATER = 23;
public static final int TYPE_WINDOW = 43; 
```

有可能谷歌会允许你通过 Android 11 中的电源菜单来控制你的智能家电。这个解释在“home”文本出现在顶部的上下文中是有意义的。如果我们对这个功能有了更多的了解，或者我们设法让我们自己的快捷方式出现在菜单中，我们会及时更新。

## 更新 2:控件提供者被黑客攻击显示了一个定制的“灯泡”应用程序

这里有一个由开发者 Kieron Quinn 提供的截图，展示了他在 Android 11 的“控件提供者”活动中组装并设法出现的快速“灯泡”应用程序。点击图标会导致系统崩溃。如果我们能让它继续工作，我们会更新这篇文章。