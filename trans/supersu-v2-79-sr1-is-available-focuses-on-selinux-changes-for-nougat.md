# SuperSU v2.79 SR1 可用，专注于牛轧糖的 SELinux 更改

> 原文：<https://www.xda-developers.com/supersu-v2-79-sr1-is-available-focuses-on-selinux-changes-for-nougat/>

昨天，Chainfire 宣布了 SuperSU 2.78 版本稳定后的首次更新。正如我们之前提到的，SR 更新基本上是 SuperSU 测试版的不同名称。更改名称是为了减少试图将测试版上传到非 Google Play 应用商店的人数，因为它将继续使用相同的版本号。

这里的大多数变化都是在 Android 7.x Nougat 上的 SELinux，尽管这个新更新还有很多其他变化。Chainfire 表示，这个版本现在将使用自己的“u:r:supersu:s0”上下文来运行。因此，这种改变可以避免一些冲突的发生，而不是重用“u:r:init:s0”上下文。然而，我们被警告说，这种变化可能会使一些根应用程序(甚至一些固件)突然停止工作。

SuperSU v2.79 SR1 不再修改 file_contexts[。bin]也是。Chainfire 注意到这一修改导致了一些特定固件的问题。虽然他们还不能确定冲突的原因，但是注意到是修改导致了冲突。一些人报告说，当一台设备安装了一堆应用程序时，SuperSU 在启动时授予某些应用程序 root 访问权限的速度很慢。这主要发生在牛轧糖上，我们被告知这应该不会再是什么大问题了。

你可以在这里下载 flash able zip for[v 2.79 SR1](http://download.chainfire.eu/1017/SuperSU/SR1-SuperSU-v2.79-SR1-20161221223537.zip)，如果你在新版本中遇到任何问题，我们鼓励你查看 SuperSU 测试版的 [XDA 论坛主题。此更新的完整变更日志可以在下面找到。](http://forum.xda-developers.com/apps/supersu/2014-09-02-supersu-v2-05-t2868133)

*   展开三星检测
*   GUI:在 7.0 以上版本中修改了“supersu”上下文
*   GUI:修正了在某些情况下用户禁用超级用户时的二进制更新通知
*   苏:修改了 7.0 以上版本的“超级苏”环境
*   su/GUI:提高 7.0 以上版本设备繁忙时的响应能力
*   sukernel:修复了文件名非常短的 cpio 恢复失败
*   sukernel:不再修补 file_contexts(。bin)
*   sukernel:revert force sec label(supersu 上下文不再需要)
*   supolicy:添加“创建”、“审核允许”、“审核拒绝”策略命令
*   supolicy:支持“*”作为“allow”、“deny”、“auditallow”、“auditdeny”、“allowxperm”策略命令的权限/范围参数
*   支持策略:- live/ -如果提供了自定义修补程序，文件不再应用默认修补程序
*   支持:- sdk=X 选项已添加(7.0 以上版本需要)
*   supolicy:修改了 7.0+的所有 SELinux 规则，作为“supersu”上下文运行
*   ZIP:分离 slotselect 和 system_root 逻辑
*   ZIP:调整系统/系统根设备和挂载点检测
*   ZIP:修复文档中的小错误
*   ZIP/frp:明确标记/su

[**来源:+火链**](https://plus.google.com/+Chainfire/posts/WrCvex7KAZR)