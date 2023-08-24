# C.2. 邮件列表

邮件列表是解决问题或向集中的 FreeBSD 受众展开技术讨论的最直接的方式。有许多关于不同的 FreeBSD 主题的列表。将问题发送到最合适的邮件列表中，必然会得到更快、更准确的回应。

技术列表主题应保持技术性。

所有 FreeBSD 的用户和开发者都应该订阅 [FreeBSD 公告邮件列表](https://lists.freebsd.org/subscription/freebsd-announce)。

> **注意**
>
> 要测试向 FreeBSD 列表发送邮件的能力，请向 [FreeBSD 测试邮件列表](https://lists.freebsd.org/subscription/freebsd-test)发送测试信息。请不要向任何其他列表发送测试信息。

当对向哪个列表发布问题有疑问时，请看[如何从 FreeBSD-questions 邮件列表中获得最佳效果](https://docs.freebsd.org/en/articles/freebsd-questions/)。

在向任何列表发帖之前，请一定要：

- 通过阅读[邮件列表常见问题（FAQ）文件](https://docs.freebsd.org/en/articles/mailing-list-faq/)，了解如何最好地使用邮件列表，例如如何帮助避免频繁重复的讨论

- 搜索归档，以确定是否有人已经发布了您打算发布的内容

归档搜索界面包括：

- [https://lists.freebsd.org/search](https://lists.freebsd.org/search) (FreeBSD, experimental)

- [https://www.freebsd.org/search/](https://www.freebsd.org/search/) (DuckDuckGo)

- [https://freebsd.markmail.org/](https://freebsd.markmail.org/) (MarkMail)

请注意，这也意味着发送到 FreeBSD 邮件列表的信息将被永久存档。如果需要保护隐私，请考虑使用一次性的辅助电子邮件地址，并只发布公开信息。

FreeBSD 提供的归档文件：

- 不会特别标识超链接

- 不显示内联图像

- 不显示 HTML 信息的 HTML 内容

可在[此处](https://lists.freebsd.org/)查阅 FreeBSD 公共邮件列表。

## C.2.1. 如何订阅或取消订阅

要订阅一个列表，请在[https://lists.freebsd.org](https://lists.freebsd.org/)，点击列表名称。显示的页面应包含该列表的所有必要的订阅说明。

要实际发布到一个特定的列表，请发送邮件到 [listname@FreeBSD.org](listname@FreeBSD.org)。然后，它将被重新分配给世界各地的邮件列表成员。

## C.2.2. 列表基本规则

_所有的_ FreeBSD 邮件列表都有一些基本的规则，使用它们的人必须遵守。如果不遵守这些规定，将导致 FreeBSD Postmaster [postmaster@FreeBSD.org](postmaster@FreeBSD.org) 发出两次书面警告，之后，如果是第三次犯错，发帖者将被从所有 FreeBSD 邮件列表中删除，并被过滤掉不再发帖。我们很遗憾这样的规则和措施是必要的，但今天的互联网是一个相当严酷的环境，似乎很多人都没有意识到它的一些机制是多么的脆弱。

列表的规则:

- 任何帖子的主题都应该遵守它所发布的列表的基本章程。如果该列表是关于技术问题的，帖子应该包含技术讨论。持续的无关紧要的闲聊或谩骂只会减损邮件列表对每个人的价值，是不能被容忍的。对于没有特定主题的自由讨论，[FreeBSD 聊天邮件列表](https://lists.freebsd.org/subscription/freebsd-chat)是免费提供的，应该使用它。

- 不应该在 2 个以上的邮件列表上发帖，而且只有在明确和明显需要在两个列表上发帖的情况下才可以。对于大多数列表，已经有大量的订阅者重叠，除了最深奥的混合（例如`-stable & -scsi`），真的没有理由同时发布到一个以上的列表。如果收到的邮件在 _抄送栏_ 里有多个邮件列表，请在回复前修剪 _抄送栏_。_回复的人仍然要对交叉张贴负责，无论发起人是谁。_

- 个人攻击和亵渎（在争论的背景下）是不允许的，这包括用户和开发者。严重违反网络礼仪的行为，例如在没有或不会得到许可的情况下摘录或转贴私人邮件，是不被允许的，但没有特别强制执行。_然而_，也有很少的情况下，这样的内容会符合列表的章程，因此它可能会被警告（或禁止），仅此而已。

- 严禁宣传非 FreeBSD 相关的产品或服务，如果明显是以垃圾邮件的方式进行宣传，将被立即禁止。

## C.2.3. 邮件列表过滤

FreeBSD 邮件列表通过多种方式进行过滤，以避免垃圾邮件、病毒和其它不需要的邮件的传播。本节所描述的过滤操作并不包括用于保护邮件列表的所有操作。

邮件列表只允许某些类型的附件。所有 MIME 内容类型不在以下列表中的附件都将在邮件列表分发前被删除。

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
> 有些邮件列表可能允许使用其他 MIME 内容类型的附件，但上述列表应适用于大多数邮件列表。

如果多部分邮件包含 text/plain 和 text/html 两部分：

- 收件人将同时收到两部分

- lists.freebsd.org 将显示 text/plain，并提供查看原始文本（源代码，其中包括原始 HTML）的选项。

如果 text/plain 没有与 text/html 同时出现：

- 将 HTML 转换为纯文本。