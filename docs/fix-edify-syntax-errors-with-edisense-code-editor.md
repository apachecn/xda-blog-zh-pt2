# 使用 EdiSense 代码编辑器查找 Edify 语法错误

> 原文：<https://www.xda-developers.com/fix-edify-syntax-errors-with-edisense-code-editor/>

如果您曾经刷新过自定义 ROM，您可能已经注意到您的自定义恢复会读取某种脚本来格式化您的系统分区、创建符号链接等等。这组命令被称为“启迪”。通常 Edify 有两部分: *updater-script* ，是一个文本文件，里面有恢复的指令；以及*更新器-二进制*，其加载所述脚本。开源项目直接从源代码生成*更新脚本*，但并不是每个 rom 都是从源代码构建的。

破解陶冶脚本的语法极其容易。一个分号的缺失会中断 flash 并导致严重的错误。如果不阅读恢复日志，查找错误是有问题的。这就是为什么你会对 XDA 资深会员的一个工具感兴趣。

Yashade2001 创建了一个 Windows 专用的应用程序，它将极大地帮助查找语法错误。根据代码的类型，EdiSense 使用不同的颜色。例如，注释是绿色的，各种命令是深蓝色的。EdiSense 可以为您节省大量时间，并在几秒钟内找到错误。

目前，该工具仅适用于 Windows。希望开发者也能将它移植到其他操作系统上。如果你正在修改你的*更新脚本，*你一定要访问[原始线程](http://forum.xda-developers.com/showthread.php?t=2599759)，给 EdiSense 一个机会。