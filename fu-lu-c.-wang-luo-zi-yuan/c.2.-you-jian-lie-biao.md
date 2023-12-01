# C.2. 邮件列表

邮件列表是直接与专注的 FreeBSD 受众提问或开展技术讨论的最直接方式。有许多不同主题的 FreeBSD 列表。将问题发送到最适合的邮件列表将始终确保更快速、更准确的响应。

技术列表的主题应该保持技术性。

所有 FreeBSD 用户和开发者都应该订阅[FreeBSD 公告邮件列表](https://lists.freebsd.org/subscription/freebsd-announce)。

> **注意**
> 
>为了测试 FreeBSD 邮件列表的功能，请使用[FreeBSD 测试邮件列表](https://lists.freebsd.org/subscription/freebsd-test)。请不要向任何其他列表发送测试消息。 

如果不确定应该将问题发布到哪个列表，请参阅[如何从 FreeBSD-questions 邮件列表中获取最佳结果](https://docs.freebsd.org/en/articles/freebsd-questions/)。

在发布到任何列表之前，请：

- 了解如何最好地使用邮件列表，如通过阅读[Mailing List Frequently Asked Questions](https://docs.freebsd.org/en/articles/mailing-list-faq/)（FAQ）文档来帮助避免频繁重复的讨论
- 搜索存档，以确定是否有其他人已经发布了您打算发布的内容。

存档搜索接口包括：

- [https://lists.freebsd.org/search](https://lists.freebsd.org/search)（FreeBSD，实验性）
- [https://www.freebsd.org/search/](https://www.freebsd.org/search/)（DuckDuckGo）

请注意，这也意味着发送到 FreeBSD 邮件列表的消息将永久存档。当保护隐私是一个关切时，考虑使用一次性的辅助电子邮件地址，并仅发布公共信息。

FreeBSD 提供的存档：

- 不以链接形式呈现链接
- 不显示内联图像
- 不显示 HTML 信息的 HTML 内容。

可以在[此处](https://lists.freebsd.org/)查看 FreeBSD 公共邮件列表。

## C.2.1. 如何订阅或取消订阅

在[https://lists.freebsd.org](https://lists.freebsd.org/)，点击列表名称以显示其选项。

要发布邮件，在订阅后，请发送邮件到`listname@FreeBSD.org`。该消息将被重新分发给列表成员。

## C.2.2. 基本规则清单

*所有*FreeBSD 邮件列表都有必须由使用它们的任何人遵守的基本规则。不遵守这些准则将导致来自 FreeBSD 邮件管理员[postmaster@FreeBSD.org](mailto:postmaster@FreeBSD.org)的两次书面警告，之后，如第三次违规，发布者将被从所有 FreeBSD 邮件列表中删除，并被过滤，不能再发布。我们很遗憾必须制定这样的规则和措施，但今天的互联网似乎是一个相当严酷的环境，许多人未能意识到某些机制是多么地脆弱。

规则：

- 任何帖子的主题应遵循其发布的列表的基本描述。如果列表涉及技术问题，帖子应包含技术讨论。持续的无关聊天或争吵只会削弱邮件列表对每个人的价值，将不被容忍。对于没有特定主题的自由讨论，[FreeBSD chat 邮件列表](https://lists.freebsd.org/subscription/freebsd-chat)是免费提供的，应该代替之。
- 不应将帖子发布到超过 2 个邮件列表，仅在明确需要同时发布到两个列表时才应该这样做。对于大多数列表来说，已经存在大量的订阅者重叠，除了最特殊的混合（例如"-stable & -scsi"）之外，实际上没有理由同时发布到多个列表。如果收到带有多个邮件列表的`Cc`行的消息，请在回复之前修剪`Cc`行。_无论起初的作者是谁，回复的人仍然负责跨邮件列表发布。_
- 不允许个人攻击和亵渎（在争论的背景下），包括用户和开发人员。粗糙的网络礼仪违规，比如在未经允许的情况下引用或转发私人邮件，虽然不是明文规定但仍然不受欢迎。
- 严禁广告（非 FreeBSD 相关的产品或服务），如果明确发现违规者正在通过垃圾邮件进行广告，将立即封禁。

## C.2.3. 邮件列表的过滤

FreeBSD 邮件列表以多种方式进行过滤，以避免分发垃圾邮件、病毒和其他不需要的电子邮件。本节描述的过滤操作不包括用于保护邮件列表的所有过滤。

只允许在邮件列表上发送某些类型的附件。在分发邮件列表之前，将剥离所有 MIME 内容类型未在下表中找到的附件。

- application/octet-stream
- application/pdf
- application/pgp-signature
- application/x-pkcs7-signature
- message/rfc822
- multipart/alternative
- multipart/related
- multipart/signed
- text/html
- text/plain
- text/x-diff
- text/x-patch

> **注意**
>
> 一些邮件列表可能允许其他 MIME 内容类型的附件，但上述列表应适用于大多数邮件列表。

如果多部分消息包括 text/plain 和 text/html 部分：

- 收件人将接收两个部分
- lists.freebsd.org 将呈现 text/plain，并提供查看原始文本（源代码，其中包含原始 HTML）的选项。

如果 text/plain 未伴随 text/html：

- 将从 HTML 转换为纯文本。
