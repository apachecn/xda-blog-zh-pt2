# 逆向工程小米 OTA 更新寻找未发布的更新

> 原文：<https://www.xda-developers.com/reverse-engineering-xiaomi-ota-updates/>

为了进入[小米](https://www.xda-developers.com/xiaomi)的夜生活——小米 MIUI 操作系统未发布的内部版本——XDA 资深成员 [duraaraa](https://forum.xda-developers.com/member.php?u=4572798) 对这家中国公司的空中下载(OTA)更新框架进行了逆向工程。这两个正在进行的漏洞迫使小米设备推出夜间版本，而不是最新的商业固件，理论上可以安装在现成的设备上，前提是(1) MIUI 的 OTA 应用程序被反向工程，以及(2)测试版本与正式版本使用相同的密钥签名。

## 方法一:精心制作小米 OTA 更新网址

两种方法中较简单的一种涉及访问 OTA 更新 URL，它向客户端设备发送如何下载所述更新的指令。[这个 URL，例如](http://update.miui.com/updates/mi-updateV6.php?v=MIUI-7.9.21&c=7.1&d=chiron_global&b=X)，包含告诉小米的 OTA 更新应用在哪里可以找到 MIUI 9 的 7.9.21 版本，这是一个内部测试版本。

```
 {"UserLevel":9,"LatestVersion":{"type":"rom","device":"chiron_global","name":"XM-MIMIX2-GLOBAL 7.9.21","description":"MIUI\u5347\u7ea7","descriptionUrl":"http:\/\/update.miui.com\/updates\/updateinfo\/7.9.21\/chiron_global_0_7.9.21_4494ccfcc506caca9904efb74b489e0a.html","md5":"7f94ca393fae77c6171e6c7a551bea2e","filename":"miui_MIMIX2Global_7.9.21_7f94ca393f_7.1.zip","filesize":"1.6G","codebase":"7.1","version":"7.9.21","branch":"X"},"UpdateList":[{"type":"rom","device":"chiron_global","name":"XM-MIMIX2-GLOBAL 7.9.21","description":"","descriptionUrl":"http:\/\/update.miui.com\/updates\/updateinfo\/7.9.21\/chiron_global_0_7.9.21_4494ccfcc506caca9904efb74b489e0a.html","md5":"7f94ca393fae77c6171e6c7a551bea2e","filename":"miui_MIMIX2Global_7.9.21_7f94ca393f_7.1.zip","filesize":"1.6G","codebase":"7.1","version":"7.9.21","branch":"X"}],"IncrementalUpdateList":[],"MirrorList":["http:\/\/bigota.d.miui.com"],"Signup":{"version":"","total":"","rank":""},"AuthResult":0,"ForceUpdate":0 
```

当一个稳定的版本最近开始在中国推出时-8 . 5 . 7 . 0 . ndecnef-[dura ara](https://forum.xda-developers.com/member.php?u=4572798)利用这个漏洞找到了固件的升级 URL。

## 方法 2:制作小米 OTA 更新请求

第二种方法稍微复杂一点，包括获取小米更新服务器的解密密钥。这需要反编译更新应用程序，并使用 Xposed 来捕获和分析网络流量。

当解密密钥(例如“miuiotavalided11”)存在时，理论上，任何用户都可以生成一个伪造的升级请求。

## 迫使小米 OTA 升级

duraaraa 使用这两种方法在小米的服务器上找到了未发布的 MIUI 版本，但还没有成功下载并在小米设备上安装。他要求开发社区的成员参与到这项工作中来。

要跟踪新的发展和/或自愿提供您的专业知识，请查看 XDA 论坛的帖子。

* * *

[**小米 OTAs**](https://forum.xda-developers.com/mi-mix-2/how-to/guide-reverse-engineering-xiaomi-ota-t3691612) 逆向工程探讨