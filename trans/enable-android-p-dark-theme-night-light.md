# 夜灯开着怎么启用 Android P 的黑暗主题

> 原文：<https://www.xda-developers.com/enable-android-p-dark-theme-night-light/>

# 夜灯开着怎么启用 Android P 的黑暗主题

你有没有想过让 Android P 的黑暗主题只有在夜灯开启的情况下才能自行启用？如果你有 Android P DP4，那你也可以！

在谷歌 Pixel 2 中，谷歌添加了一个部分系统深色主题，当你有深色壁纸时就会应用。随着 Android 8.1 Oreo 更新和最新的 Android P Beta 3/Developer Preview 4，该功能出现在最初的 Google Pixel 和其他设备上，你不再需要有深色壁纸来使用深色主题。如果你曾经想让黑暗模式变得更智能一点，我们知道如何自动化它，所以你可以在它启用之前应用任何条件。最好的部分是它**不需要根**！

作为参考，黑暗主题只为 SystemUI 和 Google Pixel Launcher 的部分主题，如快速设置面板、音量面板、文件夹背景和应用程序抽屉背景。获得全系统黑暗主题的唯一方法是要么继续使用 Android Oreo 并使用 Substratum 主题，要么让你的 Android P 设备使用 Substratum。我们意识到让你的设备根化并不是你们中的一些人想要做的事情，所以我们一直在寻找不需要根的定制选项。由于最新的 Android P 测试版，现在可以自动应用黑暗主题，例如，我们可以只在夜灯打开时启用黑暗模式。

## 用夜灯触发 Android P 的黑暗主题

我们正在做的事情的简要说明。最新的 Android P beta 允许你在显示设置中手动切换黑暗主题。因此，一个新的设置。安全值是由 Google 创建的，用于保存此设置的当前值(设置。Secure.theme_mode 其中 0 是自动基于壁纸，1 是亮主题，2 是暗主题。)通过 ADB 或具有适当权限的应用程序手动更改该值允许我们更改主题。使用最新的 Tasker beta 版本，我们可以监控设置的变化，我们可以监控夜间灯光状态，然后随意切换主题变化。

### 要求

*   你必须使用 Android P Beta 3/Developer Preview 4 才能在没有 root 用户的情况下工作。该版本在发布时适用于以下设备:
    *   谷歌像素
    *   谷歌像素 XL
    *   谷歌像素 2
    *   谷歌像素 2 XL
    *   基本电话( [PH-1](https://www.xda-developers.com/essential-phone-android-p-beta-3-july-security/) )
    *   索尼 Xperia XZ2

*   您需要安装自动化应用程序“Tasker ”,并且您需要使用最新的测试版 , v5.2.bf6。
*   您需要通过亚洲开发银行授予 Tasker 特别许可。安装最新的 Tasker 测试版后，按照此处所述设置 ADB [，并在命令提示符/PowerShell/终端中输入以下命令。](https://www.xda-developers.com/install-adb-windows-macos-linux/)
    *   Windows 命令提示符:

        ```
         adb shell pm grant net.dinglisch.android.taskerm android.permission.WRITE_SECURE_SETTINGS 
        ```

    *   Windows PowerShell:

        ```
         .\adb shell pm grant net.dinglisch.android.taskerm android.permission.WRITE_SECURE_SETTINGS 
        ```

    *   macOS/Linux 终端:

        ```
         ./adb shell pm grant net.dinglisch.android.taskerm android.permission.WRITE_SECURE_SETTINGS 
        ```

[app box Google play net . dinghly . Android . task erm]

### 说明

以下是如何设置的分步说明。最后，我还会包含一个导入它的链接。

### ![Tasker](img/3b0c1b3d97d6513f36475ca193adac38.png)

1.  打开 Tasker 并创建一个新的配置文件。命名为“夜间自动黑暗主题。”
2.  选择状态上下文。
3.  选择系统类别。
4.  选择自定义设置选项。
5.  对于类型，选择“安全”。输入“夜间显示激活”作为名称。对于该值，输入“1”。
6.  进入任务创建(不需要给任务命名。)
7.  添加一个操作。
8.  选择设置类别。
9.  选择自定义设置。
10.  对于类型，选择“安全”。对于名称，输入“主题模式”。对于该值，输入“2”。这将在夜灯开启时启用黑暗主题。
11.  退出任务创建并返回 Tasker 的主屏幕。
12.  长按您创建的任务，然后选择“添加退出任务”
13.  重复步骤 7-10，但对于步骤 10 中的值，输入“1”。当夜灯关闭时，这将禁用黑暗主题。
14.  你完了。现在 Tasker 会自动切换黑暗模式，每当夜灯被切换。您可以手动切换夜间照明，根据自定义计划进行设置，或者根据太阳周期进行设置。