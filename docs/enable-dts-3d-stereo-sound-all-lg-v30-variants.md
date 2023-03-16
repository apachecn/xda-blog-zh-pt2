# 在所有 LG V30 变体上启用 DTS 3D 立体声[Root]

> 原文：<https://www.xda-developers.com/enable-dts-3d-stereo-sound-all-lg-v30-variants/>

# 在所有 LG V30 变体上启用 DTS 3D 立体声[Root]

11 月推出的 LG V30 更新提到了 DTS 3D 立体声的添加。这种模式使它能够在设备的所有变体上运行。

有许多这样的情况，OEM 在他们的设备中使用硬件，但随后进入并使用软件来限制其功能。XDA 的发烧友社区以绕过这些限制而闻名，但也有像 LG 这样的情况。他们增加了(甚至提到了在 OTA 变更日志中增加了)一个特性，但最终搞乱了一个特性的初始实现。这似乎已经发生在 LG V30 的变种和它们的 DTS 3D 立体声音响上。

[**LG V30 XDA 论坛**](https://forum.xda-developers.com/lg-v30)

正如 XDA 认可的贡献者 [ChazzMatt](https://forum.xda-developers.com/member.php?u=3250376) 在论坛帖子中指出的，LG V30 在去年 11 月推出的更新提到了 DTS 3D 立体声的添加。但是，新功能不会作为单独的条目出现，这意味着您不能打开或关闭它。幸运的是，通过 root 访问，我们可以在 LG V30 的所有版本(V30/V30+/V30S)上修复这个错误，但截至目前，虽然 DTS 公告发布在 LG 的韩国网站上，但只有 US998 型号被确认有效。

为了让它工作，我们只需要使用一个根文件资源管理器(或 build.proper 编辑器),并在文件底部添加以下内容:

`ro.lge.globaleffect.dts=true`

[**在我们的 LG V30 论坛**](https://forum.xda-developers.com/lg-v30/how-to/enable-dts-3d-stereo-lg-v30-variants-t3887139) 查看这个 mod