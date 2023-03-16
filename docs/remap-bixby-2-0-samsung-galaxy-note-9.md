# 如何在三星 Galaxy Note 9 上重新映射 Bixby 2.0

> 原文：<https://www.xda-developers.com/remap-bixby-2-0-samsung-galaxy-note-9/>

三星随三星 Galaxy Note 9 发布了 Bixby 2.0。Bixby 2.0 承诺比去年与三星 Galaxy S8 和 Galaxy S8+一起推出的 Bixby 1.0 好得多。我已经使用三星 Galaxy Note 9 几天了，在我看来，Bixby 2.0 基本上与 1.0 相同，但缺少一些我喜欢的功能。所以像任何正常人一样，我找到了重新映射它的方法。以下是如何在 Galaxy Note 9 上安装和使用 Bixby 2.0 的两个最佳重新映射应用程序的说明。

## 在三星 Galaxy Note 9 上重新映射 Bixby 2.0

### 选项 1:按钮映射器

按钮映射器可以让你重新映射手机上的任何按钮，但就我们的目的而言，它可以让你重新映射 Galaxy Note 9 上的 Bixby 按钮。这个应用程序比选项二更可靠，但它也有一个缺点。你需要在每次重启手机时运行这个脚本。你可以按照下面的教程来设置它。

1.  从谷歌 Play 商店安装[按钮映射器](https://play.google.com/store/apps/details?id=flar2.homebutton)。
2.  在电脑上设置 ADB。您可以按照本指南进行安装。
3.  打开设置>关于手机>软件信息，点击 7 次内部版本号，启用 ADB。一旦你这样做，输入你的密码，并返回两次。您现在可以进入开发者选项菜单。只需切换 USB 调试开关来启用 ADB。
4.  打开按钮映射应用程序，在窗口的底部，会有一个弹出窗口，要求您启用辅助功能服务。然后，您只需为按钮映射器启用辅助功能服务。
5.  选择应用程序顶部的 Bixby 按钮选项。然后单击自定义按钮。一旦你这样做了，你将需要运行以下命令:

    ```
     adb shell sh /data/data/flar2.homebutton/keyevent.sh 
    ```

    然后

    ```
     adb shell sh /data/data/flar2.homebutton/keyevent.sh -d 
    ```

6.  每次重启手机时，您都需要运行第二个命令。这也将禁用 Bixby Voice。如果你没有禁用 Bixby Voice，它会在你每次按下按钮时打开，并显示你重新映射的内容。您可以使用以下命令重新启用 bix by Voice:

    ```
     adb shell sh /data/data/flar2.homebutton/keyevent.sh -e. 
    ```

7.  您可以在单击和长按菜单中选择想要使用的任何选项。你可以设置它做一些事情，比如打开谷歌助手或切换手电筒。

这个应用程序在使用中似乎更好一点，因为它禁用了 Bixby 语音并重新映射它。缺点是，每次重启手机时，你都必须运行 ADB 命令。如果你不想每次重启手机都要运行这个命令，那么选项 2 将适合你。

### 选项 2: bxActions

bxActions 是一款自去年三星 Galaxy S8 和三星 Galaxy S8+推出以来就一直在做 Bixby 重新映射的应用。这个应用程序非常可靠，可以在三星 Galaxy Note 9 上重新映射 Bixby，但 Bixby Voice 仍然安装在上面，所以可能会有一些兼容性问题。开发者正在积极开发应用程序，所以如果你发现任何错误，你应该期待他们被修复。

1.  加入[公测](https://play.google.com/apps/testing/com.jamworks.bxactions)进行比拼，然后[安装 app](https://play.google.com/store/apps/details?id=com.jamworks.bxactions) 。
2.  在你的电脑上安装 [ADB。你可以按照这个指南来安装它。](https://www.xda-developers.com/install-adb-windows-macos-linux/)
3.  打开设置>关于手机>软件信息，点击 7 次内部版本号，启用 ADB。一旦你这样做，输入你的密码，并返回两次。您现在可以进入开发者选项菜单。只需切换 USB 调试开关来启用 ADB。
4.  打开 bxActions，按照提示给予它所需的权限。
5.  选择 Bix 按钮选项，并点击红色框，上面写着“请使用电脑解锁权限”
6.  运行两个命令:

    ```
     adb shell pm grant com.jamworks.bxactions android.permission.WRITE_SECURE_SETTINGS
    adb shell pm grant com.jamworks.bxactions android.permission.READ_LOGS 
    ```

7.  一旦你这样做，关闭并重新打开应用程序。
8.  现在，您可以选择想要用来重新映射三星 Galaxy Note 9 上的 Bixby 按钮的选项。这个应用程序有类似谷歌助手和手电筒开关的动作。

这个应用程序确实很好，但在我的经验中，它并不总是像按钮映射器那样可靠。它的优点是只需要启用一次。你甚至不需要运行 adb 命令，但它确实使应用程序更快、更可靠。这个应用程序一点也不差——我要说就其功能而言，它可能是最好的。只是有时候，我在我的 Galaxy Note 9 上发现它不可靠。

## 在 Galaxy Note 9 上重新映射 Bixby 能让你做什么

按钮映射器可以让你将三星 Galaxy Note 9 上的 Bixby 按钮重新映射到长按或单按。完成后，您可以将其重新映射到下面列表中的一个操作。Zello 也有选项，这是一个对讲机应用程序。有 Pro 选项可以在锁定时禁用 Bixby，并在按下按钮时振动。

*   默认
*   主页
*   背部
*   最近的应用
*   显示菜单
*   最后一个应用程序
*   关掉屏幕
*   切换手电筒
*   电源对话框
*   屏幕上显示程序运行的图片
*   分画面银幕
*   任务者意图
*   请勿打扰
*   切换静音/振动
*   静音音量
*   静音麦克风
*   音量+
*   音量-
*   上一首曲目
*   下一首曲目

*   播放/暂停
*   向上滚动
*   向下滚动
*   复制
*   粘贴
*   杀死前台应用程序
*   快速设置
*   通知
*   清除通知
*   亮度+
*   亮度-
*   切换自动亮度
*   切换蓝牙
*   切换 WiFi
*   切换纵向
*   更换键盘
*   打开 URL
*   Zello PTT(仅专业版)
*   搜索
*   助理
*   打开任何应用程序

bxActions 有单按和长按选项，以及长按锁屏。长按和长按锁定屏幕都需要解锁专业模式，价格为 3 美元。您可以将三星 Galaxy Note 9 上的 Bixby 按钮重新映射到以下操作。

*   禁用 Bixby
*   启用 Bixby
*   主页
*   背部
*   电话(拨号程序)
*   照相机
*   启动应用程序
*   启动快捷操作
*   启动 Tasker 任务(专业版)
*   Google Now
*   谷歌助手
*   Google assistant extra(支持直接语音输入和“我的屏幕上有什么”操作
*   媒体播放/暂停
*   下一个媒体
*   提高音量
*   降低音量
*   请勿打扰(静音)

*   声音模式(声音、振动、静音)
*   声音模式 iOS(声音、振动)(专业版)
*   任务管理器
*   电源菜单
*   通知中心
*   设置托盘
*   切换自动旋转
*   切换分屏(专业版)
*   手电筒(系统)
*   手电筒(额外电源)
*   截图
*   全屏打开/关闭
*   当前应用程序的全屏显示
*   全部取消并将所有通知标记为已读(专业版)
*   标记为已读(专业版)
*   抬头通知开/关(专业版)
*   用 Samsung Capture 截图(Pro 和 root)

在我看来，Bixby 2.0 在 Galaxy Note 9 上并没有那么伟大。幸运的是，我们有了不起的开发者，他们也同意这一点，并致力于将应用程序重新映射到更有用的功能，如谷歌助手。