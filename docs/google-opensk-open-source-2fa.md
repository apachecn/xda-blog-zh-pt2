# Google 发布 OpenSK，一个开源的 2FA 安全密钥平台

> 原文：<https://www.xda-developers.com/google-opensk-open-source-2fa/>

虽然谷歌已经为移动安全做了很多，但该公司鲜为人知的事实是，他们喜欢涉足安全密钥。 [Titan 系列安全密钥](https://www.xda-developers.com/google-titan-security-key-usb-c/)与您的 Android 或 iOS 智能手机完全集成，可用于验证您的谷歌账户登录。谷歌现在已经推出了 OpenSK，这是一个开源项目，允许开发者创建和构建自己的 2FA 安全密钥。

用 Rust 编写的 OpenSK 很简单，因为它支持 FIDO U2F 和 [FIDO2](https://www.xda-developers.com/android-fido2-certified-passwordless-access/) 标准。它沿袭了其他开源项目的传统，如 Solo 和 Somu，这是另一组开源安全密钥平台。谷歌希望开发者和安全密钥制造商都能从中受益。

#### 通过开放 OpenSK 作为一个研究平台，我们希望它将被研究人员、安全密钥制造商和爱好者用来帮助开发创新功能和加速安全密钥的采用。

有了这个早期版本，开发人员将能够在 Nordic 芯片加密狗上闪存 OpenSK。Nordic 芯片加密狗支持 FIDO2 的所有主要功能，如 NFC、蓝牙低能耗、USB 和专用硬件加密内核。

*“我们很高兴能与谷歌和开源社区合作开发新的 OpenSK 研究平台，”*Nordic Semiconductor 产品管理总监 Kjetil Holstad 表示。*“我们希望我们业界领先的 nRF52840 对安全加密加速的本机支持与 OpenSK 中的新功能和测试相结合，将有助于行业获得安全密钥的主流采用。”*

OpenSK 是用 Rust 编写的，运行在 TockOS 上，以获得更好的隔离和更清晰的操作系统抽象。Rust 具有强大的内存安全性，可以帮助防止逻辑攻击，而 TockOS 提供了沙盒架构，可以更好地隔离安全密钥小程序、驱动程序和内核。如果你感兴趣，一定要看看下面的链接。

* * *

**来源:[Google](https://security.googleblog.com/2020/01/say-hello-to-opensk-fully-open-source.html)|****Via:[AndroidPolice](https://www.androidpolice.com/2020/01/30/google-releases-open-source-2fa-security-key-platform/)**