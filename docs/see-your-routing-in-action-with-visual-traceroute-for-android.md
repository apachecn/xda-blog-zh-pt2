# 使用面向 Android 的可视化 Traceroute 查看您的实际路由

> 原文：<https://www.xda-developers.com/see-your-routing-in-action-with-visual-traceroute-for-android/>

有没有想过在旅途中运行跟踪路由？如果是这样的话，你肯定已经注意到“绿色小机器人”上可供你选择的选项非常有限。为了补救这一点，XDA 论坛成员 RyanZA 创建了一个可视化的 traceroute 应用程序。

通过使用 *ping* 命令，Visual Traceroute 确定您的数据到相关服务器的路径，并直观地映射它。如果您的设备碰巧是根设备，这个应用程序将使用 *nmap* 命令。使用 *nmap* 解决了一些路由器阻塞 *ping* 的问题。用开发商的话说:

> Visual Traceroute 将在地图上向您显示您的数据传输到世界上任何服务器的路径。非常容易使用，只需输入服务器的名称，然后按 go。
> 
> Visual Traceroute 将使用大多数设备上可用的“ping”命令来确定数据传输的路径，然后使用数据库来查找该路径的地理位置。如果您的设备是根设备，Visual Traceroute 将使用“nmap”而不是“ping ”,这样可以更好、更快地(基于 UDP)检测主机。
> 
> 有些路由器会阻止“ping”(ICMP)，这种情况下你需要一个根设备。有些设备上没有安装“ping ”,在这种情况下，您也需要一个根设备。这种情况下应用会通知你。

继续进入[应用线程](http://forum.xda-developers.com/showthread.php?t=1196681)以获得更多移动黑客技术。