# 以下是 Android 4.4.4 KTU84P 中的所有变化

> 原文：<https://www.xda-developers.com/heres-everything-thats-changed-in-android-4-4-4-ktu84p/>

今天早些时候，我们都对 Android 4.4.4 的[突然发布感到惊讶。自然，这让我们都有点好奇这个最新版本到底加入了什么，根据 Sprint 的更新支持文档，它带来了一个未指明的“安全修复”。现在，](http://www.xda-developers.com/android/android-4-4-4-ktu84p-factory-images-and-driver-binaries-available-for-nexus-devices-source-code-now-live/ "Android 4.4.4 KTU84P Factory Images and Driver Binaries Available for Nexus Devices, Source Code Now Live") [FunkyAndroid](https://funkyandroid.com/) 的优秀人员已经做了他们最擅长的事情，列出了这个新版本的 Android 引入的每一个代码提交。

FunkyAndroid 团队已经给了我们 Android [4.4.1](http://www.xda-developers.com/android/browse-every-new-aosp-code-commit-in-android-4-4-1/) 、 [4.4.2](http://www.xda-developers.com/android/source-code-commits-in-android-4-4-2-kot49h-reveal-flash-sms-attack-fix-and-app-ops-removal/) 、 [4.4.2_r2](http://www.xda-developers.com/android/android-4-4-2_r2-kvt49l-rolling-out-to-the-nexus-7-2013-with-lte-factory-images-updated-and-heres-whats-new/) 和 [4.4.3](http://www.xda-developers.com/android/browse-every-new-aosp-code-commit-in-android-4-4-3/) 的开发者变更日志。现在，他们又给了我们另一个 Android 4.4.4 KTU84P 的开发者变更日志。和往常一样，这项服务之所以成为可能，要感谢前 AOSP 主角 JBQ 发布的开源脚本。

完整的变更列表:

> **项目:** [**平台/构建**](https://android.googlesource.com/platform/build)
> 
> [27aae42](https://android.googlesource.com/platform/build/+/27aae42) : "KTU84P "
> 
> 7f83b7c : MR2.1 -版本 4.4.4。开始了。不要合并
> 
> **项目:** [**平台/cts**](https://android.googlesource.com/platform/cts)
> 
> [b8e2dab](https://android.googlesource.com/platform/cts/+/b8e2dab) :不合并版本突增更新
> 
> [6da2c 75](https://android.googlesource.com/platform/cts/+/6da2c75):OpenSSL 早期 CCS 问题的 CTS 测试(CVE-2014-0224)
> 
> a3b762f :禁用主机端全息测试
> 
> [8e02f46](https://android.googlesource.com/platform/cts/+/8e02f46) : CTS 报告不得显示原始绩效数据。bug:13347703
> 
> [510cfbc](https://android.googlesource.com/platform/cts/+/510cfbc) : media:重构并提高 AdaptivePlaybackTest 的健壮性
> 
> [e502d40](https://android.googlesource.com/platform/cts/+/e502d40) :修复 OpenSSLHeartbleedTest 中的一个并发 bug。
> 
> [3a90060](https://android.googlesource.com/platform/cts/+/3a90060) :硬件:consumerir:增加测试图形长度
> 
> [c070509](https://android.googlesource.com/platform/cts/+/c070509) :硬件:消费者:修正时间差异
> 
> [1856a4e](https://android.googlesource.com/platform/cts/+/1856a4e) :针对 SSLSocket 中心脏出血漏洞的 CTS 测试。
> 
> **项目:** [**平台/外部/chromium_org**](https://android.googlesource.com/platform/external/chromium_org)
> 
> [76d1172](https://android.googlesource.com/platform/external/chromium_org/+/76d1172) :反向移植“在导航时回收旧的 V8 包装对象”
> 
> [afae5d8](https://android.googlesource.com/platform/external/chromium_org/+/afae5d8) :阻塞对注入的 java 对象中 java.lang.Object.getClass 的访问
> 
> **项目:** [**平台/外部/chromium _ org/third _ party/WebKit**](https://android.googlesource.com/platform/external/chromium_org/third_party/WebKit)
> 
> [3fb1c1e](https://android.googlesource.com/platform/external/chromium_org/third_party/WebKit/+/3fb1c1e) :修复多框架页面的 Java Bridge 包装器属性清理
> 
> [b13a6de](https://android.googlesource.com/platform/external/chromium_org/third_party/WebKit/+/b13a6de) :精选“导出 WebCore::健忘 forgetV8ObjectForNPObject”
> 
> **项目:** [**平台/外部/chromium _ org/第三方/openssl**](https://android.googlesource.com/platform/external/chromium_org/third_party/openssl)
> 
> [e2f 305 e](https://android.googlesource.com/platform/external/chromium_org/third_party/openssl/+/e2f305e):cherry pick“OpenSSL:从 1.0.1h 开始添加 CVE 补丁”
> 
> **项目:** [**平台/外部/openssl**](https://android.googlesource.com/platform/external/openssl)
> 
> dd1da36 :修复早期 CCS bug
> 
> **项目:** [**平台/框架/基地**](https://android.googlesource.com/platform/frameworks/base)
> 
> [63ade05](https://android.googlesource.com/platform/frameworks/base/+/63ade05) :增加 EventLog 事件，记录调用 java.lang.Object.getClass 的尝试
> 
> **项目:** [**平台/框架/webview**](https://android.googlesource.com/platform/frameworks/webview)
> 
> [7a7dce8](https://android.googlesource.com/platform/frameworks/webview/+/7a7dce8) :处理 intent: scheme 时整理选择器 Intent。

正如 Sprint 的更新支持文档所指出的，这确实是一个安全更新。查看对 4.4.4 的提交，我们现在可以看到这种情况。我们还可以看到，本次更新修补的漏洞并不是在 [geohot 的 tower root](http://www.xda-developers.com/android/breaking-geohot-roots-the-verizon-galaxy-s5-with-towelroot/)中利用的 Linux 内核 CVE-2014-3153 漏洞，而是一个 OpenSSL 早期 CCS 问题(CVE-2014-0224)，该问题可能导致某些类型的中间人攻击。除了安全修复之外，webview 和 chromium 以及事件日志也做了一些小的改动。

除了 AOSP 代码提交之外，可能还会有某些特定于设备的修复，这些修复来自于同时发布的专有驱动程序 blobs。然而，目前还不知道什么，包括可怕的 mm-qcamera-daemon 问题是否仍然存在。

*【来源: [FunkyAndroid](https://funkyandroid.com/aosp-KTU84M-KTU84P.html) |感谢公认的贡献者 [galaxyfreak](http://forum.xda-developers.com/member.php?u=4635923) 的提示！]*