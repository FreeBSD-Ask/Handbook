# C.2. 邮件列表

邮件列表是直接向专注于 FreeBSD 的听众提问或开展技术讨论的最直接方式。有多种不同主题的 FreeBSD 邮件列表。将问题发送到最适合的邮件列表几乎总能确保更快速和更准确的回应。

技术列表线程应保持技术性。

所有 FreeBSD 的用户和开发者都应该订阅 FreeBSD 公告邮件列表。

|  | 要测试 FreeBSD 邮件列表功能，请选择 FreeBSD 测试邮件列表。请不要向其他列表发送测试信息。 |
| -- | ------------------------------------------------------------------------------------------ |

当你对应该向哪个列表发布问题感到困惑时，请参阅如何从 FreeBSD-questions 邮件列表中获得最佳结果。

在发布到任何列表之前，请：

* 通过阅读邮件列表常见问题（FAQ）文档了解如何最好地使用邮件列表，例如如何帮助避免经常重复的讨论。
* 搜索档案，以确定是否有人已经发布了您打算发布的内容。

档案搜索界面包括：

* https://lists.freebsd.org/search（FreeBSD，实验性）
* [https://www.freebsd.org/search/](https://www.freebsd.org/search/) (DuckDuckGo)

注意，这也意味着发送到 FreeBSD 邮件列表的消息将永久存档。当保护隐私是一个关注点时，请考虑使用一次性次要电子邮件地址，并仅发布公共信息。

FreeBSD 提供的存档：

* 不要将链接显示为链接
* 不要显示内嵌图像
* 不要显示 HTML 消息的 HTML 内容

FreeBSD 公共邮件列表可以在这里查阅。

### C.2.1. 如何订阅或取消订阅

在 https://lists.freebsd.org 上，点击列表名称以显示其选项。

To post, after subscribing, send mail to `listname@FreeBSD.org`. The message will be redistributed to list members.

### C.2.2. Lists Basic Rules

所有 FreeBSD 邮件列表都有一些基本规则，所有使用者必须遵守。如果不遵守这些指导方针，将会收到两封来自 FreeBSD 邮件管理员 postmaster@FreeBSD.org 的书面警告。在第三次违规后，将从所有 FreeBSD 邮件列表中删除该用户，并且不允许继续发布。我们很遗憾必须制定这些规则和措施，但今天的互联网环境似乎相当恶劣，许多人未能意识到一些机制是多么脆弱。

道路规则：

* 任何帖子的主题都应符合其所发布到的列表的基本描述。如果列表是关于技术问题的，帖子应包含技术讨论。持续的无关废话或争吵只会削弱邮件列表对所有人的价值，将不受容忍。对于没有特定主题的自由讨论，请使用免费提供并应该使用的 FreeBSD 聊天邮件列表。
* 不应该向超过 2 个邮件列表发布帖子，只有在明显需要同时发布到两个列表时才可以。对于大多数列表，订阅者的重叠已经很多了，除了一些最神秘的组合（比如 "-stable & -scsi"），实际上没有理由同时发布到多个列表。如果收到带有多个邮件列表的邮件，请在回复之前修整邮件列表行。无论原始发起人是谁，回复的人仍然负责跨列表发布。
* 个人攻击和粗言秽语（在争论的背景下）是不允许的，包括用户和开发者。对网络礼仪的严重违反，比如未经许可擅自引用或转载私人邮件，虽然不会特别执行，但也受到谴责。
* 禁止广告非 FreeBSD 相关的产品或服务，如果明显是垃圾邮件广告，将立即封禁。

### C.2.3. 在邮件列表上的过滤

FreeBSD 邮件列表通过多种方式进行过滤，以避免分发垃圾邮件、病毒和其他不需要的电子邮件。本节所述的过滤操作不包括用于保护邮件列表的所有操作。

邮件列表上只允许某些类型的附件。所有未在下表中找到的 MIME 内容类型的附件将在邮件分发到邮件列表之前被删除。

* application/octet-stream
* application/pdf
* application/pgp-signature
* application/x-pkcs7-signature
* message/rfc822
* multipart/alternative
* multipart/related
* multipart/signed
* text/html
* text/plain
* text/x-diff
* text/x-patch

|  | 一些邮件列表可能允许附件为其他 MIME 内容类型，但上述列表适用于大多数邮件列表。 |
| -- | -------------------------------------------------------------------------------- |

如果多部分消息包括 text/plain 和 text/html 部分：

* 收件人将收到两个部分
* lists.freebsd.org 将显示 text/plain，并提供查看原始文本（源代码，包含原始 HTML 部分）的选项。

如果 text/plain 没有伴随 text/html：

* 将会将 HTML 转换成纯文本。
