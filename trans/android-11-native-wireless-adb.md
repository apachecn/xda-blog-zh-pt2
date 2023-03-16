# Android 11 可能最终会带来一个合适的原生无线 ADB 实现

> 原文：<https://www.xda-developers.com/android-11-native-wireless-adb/>

对于 Android 应用开发者来说，ADB 是调试应用不可或缺的工具。ADB 具有生成日志、推/拉文件、侧装 apk 和进入 shell 的能力，使开发人员在使用 PC 时能够对测试设备进行大量控制。虽然可以通过 TCP/IP*连接到您的设备来无线使用 ADB，但许多开发人员可能不知道这一点，因此他们只是坚持使用有线连接。此外，如果您的设备没有静态 IP 地址，或者您要处理多个测试设备，无线 ADB 目前并不方便。最后，通过 ADB 在 TCP/IP 上进行的数据传输是以纯文本的形式进行的，所以在连接到不可信的网络时使用它并不是一个好主意。令人欣慰的是，看起来谷歌正在努力实现一个合适的、本地的(可能)安全的无线 ADB，它可能会在明年的 Android 11 中登陆。

Google 的软件工程师 Joshua Duong 向 AOSP Gerrit 提交了多个实现该功能的提交。这些承诺[为亚洲开发银行](https://android-review.googlesource.com/c/platform/system/core/+/1148015)创建一个 WiFi 服务，同时[支持安全配对](https://android-review.googlesource.com/c/platform/system/core/+/1148676)。我们还没有发现新实现对传输中的数据进行加密的证据，但这一功能显然仍在开发中，因此可能会在以后的提交中实现。在用户端，谷歌计划在开发者选项中添加一个新的“无线调试”开关，支持通过扫描二维码或输入 6 位数字代码来配对设备。

### Android 11 的无线 ADB 字符串

```
 <string name="enable_adb_wireless">Wireless debugging</string>
<string name="enable_adb_wireless_summary">Debug mode when Wi\u2011Fi is connected</string>
<string name="adb_wireless_error">Error</string>
<string name="adb_wireless_settings">Wireless debugging</string>
<string name="adb_wireless_list_empty_off">To see and use available devices, turn on wireless debugging</string>
<string name="adb_pair_method_qrcode_title">Pair device with QR code</string>
<string name="adb_pair_method_qrcode_summary">Pair new devices using QR code Scanner</string>
<string name="adb_pair_method_code_title">Pair device with pairing code</string>
<string name="adb_pair_method_code_summary">Pair new devices using six digit code</string>
<string name="adb_paired_devices_title">Paired devices</string>
<string name="adb_wireless_device_connected_summary">Currently connected</string>
<string name="adb_wireless_device_details_title">Device details</string>
<string name="adb_device_connect">Connect</string>
<string name="adb_device_disconnect">Disconnect</string>
<string name="adb_device_forget">Forget</string>
<string name="adb_device_mac_addr_title_format">Device MAC address: %s</string>
<string name="adb_wireless_connection_failed_title">Connection unsuccessful</string>
<string name="adb_wireless_connection_failed_message">Make sure %s is connected to the correct network</string>
<string name="pairing_progress_category_title">Waiting for pairing requests..</string>
<string name="adb_pair_new_devices_title">Pair new devices</string>
<string name="adb_no_pairing_devices_found">No devices were found for pairing.</string>
<string name="adb_pairing_device_dialog_title">Pair with device?</string>
<string name="adb_pairing_device_dialog_pairing_code_label">Wi\u2011Fi pairing code</string>
<string name="adb_pairing_device_dialog_failed_title">Pairing unsuccessful</string>
<string name="adb_pairing_device_dialog_failed_msg">Make sure the device is connected to the same network.</string>
<string name="adb_wireless_verifying_qrcode_text">Checking QR code...</string>
<string name="adb_qrcode_pairing_device_failed_msg">Failed to pair the device. Either the QR code was incorrect, or the device is not connected to the same network.</string>
<string name="adb_discovery_enable_failed_title">Discovery unsuccessful</string>
<string name="adb_discovery_failed_msg">Failed to enable ADB wireless discovery. Please make sure you are connected on a Wi\u2011Fi network.</string>
<string name="keywords_adb_wireless">adb, debug, dev</string> 
```

看起来谷歌终于开始开发这项功能了，所以我希望它能在明年的 Android 11 中实现。然而，这些提交还没有合并，所以不能保证这个特性会出现在下一个 Android 版本中。我们将密切关注 AOSP Gerrit，以跟踪它何时被合并，并了解更多关于该实现的信息。

*XDA 知名开发者 phhusson 让我注意到，ADB [支持多播 DNS](https://android.googlesource.com/platform/system/core/+/master/adb/daemon/mdns.cpp) ，因此已经可以无线连接到 ADB，而不需要您设备的 IP 地址。然而，启动服务需要 root 用户，并且一次只能连接一个设备，因此这不是一个理想的解决方案。另外，它没有在任何地方公开记录，所以很少有人知道它。

* * *

*感谢 XDA 知名开发者 [luca020400](https://forum.xda-developers.com/member.php?u=5778309) 的提示，感谢 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 指出 mDNS 在亚行的支持！*