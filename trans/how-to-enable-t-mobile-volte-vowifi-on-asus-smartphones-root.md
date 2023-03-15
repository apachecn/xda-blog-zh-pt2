# 如何在华硕智能手机上启用 T-Mobile VoLTE/VO wifi[Root]

> 原文：<https://www.xda-developers.com/how-to-enable-t-mobile-volte-vowifi-on-asus-smartphones-root/>

从传统电路交换语音网络过渡到 IP 多媒体子系统(IMS)让我们有机会使用高级蜂窝服务，如 LTE 语音(VoLTE)、Wi-Fi 呼叫(VoWiFi)和[丰富通信服务](https://www.xda-developers.com/tag/rcs/) (RCS)。现在 [5G 支持已经准备好登陆预算段](https://www.xda-developers.com/qualcomm-5g-budget-smartphones-snapdragon-4-series-chips/)，几家运营商正在逐步淘汰老式的 2G/3G 基础设施，甚至要求所有连接到 4G LTE 和 5G 网络的设备都使用 VoLTE。例如，T-Mobile 和 AT&T,[将在不久的将来为不支持 VoLTE 的手机屏蔽](https://www.xda-developers.com/t-mobile-att-require-volte-phone-calls-shut-down-3g/)语音和数据服务。

房间里的大象来了:运营商解锁模式的普通消费者如何确保他们的智能手机与服务提供商的 VoLTE(和 VoWiFi)兼容？当我们在谈论像华硕这样的 OEM 厂商时，整个情况真的很复杂。如果你想买任何一部当代华硕 ROG 手机或华硕 ZenFone 品牌的智能手机——包括最近推出的 [ROG 手机 3](https://www.xda-developers.com/asus-rog-phone-3-review/) 和[Zen fone 7/7 Pro](https://www.xda-developers.com/asus-zenfone-7-pro-specs-features-pricing-availability/)——作为你的下一部手机，你会惊讶地发现，上述美国运营商都没有正式支持 VoLTE。好消息是，XDA 的汽车后市场开发社区再次出手相救。

**t1【ASUS rog phone 3 论坛】| |[ASUS zenfone 7 论坛](https://forum.xda-developers.com/asus-zenfone-7)| |[ASUS zenfone 7 pro 论坛](https://forum.xda-developers.com/asus-zenfone-7-pro)**

这一次，XDA 认可的开发商 [HomerSp](https://forum.xda-developers.com/member.php?u=2266182) 找到了一种方法，可以摆弄高通骁龙调制解调器的内部诊断接口，并设置正确的参数，以便目标华硕智能手机可以无缝支持高级 IMS 服务，如 T-Mobile 网络上的 VoLTE。虽然开发者在[华硕 ROG 手机 II](https://www.xda-developers.com/tag/asus-rog-phone-ii/) 上成功测试了该方法，但我们论坛上的用户也在他们的 [ZenFone 6](https://www.xda-developers.com/tag/asus-zenfone6/) 上成功测试了该方法。根据 XDA 公认的开发者 [Captain_Throwback](https://forum.xda-developers.com/member.php?u=1162986) 和 XDA 资深成员 [bs3pro](https://forum.xda-developers.com/asus-rog-phone-3/how-to/ive-asus-rog-phone-3-1-month-t4137097/post83431427#post83431427) 的说法，修改 ROG Phone 3 上的那些参数(也就是厂商 prop 值)就足以让 VoLTE 和 VoWiFi 在 T-Mobile 上工作，这意味着 mod 也与最新的华硕手机兼容！

**t1【ASUS zenfone 6 论坛】| |[ASUS rog phone ii 论坛](https://forum.xda-developers.com/rog-phone-2)**

* * *

## 如何在华硕智能手机上启用 T-Mobile VoLTE/VoWiFi

### 步骤 1–启用隐藏高通诊断模式

1.  确保您拥有 root 访问权限。
2.  下载高通产品支持工具(QPST)的最新版本，高通 USB 驱动程序，以及由 [HomerSp](https://forum.xda-developers.com/member.php?u=2266182) 开发的 [AsusVoLTE](https://github.com/HomerSp/AsusVoLTE) 应用程序。
3.  使用 AsusVoLTE 应用程序或 QPST 的远程连接功能来触发高通诊断模式。进一步的细节，看一看[这个线程](https://forum.xda-developers.com/rog-phone-2/how-to/guide-enabling-diag-qpst-t4027493)。

### 步骤 2 -设置适当值

1.  通过股票拨号器 app 拨打`*#*#3642623344#*#*`。
    *   这个秘密代码可以用来从手机上强制启用 VoLTE/VoWiFi，但它无法在重启后存活。
2.  或者，从提升的 shell 中执行下面的命令:

    ```
     setprop persist.vendor.dbg.ims_volte_enable 1
    setprop persist.vendor.dbg.volte_avail_ovr 1
    setprop persist.vendor.dbg.vt_avail_ovr 1
    setprop persist.vendor.dbg.wfc_avail_ovr 1 
    ```

3.  您也可以使用 AsusVoLTE 应用程序来设置这些值。

如果一切正常，在关闭然后再次打开移动数据后，此时您应该能够在状态栏中看到 VoLTE(或 VoWiFi)图标。

### (可选)步骤 3 -修改 EFS 分区

您可能需要将运营商配置推送到目标 ASUS 设备的 EFS 分区，以获得更好的兼容性。为此，请按照下面链接的主题中提到的步骤进行操作。

**[在华硕智能手机上启用 VoLTE/VO wifi—XDA 线程](https://forum.xda-developers.com/rog-phone-2/how-to/guide-enabling-volte-vowifi-v2-t4028073)**

* * *

值得一提的是，与 T-Mobile 不同，[为 VoLTE(又名“高清语音”)兼容性维护了一个白名单](https://www.anrdoezrs.net/links/100122946/type/dlg/sid/UUxdaUeUpU29740/https://www.att.com/idpassets/images/support/wireless/Service-Capabilities-Unlocked-Devices-ATT-Network.pdf)。虽然有一些使用本指南在运营商上启用 VoLTE 的成功报告，但您的里程数可能会有所不同。