# 从出厂的 Rom 中轻松提取 Android Rom 文件

> 原文：<https://www.xda-developers.com/easily-extract-android-rom-files-from-shipped-roms/>

如果你是一个 Android 开发人员，正在研究最新发布的 rom 来提取 apk、驱动程序等等，你可能知道从。exe 包有点棘手。特别是，因为如果你正在使用任何一个 Linux 发行版，在系统崩溃之前，你只有很短的时间去寻找需要的文件。为了解决这个问题，XDA 成员 [MartinEve](http://forum.xda-developers.com/member.php?u=2799448) 做了一个小脚本，可以自动从安装程序中提取 rom.zip 文件。

尝试应用程序，并向开发人员报告一些反馈。

> 今天，我第一次尝试从一个已发布的 rom 版本中提取一个 rom.zip 文件。exe)。
> 
> 这个过程是有问题的，因为在使用 wine 启动可执行文件后，应用程序崩溃，删除了所有文件。因此，你必须非常快速地查看~/。rom.zip 的 wine/users/username/Temp 文件夹
> 
> 无论如何，我已经完成了一个快速的 python 脚本，它将监视这个目录中的 rom.zip 并将其复制到您的主文件夹中。
> 
> 在运行之前，您需要做的唯一修改是将用户名字段更改为您自己的用户名。我本来会使用 getpass 来获得这个，但是由于某种原因，在某些系统上，您需要使用 sudo，这会把它弄乱。

您可以在[应用程序线程](http://forum.xda-developers.com/showthread.php?t=760991)中找到更多信息。