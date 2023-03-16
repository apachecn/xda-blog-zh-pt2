# 如何从 Android 智能手机或平板电脑上运行《我的世界》服务器

> 原文：<https://www.xda-developers.com/run-minecraft-server-android/>

# 以下是如何在你的安卓手机上运行《我的世界》服务器，为什么不呢

你曾经想从你的 Android 智能手机或平板电脑上运行《我的世界》服务器吗？没有吗？如果你真的想的话，现在你可以了。

游戏中

你曾经想从你的手机上运行《我的世界》服务器吗？没有吗？现在你可以了。多亏了 Reddit 用户 endmymisouri 的一组指令，你可以使用一个无根的 Android 设备来托管《我的世界》服务器。说真的，这是一个利用你身边旧的安卓手机或平板电脑的好方法。当然，你的 Android 设备作为服务器不会特别强大，但它会工作。我在运行 One UI 2.0 的三星 Galaxy Note9 上设置了一个《我的世界》服务器，并能够从我的电脑上顺利加入。

如果你感兴趣，建议你使用至少 4GB 内存的手机或平板电脑。尽管《我的世界》服务器可以在 1GB 的内存上轻松运行，但你需要更多的内存，这样 Android 本身才不会崩溃。你还应该有一个相当强大的处理器，因为《我的世界》确实需要做一些计算工作。如果这些对你来说听起来不错，继续读下去，因为是时候看说明书了。

## 建立《我的世界》

1.  你需要做的第一件事是下载 Termux 和 AnLinux，它们都可以从 Play Store 获得。
2.  打开 AnLinux，从左侧轻扫以打开导航抽屉，然后点按“仪表板”
3.  点击“选择”按钮并选择 Ubuntu。
4.  点击“复制”按钮，然后点击“启动”按钮。Termux 现在应该打开了。
5.  如果需要，让 Termux 自己设置。按住“终端”窗口的任意位置一秒钟，然后选取“粘贴”按回车键让它运行。
6.  一旦完成，就该启动 Ubuntu 了。输入以下命令:

    ```
     chmod +x start-ubuntu.sh
    ./start-ubuntu.sh 
    ```

7.  如果成功了，您应该会看到类似于`root@localhost:~#`的提示。
8.  现在您需要安装一些依赖项。运行以下命令:

    ```
     apt install software-properties-common
    add-apt-repository ppa:openjdk-r/ppa && apt update
    apt install openjdk-8-jre 
    ```

9.  现在你已经准备好安装《我的世界》了。
10.  运行:

    ```
     cd ~/ 
    ```

    ...以确保您在正确的目录中。
11.  接下来，运行:

    ```
     mkdir mc && cd mc 
    ```

12.  现在运行:

    ```
     wget -O minecraft_server.jar https: 
    ```

    这将下载 1.15.2《我的世界》服务器 JAR。如果你想要另一个版本，你可以在这里[下载 JAR。](https://www.minecraft.net/en-us/download/server/)
13.  下载完 JAR 后，执行以下命令:

    ```
     chmod +x minecraft_server.jar 
    ```

14.  然后:

    ```
     echo eula=true > eula.txt 
    ```

15.  最后，运行:

    ```
     java -Xmx1024M -Xms1024M -jar minecraft-server.jar nogui 
    ```

    这将运行内存为 1GB (1024MB)的《我的世界》服务器。如果您想给它更多或更少的内存，可以在-Xmx 参数中更改“1024M”这个数字。
16.  让它启动。

如果一切顺利，你现在将有一个香草《我的世界》服务器运行在你的 Android 设备上！

如需更高级的说明，如 SSH 访问、Forge 安装和将您的服务器公之于众，一定要访问[原始的 Reddit 线程](https://www.reddit.com/r/Android/comments/glr4gc/hosting_a_minecraft_server_on_android_20/)。