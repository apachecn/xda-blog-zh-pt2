# 这个家伙在他的小米吸尘器上安装了 Spotify

> 原文：<https://www.xda-developers.com/this-guy-installed-spotify-on-his-xiaomi-vacuum-cleaner/>

# 这个家伙在他的小米吸尘器上安装了 Spotify

埃迪·张(Eddie Zhang)在他们的 Roomba 形状的小米机器人吸尘器上安装了 spotify，以便直接在吸尘器上播放 Spotify。

Spotify 是[付费音乐流媒体](https://www.xda-developers.com/waze-7-new-streaming-services/)最喜欢的目的地之一。Spotify 聪明的推荐引擎吸引并留住了大部分用户，其中一半用户为这项服务付费，尽管它是以免费增值模式运营的。除了音乐推荐系统之外，Spotify 还有无数的功能，使得分享音乐比其他服务更方便。该服务的另一个好处包括跨平台播放和远程控制选项。虽然在 PC 或智能手机上运行 Spotify 很常见，但有一种变通方法可以将其安装在 Raspberry Pi 机器上。所以，有人先行一步，把它安装在他们的小米牌吸尘器上。*因为，为什么不呢！？*

一位名叫埃迪·张(Eddie Zhang)的绅士用 Raspotify 在他们的第一代小米机器人吸尘器上运行 spotify，这款吸尘器类似于 iRobot Roomba。Raspotify 是一个经过修改的开源客户端，用于在 Raspbian(基于 Debian 的 Raspberry Pi 操作系统)上安装 spotify。有了这个设置，Spotify 就可以在小米吸尘器上使用张自己所说的“*质量很差的扬声器*”。他们还制作了一个视频，展示他们会唱歌的吸尘器。

小米吸尘器内部扬声器的微弱噪音通过吸气噪音泄漏，高保真音响发烧友很可能不会将它作为他们的主要收听设备。然而，对于喜欢在清洁时移动到凹槽的洁癖者来说，或者甚至对于爱恶作剧的人来说，这是一个很好的补充。我们让您选择使用方式，但为了让 Spotify 在您的小米吸尘器或任何其他 Raspberry Pi 设备上运行，您需要完成几个步骤。

你需要通过 SSH 进入吸尘器的根目录，安装 Curl 和 Raspotify。然后，您需要在 Raspbian 中创建一个. config 文件来安装 Librespot，以便在每次启动时在吸尘器上启动 Spotify casting。如果你不确定这些步骤，张在他们的博客上有一个详细的[设置指南](https://eddiez.me/spotify-vacuum/)供你参考。