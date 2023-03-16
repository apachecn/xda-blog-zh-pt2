# Discord 测试了新的底部标签设计和滑动手势控制

> 原文：<https://www.xda-developers.com/discord-android-bottom-tab-redesign-swipe-gestures/>

# Discord 测试了新的底部标签设计和滑动手势控制

Discord 正在测试 Android 上的一个重大重新设计，底部标签用于按钮和滑动手势来打开侧边栏菜单。

当我们都被困在家里喝一杯冰啤酒，等待这一切过去的时候，我们增加了对消息应用的使用，以与我们的朋友和家人保持联系。有数百种消息应用程序，其中许多在特定地区或特定人群中更受欢迎。Discord 现在是更受欢迎的聊天应用之一，此前它已经超越了最初只为游戏玩家提供消息服务的基础。该应用程序的开发人员高度参与社区，并经常进行 A/B 测试，以了解人们对新 UI 和行为变化的反应。少数用户正在试验的变化之一是重新设计 Android 应用程序，在底部栏放置许多按钮。一个额外的实验允许用户在聊天中向左或向右滑动以打开参与者列表和/或服务器/频道列表。

以下是展示新底部标签设计和滑动手势控制的屏幕记录:

https://gfycat.com/ifr/HighlevelAdeptBinturong

就个人而言，我是这些变化的忠实粉丝，因为它们允许更好的单手使用。Discord 团队已经将您可能会按下的大多数按钮移到了屏幕的更下方。聊天屏幕中的操作栏现在是多余的，所以如果它在这个实验的未来迭代中消失，我不会感到惊讶。

这些实验最初是由 XDA 资深会员 [Some_Random_Username](https://forum.xda-developers.com/member.php?u=8234677) 引起我们注意的。我们证实，这些变化正在我们自己的设备上进行测试，这些设备运行最新的 Android alpha 版本的 Discord。用户可以通过修改`/data/data/com.discord/shared_pref`中的`com.discord_preferences.xml`共享偏好文件并添加行`<int name="CACHE_KEY_TABS_EXPERIMENT_BUCKET" value="N" />`来手动启用这个实验，其中 N 是 0、1 或 2。输入 0 表示用户退出实验，而输入 1 仅显示底部标签重新设计，输入 2 显示底部标签并启用滑动手势。

* * *

你怎么看待这些变化？对了，[我们有一个不和谐服务器](https://discord.gg/EhaMzy2)！