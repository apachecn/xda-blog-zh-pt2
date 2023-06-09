# Android P 还将防止闲置的后台应用程序通过麦克风记录你

> 原文：<https://www.xda-developers.com/android-p-audio-recording-limitations-privacy/>

Android 的下一个主要版本 Android P 可能还有几周的时间，但每一天都会带来新的线索。Android P 的重点之一似乎是保护用户隐私。昨天，我们写了 Android P 将如何对请求访问相机的[“空闲”后台应用施加限制。接下来，我们还发现了一个 Android 开源项目(AOSP)](https://www.xda-developers.com/android-p-background-apps-camera/) [commit](https://android-review.googlesource.com/c/platform/system/sepolicy/+/577303) 在同一天合并，**阻止空闲的后台应用程序访问麦克风**。

我们可以想象这个消息可能会让你们中的一些人感到震惊。是的，从技术上来说，你允许访问你设备麦克风的任何应用程序都可以在后台运行，并记录你说的任何话，尽管 Android Oreo 在后台服务上的限制可能间接使这变得有点难以逃脱。尽管如此，一个在后台闲置的应用程序可能会偷偷记录你的想法是一个直接来自*黑镜*的可怕前提——这就是为什么谷歌正在努力解决这个问题。

## Android P 有什么变化？

它是这样工作的:当一个应用程序由它的 UID(Android 系统在安装时分配的唯一、不变的标识符)标识时，它进入**空闲**状态，Android 的音频系统将不允许它录制音频。(这里的“空闲”是指[后台应用对 CPU 和网络密集型服务](https://www.xda-developers.com/how-android-n-will-improve-battery-and-memory-management/)的访问受到限制时的空闲[瞌睡](https://www.xda-developers.com/xda-external-link/check-for-doze-support-on-your-device/)状态。)它将报告空数据(字节数组中的一串零)，而不是将数据从麦克风写入文件。一旦应用程序再次激活(即退出瞌睡模式)，它将开始记录真实数据。

这听起来可能有点复杂(没有双关语的意思)，但是目标是保护隐私。记录垃圾音频的闲置应用程序将防止假设的恶意应用程序迅速意识到其访问被切断，从而防止他们偷偷记录环境噪音、私人对话和你的周围环境。

## 为什么重要？

秘密接入你手机麦克风的应用不仅仅是安全研究人员的偏执妄想。去年年底，*《纽约时报》* [报道](https://www.xda-developers.com/android-apps-tracking-mic-always-listening/)超过 1000 个流行的安卓应用通过设备麦克风监听广告跟踪音频信号。

Android 6.0 Marshmallow 引入了一个权限系统，默认情况下阻止应用程序访问麦克风(和其他传感器)。但这是一次性交易:在你授予一个应用程序权限后，没有什么可以阻止它在未来滥用该权限。事实上，撤销权限有点麻烦:你必须进入 Android **设置**菜单，点击**应用**，滚动到应用并选择它，点击**应用权限**，找到相关权限。

运气好的话，Android P 会替你完成这项艰巨的工作。