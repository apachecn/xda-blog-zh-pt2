# 谷歌收集位置数据，即使定位服务被禁用

> 原文：<https://www.xda-developers.com/google-collecting-location-data/>

默认情况下，大多数安卓设备(只要它们有谷歌服务)都会追踪主人的位置。这些位置用于广告目的，但也为所有者提供有用的服务，如运动跟踪、健身统计、未来通勤建议等。那些更关心隐私的人可能会选择关闭定位服务，这是 Android 内部提供的，似乎没有任何附加条件。不想你的位置数据被挖掘？禁用定位服务。

或者这就是他们希望你相信的。

[关于 *Quartz*](https://qz.com/1131515/google-collects-android-users-locations-even-when-location-services-are-disabled/) 的一份报告显示，这种乐观的观点实际上并非如此，即使禁用位置服务，谷歌仍然会向你提供位置数据。自 2017 年以来，谷歌一直在接收每台使用谷歌 Firebase 消息推送通知服务的安卓设备的手机信号塔数据。谷歌已经证实了这一做法，但坚称这些数据从未被使用或存储。

“今年一月，我们开始研究使用手机识别码作为额外的信号，以进一步提高信息传递的速度和性能”谷歌发言人在被联系时告诉 *Quartz* 。*然而，我们从未将 Cell ID 整合到我们的网络同步系统中，因此数据立即被丢弃，我们将其更新为不再请求 Cell ID* 。目前还不清楚这将如何实际帮助消息传递时间或改进 Firebase 云消息传递的当前迭代。

 <picture>![google quartz firebase cloud messaging FCM location data privacy concern](img/bdd19596af1e438ad1a35746d247b946.png)</picture> 

Location data sent to Google // Source: Quartz

当然，可以说这些数据不是非常准确，不会帮助谷歌获得任何形式的个人准确位置数据，但这一增加仍然有两个问题。第一点非常明显，那就是当定位服务关闭时，它们实际上应该是关闭的。

第二，虽然手机信号塔的信息不会像 GPS 那样精确，但它仍然可以将位置信息与附近的其他手机信号塔结合起来，计算出设备用户周围四分之一英里内的位置。数据是加密的，但仍有可能被设备上的恶意软件截获。此外，即使没有 SIM 卡的用户也不安全，位置数据是通过使用附近的手机信号塔计算位置来发送的。

谷歌还表示，这“与定位服务截然不同，定位服务向应用程序提供设备的位置”这就是为什么，显然，这是没问题的。如果不从你的设备上移除所有的谷歌服务，你就无法选择退出。这个“问题”可能会影响所有使用谷歌服务的设备，平板电脑和手机都向谷歌发送相同的数据。如果谷歌不再使用这些数据，这种侵犯隐私的行为有望被消除，但目前避免这种情况的唯一方法是从你的设备上删除谷歌服务。

* * *

[**来源:石英**](https://qz.com/1131515/google-collects-android-users-locations-even-when-location-services-are-disabled/)