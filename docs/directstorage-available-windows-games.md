# Windows 游戏现在可以使用 DirectStorage 在固态硬盘上更快地加载

> 原文：<https://www.xda-developers.com/directstorage-available-windows-games/>

微软宣布，从今天开始，Windows 游戏可以开始支持 DirectStorage API。这个 API 最早出现在 Xbox Series X|S 上，它通过利用现代 NVMe 固态硬盘的全速来加快游戏加载速度。微软早在 2020 年 9 月就宣布了它在 Windows 上的应用，但直到现在它才被开发者广泛使用。

如果你想知道为什么 DirectStorage 很重要，这里有一个快速的解释:以前的 API 只允许游戏通过一次执行一个 I/O 请求来从驱动器加载资源，并且每个请求必须在另一个请求被处理之前彻底完成。这只会导致每个请求的开销增加很少，因为机械硬盘和 SATA 固态硬盘没有那么快，对加载时间的影响也没有那么大。

然而现在，随着 NVMe 硬盘能够达到数千兆字节的读取速度，这一过程意味着几乎不可能在一次只处理一个请求的同时使用硬盘的全部带宽，这意味着游戏加载速度比预期慢得多。此外，这些资产通常是压缩的，它们需要解压缩才能加载到游戏中。

DirectStorage 通过一次允许多个 I/O 请求、利用新的解压缩技术以及更高效地向 GPU 提供资产来解决所有这些问题。通过改变这一切，当游戏使用 DirectStorage 时，它们可以加载得更快，最重要的是，它们可以开始使用更大的资产，因为开发人员可以放心，它们会加载得更快，不会让玩家等待。最终，这将缩短加载时间，并且随着开发者习惯于在游戏中拥有更多细节纹理。

然而，这个好处对 NVMe 固态硬盘更有利，这是因为它们使用的独特接口，由多个数据访问队列组成，这使得游戏更容易同时请求访问多个资产，而不必等待之前的请求完成。[由于采用了新的存储堆栈，Windows 11 用户也将受益最大](https://www.xda-developers.com/windows-11-auto-hdr-direct-storage/)。 [Windows 10 用户也将看到改进](https://www.xda-developers.com/microsofts-directstorage-api-for-games-is-coming-to-windows-10/)。

微软目前没有提到任何将使用该技术的游戏，但你可以假设任何在 Xbox 上利用 DirectStorage 的游戏也将在 Windows 上使用它。然而，你必须等待个别开发者在每款游戏中实现它，因为这不是微软能轻易打开的开关。

* * *

来源:[微软](https://devblogs.microsoft.com/directx/directstorage-api-available-on-pc/)