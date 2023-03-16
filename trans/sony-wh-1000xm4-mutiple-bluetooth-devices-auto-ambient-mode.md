# 新的索尼 WH-1000XM4 耳机功能得到详细泄漏

> 原文：<https://www.xda-developers.com/sony-wh-1000xm4-mutiple-bluetooth-devices-auto-ambient-mode/>

在具有主动降噪功能的无线蓝牙耳机的汪洋大海中，有一款产品脱颖而出:索尼 WH-1000XM3。人们真的很喜欢这些耳机(许多 XDA 员工都有)，这意味着人们真的很想知道索尼将如何跟进它们。关于索尼 WH-1000XM4 耳机的信息已经开始出现，今天，APK 的拆解揭示了更多的功能。

首先，回到 3 月份，XDA 的米沙·拉赫曼分享了一些索尼 WH-1000XM4 的现场照片。WH-1000XM4 耳机的设计并不令人兴奋，因为它与索尼 WH-1000XM3 基本相同。这款耳机获得了巴西 Anatel 的认证，该机构相当于美国的 FCC。米莎尔还分享了两页设备手册。

快进到今天，我们有更多关于索尼 WH-1000XM4 的好东西要分享。推特用户@ [justplayinghard](https://twitter.com/justplayinghard/status/1263457145619714050) 发布了他在拆卸索尼耳机 Connect APK 时的一些发现。我们也做了自己的拆卸来证实这些细节。首先，将有三种颜色:黑色，银色和白色。黑色和银色可以在下面看到，但我们没有包括白色模型的渲染，因为 APK 中的图像是一个占位符。

**DSEE 极限**

接下来是 DSEE 极限。基于字符串，它听起来像 DSEE 极端是 DSEE HX 与一些未指明的人工智能增强。DSEE HX 是索尼耳机(包括 WH-1000XM3)的现有功能，可将声源升级到更高的质量。索尼上个月为 DSEE 极限版[申请了商标](https://uspto.report/TM/88896137)，并与 Xperia 1 II 一起推出了[【DSEE 极限版】。很可能这两个术语指的是同一项技术，但我们还得等等看。](https://www.xda-developers.com/sony-xperia-1-ii-xperia-10-ii-xperia-pro-announcement/)

```
 <string name="DSEEHX_AI_Param_Auto">Auto</string>
<string name="DSEEHX_AI_Param_Off">Off</string>
<string name="DSEEHX_AI_Title">DSEE Extreme</string>
<string name="DSEE_HX_AI_ON">DSEE Extreme On</string> 
```

**多点连接**

下一个特性是人们会真正喜欢的。索尼 WH-1000XM4 可能能够同时连接多个设备，以便在它们之间快速切换，尽管这似乎仅限于最多两个设备。索尼 WH-1000XM3 可以存储多个蓝牙配对，但你必须从一个连接到另一个。这意味着 WH-1000XM4 耳机在配对设备之间的切换速度可能比 WH-1000XM3 快得多。根据字符串，听起来好像您要将音频输出从一个设备交换到另一个设备，只需播放当前不活跃但已配对和连接的设备上的媒体。此功能的一个缺点是，当多点启用时，高质量的 LDAC 蓝牙音频编解码器无法使用。

### 多点字符串

```
 <string name="Msg_MultiPoint_CancelPairingMode">Cancels connection to the new device.</string>
<string name="Msg_MultiPoint_CannotEnterPairingMode_History_Description">To connect to the selected device, try again after disconnecting one of the connected devices.</string>
<string name="Msg_MultiPoint_CannotEnterPairngMode_Description">To connect a new device, try again after disconnecting one of the connected devices.</string>
<string name="Msg_MultiPoint_CannotEnterPairngMode_Title">Disconnection of the currently connected device required</string>
<string name="Msg_MultiPoint_ConfirmToDisconnect">Disconnect %s?</string>
<string name="Msg_MultiPoint_ConfirmToDisconnectDescription">"Disconnect %s? If disconnected, connection with this app will be disconnected."</string>
<string name="Msg_MultiPoint_Confirm_Reconnection_Title">Reconnection is necessary</string>
<string name="Msg_MultiPoint_Confirm_Reconnection_TurnOff">The currently playing music will stop since reconnection to the headphones is necessary. Reconnect to headphones?</string>
<string name="Msg_MultiPoint_Confirm_Reconnection_TurnOn">The currently playing music will stop since reconnection to the headphones is necessary. LDAC cannot be used when this setting is enabled. Reconnect to headphones?</string>
<string name="Msg_MultiPoint_DeviceRemoveConfirmation">"Cancel registration of %1$s? To connect to %1$s again after canceling the registration, cancel the registration of %2$s from %1$s, and perform device registration again."</string>
<string name="Msg_MultiPoint_Disconnect_Device_FWUpdate">To update the software, %s connected to the headphones must be disconnected. Disconnect and start update?</string>
<string name="Msg_MultiPoint_Disconnect_Device_Update_Title">Required to disconnect the connected %s</string>
<string name="Msg_MultiPoint_Disconnect_Device_VoiceGuidance">To change the language, %s connected to the headphones must be disconnected. Disconnect and change the language?</string>
<string name="Msg_MultiPoint_FailedToConnect">Connection with %s failed.</string>
<string name="Msg_MultiPoint_FailedToDisconnect">Disconnection with %s failed.</string>
<string name="Msg_MultiPoint_FailedToPair">Connection with a new device failed.</string>
<string name="Msg_MultiPoint_FailedToRemove">Canceling of %s registration failed.</string>
<string name="Msg_MultiPoint_Info_Detail">By enabling this setting, the headphone will be able to connect to two devices simultaneously. Connected devices can be checked from [%s]. LDAC cannot be used when this setting is enabled.</string>
<string name="Msg_MultiPoint_Interrupt_FWUpdate_AddDevice">To connect new devices, the software update must be aborted. Software update can be resumed even if it is aborted. Connect?</string>
<string name="Msg_MultiPoint_Interrupt_FWUpdate_AddDevice_Title">Required to abort software update</string>
<string name="Msg_MultiPoint_Interrupt_FWUpdate_DeviceHistory">To connect with %s, the software update must be aborted. Software update can be resumed even if it is aborted. Connect?</string>
<string name="Msg_MultiPoint_SucceedToPairing">Connection to %s complete.</string>

<string name="MultiPoint_Talkback_Device_Disconnected">No device is connected.</string>
<string name="MultiPoint_Talkback_Playing_Right">Audio is played back.</string>
<string name="MultiPoint_Talkback_Status_Connect">Connected.</string>
<string name="MultiPoint_Talkback_Status_Connecting">Connecting...</string>
<string name="MultiPoint_Talkback_Status_Quitting">Disconnecting...</string>
<string name="MultiPoint_Title">Connect to 2 devices simultaneously</string>
<string name="MultiPoint_TitleNum_1">1.</string>
<string name="MultiPoint_TitleNum_2">2.</string>

<string name="MultiPoint_AddNewDevice_Description">Open Bluetooth settings with the device you want to connect and select %s.</string>
<string name="MultiPoint_DeviceNotConnect">Not connected.</string>
<string name="MultiPoint_DeviceStatus_Title">Device Currently Being Connected</string>
<string name="MultiPoint_Device_Add">Connect to New Device</string>
<string name="MultiPoint_Header_History">Paired</string>
<string name="MultiPoint_Header_Pairing">Connecting...</string>
<string name="MultiPoint_Menu_Delete">Cancel Registration</string>
<string name="MultiPoint_Menu_Disconnect">Disconnect</string>
<string name="MultiPoint_Setting_Description">"This headphone can be simultaneously connected to %d devices. To switch between music players, perform the play operation from the other device."</string>
<string name="MultiPoint_Setting_Title">Manage Connected Device</string>
<string name="MultiPoint_Status_Connecting">Connecting...</string>
<string name="MultiPoint_Status_Disconnecting">Disconnecting...</string>
<string name="MultiPoint_Talkback_Add_Device">Connects to a new device.</string> 
```

**智能通话/语音聊天**

最后一个特性可能是最有趣和最有用的。“智能通话”可以允许索尼 WH-1000XM4 在检测到语音时自动启用环境声音。因此，如果你试图与人交谈，耳机会自动允许环境噪音通过，这样你就可以沟通。在用户定义的时间(快、中、慢或无)后，噪声消除将恢复。用户还可以在自动(基于环境声音)、高或低之间调整语音检测灵敏度，以防用户发现它激活得太频繁(例如当说话的人在附近时)或太少(例如当你在车上时)。您可以在应用程序内或耳机上的 NC/Ambient 按钮(可能)切换此设置。

### 智能发声琴弦

```
 <string name="SmartTalkingMode_Setting_ModeOutTime_Detail">"If the headphones do not detect your voice for the specified amount of time, Speak-to-Chat mode closes and returns to the normal state. Also, the mode can be closed at any time by operating the headphones."</string>
<string name="SmartTalkingMode_Setting_ModeOutTime_Option1">Fast</string>
<string name="SmartTalkingMode_Setting_ModeOutTime_Option2">Standard</string>
<string name="SmartTalkingMode_Setting_ModeOutTime_Option3">Slow</string>
<string name="SmartTalkingMode_Setting_ModeOutTime_Option4">Does not close automatically</string>
<string name="SmartTalkingMode_Setting_ModeOutTime_Option4_short">Do not</string>
<string name="SmartTalkingMode_Setting_ModeOutTime_Title">Time until the mode closes</string>
<string name="SmartTalkingMode_Setting_ModeOutTime_minute">Approx. 1 m</string>
<string name="SmartTalkingMode_Setting_ModeOutTime_second">Approx. 1 s</string>
<string name="SmartTalkingMode_Setting_ModeOutTime_seconds">Approx %d s</string>
<string name="SmartTalkingMode_Setting_ModesOutTime_minute">Aprox %d m</string>
<string name="SmartTalkingMode_Setting_Sensitivity_Auto">Automatic</string>
<string name="SmartTalkingMode_Setting_Sensitivity_Auto_Detail">Automatically adjusts the sensitivity based on the ambient sound.</string>
<string name="SmartTalkingMode_Setting_Sensitivity_Auto_iOS">Automatic:</string>
<string name="SmartTalkingMode_Setting_Sensitivity_High">H Sensitivity</string>
<string name="SmartTalkingMode_Setting_Sensitivity_High_Detail">Select this setting when voice detection sensitivity is too low. Effective when the ambient sound is loud such as while you are in a vehicle.</string>
<string name="SmartTalkingMode_Setting_Sensitivity_High_iOS">H Sensitivity:</string>
<string name="SmartTalkingMode_Setting_Sensitivity_Low">L Sensitivity</string>
<string name="SmartTalkingMode_Setting_Sensitivity_Low_Detail">Select this setting when voice detection sensitivity is too high. Effective when the speaker is close by.</string>
<string name="SmartTalkingMode_Setting_Sensitivity_Low_iOS">L Sensitivity:</string>
<string name="SmartTalkingMode_Setting_Sensitivity_Title">Voice Detect Sensitivity</string>
<string name="SmartTalkingMode_Setting_Title">Speak-to-Chat Setting</string>

<string name="SmartTalkingMode_Title_EnableFirstTime">Enabled Speak-to-Chat</string>
<string name="SmartTalkingMode_TurnOn">Enables Speak-to-Chat to perform settings.</string>
<string name="SmartTalkingMode_TurnOn_Title">Enables Speak-to-Chat</string>
<string name="SmartTalkingMode_TurnOn_conf">"This setting can be switched through operations on your headphones. The operation method can be checked in [Help]."</string>
<string name="SmartTalkingMode_TurnOn_conf_Title">Enable Speak-to-Chat?</string> 
```