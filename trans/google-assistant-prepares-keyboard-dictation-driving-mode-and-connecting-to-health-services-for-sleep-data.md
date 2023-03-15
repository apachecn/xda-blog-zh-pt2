# 谷歌助手准备键盘听写，驾驶模式和更多

> 原文：<https://www.xda-developers.com/google-assistant-prepares-keyboard-dictation-driving-mode-and-connecting-to-health-services-for-sleep-data/>

谷歌助手已经成为许多人生活的中心，一个可以分享信息、控制设备和提供关键提醒的工具。我们深入研究了最新的谷歌应用程序更新，看看谷歌助手还能做什么，我们发现了一些新功能，包括针对特定像素设备的键盘听写和专用驾驶模式。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

## **谷歌助手驾驶模式**

谷歌应用程序版本 11.31.9.29 今天在谷歌 Play 商店推出，有迹象表明谷歌助手的驾驶模式可能最终启动。我们设法展示了新功能的 onboarding UI，尽管不幸的是我们无法实际启动新的驾驶模式。

谷歌助手的驾驶模式是在 2019 年的 I/O 上首次公布的，在那里我们[第一次看到了](https://www.xda-developers.com/google-assistant-driving-mode-android-auto-redesign-video/)。这意味着[将取代手机的 Android Auto 应用](https://www.xda-developers.com/android-auto-app-no-longer-supported-google-assistant-new-driving-mode/)，尽管谷歌仍将通过一个单独的应用提供手机界面，作为旧用户界面的快捷方式。自从它在 I/O 2019 上被取笑以来，我们一直在等待这款 Android 自动替代产品，看起来我们不用等太久就可以上线了。

然而，看起来最终的用户界面会和我们预期的有点不同。事实上，上周谷歌地图为一些用户展示的[新车模式用户界面](https://www.xda-developers.com/google-maps-tests-car-mode-ui-bigger-buttons/)与截图中显示的更接近。新的汽车模式用户界面非常简洁，让人想起 Android Auto for Android，它本身提供了一个简洁的界面，可以快速访问功能和服务。

谷歌地图中新的汽车模式用户界面可能是谷歌助手即将推出的驾驶模式的一部分。演职员表:[安卓警察](https://www.androidpolice.com/2020/09/27/google-maps-is-getting-a-dedicated-car-mode-ui/)

## **新谷歌助手键盘听写**

我们还能够启用新的谷歌助手的集成键盘听写功能，如下图所示，在一个 [Pixel 4](https://forum.xda-developers.com/pixel-4) 上运行。在 Gboard 中，你可以点击麦克风按钮来口述信息并发送(或删除)它们，而无需狂热地打字。你已经可以通过集成的语音输入做到这一点，但一旦这个版本的功能推出，你就不必在 Gboard 中下载独立的语音模型。这将节省一些存储空间，但新的谷歌助手的设备上机器学习模型应该能够更快更准确地进行语音听写。

正如您在我们的快速动手演示中所看到的，新功能无缝集成到键盘中，并且在口述信息方面做得很好。当然，我们在它正式发布之前就激活了它，所以它可能运行得不太顺畅。上一次我们看到这个功能的时候，它要慢得多，尽管那是因为它运行在一个改进的第一代 Pixel 设备上。键盘听写界面也有点不同，所以我们不确定这两个界面中的哪一个会成为最终版本。不过，我们有望很快找到答案。

新的谷歌助手仅在 [Pixel 4](https://forum.xda-developers.com/pixel-4) 、 [Pixel 4a](https://forum.xda-developers.com/pixel-4a) 、 [Pixel 4a 5G](https://forum.xda-developers.com/pixel-4a-5g) 和 [Pixel 5](https://forum.xda-developers.com/pixel-5) 上可用。因此，这种新的键盘听写功能很可能也仅限于这些设备。

## **连接到健康服务获取睡眠数据**

最后，谷歌应用程序版本 11.31.9.29 的新字符串表明，你可以将谷歌助手连接到健康服务提供商，如 Fitbit，以便让助手访问你的睡眠数据。

```
 <string name="sleep_account_linking_action_button_positive">Connect</string>
<string name="sleep_account_linking_legalese">&lt;p> Your Assistant will get access to your &lt;xliff:g id=provider example=Fitbit>%1$s&lt;/xliff:g> sleep data. Google Assistant will use this data to answer your sleep-related questions across your devices that have personal results turned on. &lt;/p>&lt;p> On devices where you have proactive health and fitness results turned on, the Assistant will show this data, suggestions, and related content without you having to ask. This data also helps troubleshoot and improve your health and fitness experience with the Assistant. Once your Assistant successfully fulfills your request to update, show, or answer questions about this data, Google will delete your audio query. The text from your request and other Assistant usage information is used to troubleshoot, develop, and improve Assistant services. &lt;/p>&lt;p> &lt;b>Things to know&lt;/b> &lt;ul> &lt;li>Disconnect your Assistant from &lt;xliff:g id=provider example=Fitbit>%1$s&lt;/xliff:g> in your Assistant settings.&lt;/li> &lt;li>Turn off personal results, or just your proactive health and fitness results, in your Assistant settings.&lt;/li> &lt;li>Review and delete your Assistant activity at myactivity.google.com.&lt;/li> &lt;/ul> &lt;/p></string>
<string name="sleep_account_linking_legalese_title">Connect %1$s to your Google Assistant?</string> 
```

根据字符串，一旦连接到健康服务，谷歌助理将能够使用你的睡眠数据来回答睡眠相关的问题。如果您的设备打开了主动健康和健身结果，Assistant 将显示这些数据以及建议和相关内容，无需您询问。

* * *

*感谢 PNF 软件为我们提供了使用* *[JEB 反编译](https://www.pnfsoftware.com/?aid=xdadev)* *的许可，这是一款针对 Android 应用的专业级逆向工程工具。*