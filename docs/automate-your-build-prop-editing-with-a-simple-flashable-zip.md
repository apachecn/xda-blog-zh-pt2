# 自动化您的构建。用一个简单的闪光拉链进行适当的编辑

> 原文：<https://www.xda-developers.com/automate-your-build-prop-editing-with-a-simple-flashable-zip/>

这绝对不是秘密，我们许多人喜欢破解闪光我们的 ROM 夜生活。毕竟，这是保持 rom 特性最前沿的最好方法，除非你自己编译并从 ROM 的 Gerrit 中挑选。我们中的许多人也喜欢修改我们的 *build.prop* ,或者为 Android 版本字段添加厚脸皮的文本，或者修改可能改变某些功能操作方式的设置。但是如果你每天都在刷新你的 ROM，这可能会变得相当麻烦。

幸运的是，XDA 论坛成员 [klenamenis](http://forum.xda-developers.com/member.php?u=5431257) 创造了一种自动编辑你的 *build.prop* 的方法。klenamenis 的解决方案不是简单地将你的 *build.prop* 从一个 ROM build 复制到另一个 ROM build，而是允许你在一个 *tweakprop.sh* 文件中创建一个变更列表，该列表定位你想要修改和变更的字段。

以这种方式执行 *build.prop* 修改有两个好处。首先，如果 ROM 的 *build.prop* 改变也没关系，因为它只搜索和替换你选择的文本。即使你的 ROM 的 *build.prop* 保持不变，这仍然比在闪存之前手动将文件复制到存档中更方便。

如果你发现自己经常在夜间刷新 ROM 构建，并且厌倦了手动 *build.prop* 编辑，那就去[原始线程](http://forum.xda-developers.com/showthread.php?t=2664332)那里试试吧。