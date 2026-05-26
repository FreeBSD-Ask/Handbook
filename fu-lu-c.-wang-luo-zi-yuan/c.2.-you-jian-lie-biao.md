# C.2.邮件列表

邮件列表是向聚焦 FreeBSD 的受众提问或展开技术讨论的最直接途径。FreeBSD 有许多不同主题的邮件列表。将问题发到最合适的列表，几乎总能得到更快、更准确的回复。

技术列表的讨论应围绕技术话题展开。

所有 FreeBSD 的用户和开发者都应该订阅 [FreeBSD 公告邮件列表](https://lists.freebsd.org/subscription/freebsd-announce)。

如需测试 FreeBSD 邮件列表功能，请发往 FreeBSD 测试邮件列表，不要向其他列表发送测试消息。

不确定该向哪个列表提问时，可参考《如何从 FreeBSD-questions 邮件列表获得最佳结果》。

向任何列表发帖之前，请：

* 阅读[邮件列表常见问题（FAQ）文档](https://docs.freebsd.org/en/articles/mailing-list-faq/)，了解如何善用邮件列表，例如怎样避免反复出现相同的讨论。
* 搜索历史存档，确认是否已经有人发过相同问题。

存档搜索方式包括：

* <https://lists.freebsd.org/search>（FreeBSD，实验性）
* [https://www.freebsd.org/search/](https://www.freebsd.org/search/) (DuckDuckGo)

请注意，发往 FreeBSD 邮件列表的消息会永久存档。如有保护隐私的需要，建议使用一次性辅助邮箱地址，只发送公开信息。

FreeBSD 官方存档：

* 不将链接渲染为可点击的链接
* 不显示内嵌图片
* 不渲染 HTML 邮件中的 HTML 内容

FreeBSD 公共邮件列表可[在此](https://lists.freebsd.org/)查阅。

## C.2.1. 如何订阅或取消订阅

访问 <https://lists.freebsd.org>，点击列表名称可展开其选项。

订阅后，向 `listname@FreeBSD.org` 发送邮件即可发帖。邮件将分发给所有列表成员。

### C.2.2. 邮件列表基本规则

所有 FreeBSD 邮件列表均有基本规则，使用者必须遵守。违规者将收到 FreeBSD 邮件管理员 <postmaster@FreeBSD.org> 的两封书面警告，第三次违规时，该用户将被移出所有 FreeBSD 邮件列表，并禁止再次发帖。我们很遗憾不得不制定这些规则和措施，但如今互联网环境确实严酷，许多人未曾意识到某些机制有多么脆弱。

基本守则：

* 任何帖子的主题应符合所在列表的基本定位。如果列表以技术问题为主，帖子就应围绕技术讨论展开。持续发表无关言论或人身攻击只会降低邮件列表对所有人的价值，不会被容忍。若无特定主题、希望自由讨论，可使用 FreeBSD 聊天邮件列表。
* 不应同时向超过 2 个邮件列表发帖，且仅在确实有必要双发时才可如此。大多数列表的订阅者高度重叠，除了极罕见的组合（如 "-stable 与 -scsi"），没有理由向多个列表发帖。如果收到的邮件在抄送行列出多个邮件列表，回复前请先修剪抄送行。无论最初的发帖者是谁，回复者仍需对跨列表发帖负责。
* 禁止人身攻击和辱骂（包括争论中），用户和开发者无一例外。严重违反网络礼仪的行为（如未经许可摘录或转发私人邮件），虽然不会特别强制执行，但会受到谴责。
* 严禁推广与 FreeBSD 无关的产品或服务，一旦确认为垃圾广告发帖，将立即封禁。

### C.2.3. 在邮件列表上的过滤

FreeBSD 邮件列表经过多重过滤，以阻止垃圾邮件、病毒及其他不受欢迎邮件的分发。本节描述的过滤措施并非全部，仅涉及部分保护手段。

邮件列表只允许部分类型的附件。MIME 类型不在下表中的附件，会在邮件分发到邮件列表之前被剥离。

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

部分邮件列表可能允许其他 MIME 类型的附件，但上表已涵盖大多数邮件列表。

若一封多部分邮件同时包含 text/plain 和 text/html：

* 收件人将收到两部分
* lists.freebsd.org 会展示 text/plain 部分，并提供查看原始文本（源码，其中包含原始 HTML 内容）的选项。

若 text/plain 未与 text/html 同时出现：

* 将把 HTML 转换为纯文本。