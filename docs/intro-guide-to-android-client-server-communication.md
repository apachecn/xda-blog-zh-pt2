# Android 客户端-服务器通信介绍指南

> 原文：<https://www.xda-developers.com/intro-guide-to-android-client-server-communication/>

随着我们的移动设备变得越来越互联，客户端-服务器通信也变得越来越必要。令人欣慰的是，一个新的指南已经出现，帮助用户设置 RESTful web API。

新的指南来自 XDA 论坛成员 Alkonic，涵盖的主题包括建立数据库和 PHP 脚本，测试新的数据库服务器，以及如何从 Android 访问它。该指南针对的是经验相对丰富的开发人员，他们有一个工作开发环境，已经编写了应用程序，但缺乏 MySQL 或 PHP 经验。

初涉云端的开发人员需要具备哪些入门条件？不多:一台用于测试的 Android 设备和一台运行在同一网络上的计算机，一台 Apache/MySQL/PHP 服务器，如 Windows 的 WAMP，以及 Chrome 的 Postman Rest 客户端。值得庆幸的是，Alkonic 还总结了客户端-服务器通信的新步骤:

> 1.  客户端使用 HTTP POST 向服务器发出请求
> 2.  PHP 脚本查询 MYSQL 服务器
> 3.  PHP 脚本获取 SQL 数据
> 4.  PHP 脚本将数据放入一个数组，并为这些值分配键。然后，脚本将数据输出为 JSON 数组。JSON(JavaScript Object Notation)是一个数据交换的标准，以一种人类和计算机都容易阅读的方式格式化数据。
> 5.  该应用程序解析 JSON 并显示数据。

要了解更多信息，请前往[导丝](http://forum.xda-developers.com/showthread.php?t=2325799)。