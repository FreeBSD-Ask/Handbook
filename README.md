## 2024 FreeBSD 中文社区 翻译项目

> **PDF 文档**
>
> - 使用社区成员提供的脚本：
>   
>> 　　<https://github.com/safreya/tobook> 用于导出本书的 pdf，打印的话比 gitbook 导出的应该要好点。该脚本运行于 FreeBSD。
>> 
>> 具体使用方法见该项目的 README.

> **手册版本说明**
>
> 当前文档版本同步至官方文档 [2023-7-18 commit a9c93bee1de624ad6e55f2f081bce23da8df57a6](https://github.com/freebsd/freebsd-doc/commit/a9c93bee1de624ad6e55f2f081bce23da8df57a6)。如需更新请提交 issue 或 pull request。

## 译者相关

### 2023.12.1-2024 第二版中文翻译


使用 ChatGPT 重译。需要人手。



### 2022.1.8-2023.12.1 第一版中文翻译

**Deepl 机器翻译相关**

|               章节               |     Deepl 机器翻译    |        格式调整       |
| :----------------------------: | :---------: | :---------------: |
|               前言               |     ykla    |        魔王酱        |
|            第 1 章：简介            |     ykla    |        魔王酱        |
|        第 2 章：安装 FreeBSD        |     ykla    |   ulianchn38、歸野鴿  |
|    第 3 章：FreeBSD 基础【3.1-3.2】   |     ykla    |        ykla       |
|    第 3 章：FreeBSD 基础【3.3-EOL】   |    亲爱的翻译官   |      ykla、歸野鴿     |
|    第 4 章：安装应用程序: 软件包和 Ports    |    亲爱的翻译官   |   ykla、skadomsky  |
|   第 5 章：X Window 系统【5.1-5.2】   |  ykla|    ulianchn38、冰   |
|  第 5 章：X Window 系统 【5.3-5.4.6】 |    冰   |  ykla、ulianchn38  |
|  第 5 章：X Window 系统 【5.4.6-EOL】 |    Lin🌠    | ykla、ulianchn38、冰 |
|  第 6 章：FreeBSD 中的 Wayland          |    ykla  |          ykla|
|          第 7 章：桌面环境          |     胞嘧啶     |        ykla       |
|            第 8 章：多媒体           |     无目先生    |        ykla       |
|       第 9 章：配置 FreeBSD 内核      | Jasonlecson |       ykla、冰      |
|       第 10 章：打印 【9.1-9.4】       |     潇潇雨竹    |        ykla       |
|       第 10 章：打印 【9.5-EOL】       |  ulianchn38 |        ykla       |
|   第 11 章：Linux 二进制兼容层 【10.1】   |    Sayunosyjou   |        ykla       |
| 第 11 章：Linux 二进制兼容层 【10.2-EOL】 |  亲爱的翻译官|        ykla       |
|           第 12 章：wine          | Jasonlecson |       ykla、冰      |
|          第 13 章：配置与优化          |     胞嘧啶     |       ykla、冰      |
|      第 14 章：FreeBSD 的引导过程      |     徐艺扬     |     ykla、冰、歸野鴿    |
|            第 15 章：安全           |      陈诚     |       ykla、冰      |
|           第 16 章：Jail          |      陈诚     |       ykla、冰      |
|          第 17 章：强制访问控制         |      陈诚     |       ykla、冰      |
|          第 18 章：安全事件审计         |      冰      |      ykla、歸野鴿     |
|            第 19 章：存储           | Jasonlecson |       ykla、冰      |
|     第 20 章：GEOM: 模块化磁盘转换框架     | Jasonlecson |       ykla、冰      |
|       第 21 章：Z 文件系统（ZFS）|    徐艺扬、冰    |  ykla、ulianchn38  |
|          第 22 章：其他文件系统         | Jasonlecson |        ykla       |
|           第 23 章：虚拟化           |     歸野鴿     |       ykla、冰      |
|  第 24 章：本地化——i18n/L10n 的使用和设置 |      郴      |       ykla、冰      |
|      第 25 章：FreeBSD 更新与升级       |  亲爱的翻译官 |        ykla       |
|          第 26 章：DTrace         |     歸野鴿     |       ykla、冰      |
| 第 27 章：USB 设备模式/USB OTG | Jasonlecson |        ykla       |
|           第 28 章：串行通信          |     胞嘧啶     |       ykla、冰      |
|           第 29 章：PPP           |   ykla  |        ykla       |
|           第 30 章：电子邮件          |   ykla  |        ykla       |
|          第 31 章：网络服务器          |      陈诚     |       ykla、冰      |
|           第 32 章：防火墙           |      陈诚     |       ykla、冰      |
|           第 33 章：高级网络          |      陈诚     |       ykla、冰      |
|         附录 A：获取 FreeBSD        |    亲爱的翻译官   |        ykla       |
|             附录 B：书目            |     ykla    |        ykla       |
|            附录 C：网络资源           |    亲爱的翻译官   |        ykla       |
|         附录 D：OpenPGP 密钥        |     ykla    |        ykla       |
|               术语表              |    亲爱的翻译官   |        ykla       |

> >**名单排序以提交的先后顺序为准。未标明部分由 ykla 完成，下同。**

**校对相关（标记用户即为完成，下同）**

|               章节               |    第一轮校对  | 第二轮校对 | 第三轮校对 |
| :----------------------------: | :-----------: | :------: | :------: |
|               前言               | ykla |     罗胜(superluosheng)       |        |
|            第 1 章：简介            | ykla |    罗胜(superluosheng)        |        |
|        第 2 章：安装 FreeBSD    | ykla/Shengyun |    罗胜(superluosheng)        |         |
|        第 3 章：FreeBSD 基础        | ykla/Shengyun |    罗胜(superluosheng)        |        |
|    第 4 章：安装应用程序: 软件包和 Ports    | ykla/Shengyun |       罗胜(superluosheng)   |          |
|        第 5 章：X Window 系统       | ykla/Shengyun |   罗胜(superluosheng)         |       |
|        第 6 章：FreeBSD 中的 Wayland       | ykla/Shengyun |        |          |
|          第 7 章：桌面环境          | ykla/Shengyun |     罗胜(superluosheng)     |          |
|            第 8 章：多媒体           |      ykla     |  罗胜(superluosheng)        |          |
|       第 9 章：配置 FreeBSD 内核      |      ykla     |  罗胜(superluosheng)        |          |
|            第 10 章：打印            |      ykla     |      |          |
|       第 11 章：Linux 二进制兼容层      |      ykla     | 罗胜(superluosheng)         |          |
|           第 12 章：wine          |      ykla     |        |          |
|          第 13 章：配置与优化          |      ykla     |  罗胜(superluosheng)        |          |
|      第 14 章：FreeBSD 的引导过程      |      ykla     |         |          |
|            第 15 章：安全           |      ykla          |   罗胜(superluosheng)       |          |
|           第 16 章：Jail          |       ykla        |   罗胜(superluosheng)       |          |
|          第 17 章：强制访问控制         |       ykla/KCommit         |    罗胜(superluosheng)      |          |
|          第 18 章：安全事件审计         |    ykla           |         |          |
|            第 19 章：存储           |       ykla       |        |          
|     第 20 章：GEOM: 模块化磁盘转换框架     |     ykla           |        |          |
|       第 21 章：Z 文件系统 (ZFS)      |     ykla          |   罗胜(superluosheng)       |          |
|          第 22 章：其他文件系统         |     ykla          |   罗胜(superluosheng)       |          |
|           第 23 章：虚拟化           |        ykla       |    罗胜(superluosheng)      |          |
|  第 24 章：本地化——i18n/L10n 的使用和设置 |    ykla           |      |          |
|      第 25 章：FreeBSD 更新与升级      |       ykla        |   罗胜(superluosheng)       |          |
|          第 26 章：DTrace         |         ykla      |    罗胜(superluosheng)      |          |
| 第 27 章：USB 设备模式/USB OTG |             ykla  |        |          |
|           第 28 章：串行通信          |        ykla       |    罗胜(superluosheng)      |          |
|           第 29 章：PPP           |         ykla      |   罗胜(superluosheng)       |          |
|           第 30 章：电子邮件          |         ykla      |    罗胜(superluosheng)      |          |
|          第 31 章：网络服务器          |          ykla     |  罗胜(superluosheng)        |          |
|           第 32 章：防火墙           |        ykla       |    罗胜(superluosheng)      |          |
|           第 33 章：高级网络          |         ykla      |   罗胜(superluosheng)       |          |
|         附录 A：获取 FreeBSD        |         ykla      |   罗胜(superluosheng)       |          |
|             附录 B：书目            |     ykla          |          |          |
|            附录 C：网络资源           |      ykla         |          |          |
|         附录 D：OpenPGP 密钥        |     ykla          |          |          |
|               术语表              |          ykla       |   罗胜(superluosheng)       |          |

>> **章节之间的未标明部分也经过了校对。当前已校对章节仍然可能存在一些问题需要解决，见 [issue](https://github.com/FreeBSD-Ask/Handbook/issues)。**

## Q & A



本手册的翻译是为了活跃 FreeBSD 中文社区、助力 FreeBSD 系统生态发展。我们争取做到人人都可以写教程、参与开源协作。没有人强迫您阅读本手册，所以也请您不要诋毁我们。FreeBSD 中国境内的社区这十几年一本教程都没有，这不是我们想看到的。


* Q：怎样维护？
  * A：

翻译完毕后约 1 个月整体维护一次。对比官方 Handbook 进行更新。

## 关于

### 简介

来到这里你可能什么也得不到。也将不会失去任何东西。FreeBSD 中文用户社区！恪守古老的法则，追寻真正的自由。BSD 方为真正 UNIX 哲学继承者。加入我们，共同推进 FreeBSD 中国化与世界化。

|       资源      |                            链接                            |
| :-----------: | :------------------------------------------------------: |
|   Telegram 群  |     [https://t.me/freebsdba](https://t.me/oh_myBSD)     |
|      QQ 群     |                         787969044                        |
| Handbook 最新翻译 | [https://handbook.bsdcn.org](https://handbook.bsdcn.org) |
|  FreeBSD 入门书籍 |     [https://book.bsdcn.org](https://book.bsdcn.org)     |
|FreeBSD 开发者手册 最新翻译|       <https://porters-handbook.bsdcn.org>              |
|    FreeBSD 中文 man 手册       |         [https://man.bsdcn.org](https://man.bsdcn.org)                           |

扫码关注微信公众号：

![扫码关注微信公众号](./.gitbook/assets/qr.png)

### FreeBSD 中文社区 寄言：

> 每一个人的不经意付出和教程完善的分享，都是极具意义的，理论上会长久存在，你做的每一点一滴的努力与付出都会成为历史的印记和未来某些科技的驱动力的先驱。手册是死的，我们对手册的贡献是一直存活的，存活在那些使用 Handbook 的人的心中。
>
> **“The best time to plant a tree is 20 years ago. The second-best time is now.”（种一棵树最好的时间是十年前，其次是现在）——Dambisa Moyo,** _**dead aid**_
>
> 我希望有更多的人参与进来，一起协作这个开源项目。英语水平和计算机水平固然重要，但是翻译凭借的不是傲慢与偏见，不是苦难哲学，也不是泥潭般的社区，更不是所谓的巨苣，而是我们的心，翻译是用心来完成的！用心，每个人都可以参与，无论是错别字的修正还是大章节的翻译，都是有意义的。
>
> 想参加的朋友可以看看 [https://docs.qq.com/doc/DSUtxYmVwU29EdGVn](https://docs.qq.com/doc/DSUtxYmVwU29EdGVn)

### FreeBSD 中文社区的愿景

我们成立于 2018年3月17日，由贴吧——FreeBSD 吧发展到了 QQ 群（主群 787969044），Telegram 群，乃至于微信群。

我们的成员具有非常大的广泛性和普遍性，能够代表绝大多数 FreeBSD 用户的平均水平：可能根本没有听说过何为 FreeBSD，但这并不影响我们的交流与沟通。也许有人觉得这是浪费时间，但是没有新生力量的培养，何来 FreeBSD 的明天呢？谁不知道新人可能有很多坏习惯呢。

同鲁迅先生说的那样，但愿每个人都是一束光，照亮 FreeBSD 在中国大陆地区前进的光荣的荆棘路。也希望，你可以加入我们，共同组成漫天星光亦或者是星星之火。

无穷的远方，无数的人们，都和我有关。

我曾无数次眺望远山，想要找到一汪清泉，天总是不随人愿，还是没有找到。

我是谁，我们是谁？这个问题永远也不会有结果。

我们选择 FreeBSD，是因为想选择一个清晰、明了、可靠、稳固的一个操作系统在工作上给我们带来收益以及在生活中给我们带来乐趣。当然 FreeBSD 还存在很多问题，有待大家积极发现、探讨、完善，社会在进步，技术在进步，热情丝毫不减在持续，未来越来越美好。

我们必须团结起来做些什么事情，无论大小，哪怕只是谈谈自己的学习体会（但并非出于炫耀）。否则如果只是夸夸其谈的话，我们和那些只会吹牛逼的、只会键政的、互称大佬的群或社区有任何区别吗？如果没有区别，那就没有任何意义，那么我宁愿这个社区不再存在。如果大家有时间有精力的话可以考虑翻译文档，如果会编程的话可以考虑移植软件到 BSD，如果能力更高甚至可以参与系统开发。

### 黑名单与社区失信名单

见 <http://chinafreebsd.org/>。

