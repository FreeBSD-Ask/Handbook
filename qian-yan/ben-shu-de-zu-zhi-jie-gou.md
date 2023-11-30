# 本书的组织结构

这本书分为五个逻辑上独立的部分。第一部分，_入门_，涵盖了 FreeBSD 的安装和基本用法。预计读者会按顺序阅读这些章节，可能会跳过涵盖熟悉主题的章节。第二部分，_常见任务_，涵盖了 FreeBSD 的一些经常使用的功能。这一部分以及后续的所有部分都可以无序阅读。每个章节都以简明扼要的概要开始，说明了章节涵盖的内容以及读者预期已经了解的内容。这旨在使普通读者能够跳到感兴趣的章节。

第三部分，_系统管理_，涵盖了管理主题。第四部分，_网络通信_，涵盖了网络和服务器主题。第五部分包含参考信息的附录。

- **[向新用户介绍 FreeBSD](https://docs.freebsd.org/en/books/handbook/book/#introduction)**。

说明了 FreeBSD 项目的历史、目标和开发模型。

- **[安装 FreeBSD](https://docs.freebsd.org/en/books/handbook/book/#bsdinstall)**

引导用户使用 bsdinstall 完成 FreeBSD 9.x 及更高版本的整个安装过程。

- **[FreeBSD 基础](https://docs.freebsd.org/en/books/handbook/book/#basics)**

涵盖了 FreeBSD 操作系统的基本命令和功能。如果您熟悉 Linux® 或其他 UNIX® 的变种，可能可以跳过这一章节。

- **[安装应用程序：软件包和 Ports](https://docs.freebsd.org/en/books/handbook/book/#ports)**

使用 FreeBSD 创新的"Ports Collection"和标准二进制软件包安装第三方软件。

- **[X Window 系统](https://docs.freebsd.org/en/books/handbook/book/#x11)**

概述 X Window System 及在 FreeBSD 上使用 X11。还说明了常见的桌面环境，如 KDE 和 GNOME。

- **[Wayland](https://docs.freebsd.org/en/books/handbook/book/#wayland)**

概述 Wayland 显示服务器及在 FreeBSD 上使用 Wayland。还说明了常见的合成器，如 Wayfire、Hikari 和 Sway。

- **[桌面应用程序](https://docs.freebsd.org/en/books/handbook/book/#desktop)**

列出一些常见的桌面应用程序，如 Web 浏览器和办公套件，并说明如何在 FreeBSD 上安装它们。

- **[多媒体](https://docs.freebsd.org/en/books/handbook/book/#multimedia)**

演示如何设置系统的声音和视频播放支持。还说明了一些示例音频和视频应用程序。

- **[配置 FreeBSD 内核](https://docs.freebsd.org/en/books/handbook/book/#kernelconfig)**

解释为什么可能需要配置新内核，并提供详细的配置、构建和安装自定义内核的说明。

- **[打印](https://docs.freebsd.org/en/books/handbook/book/#printing)**

说明在 FreeBSD 上管理打印机，包括有关横幅页、打印机记账和初始设置的信息。

- **[Linux 二进制兼容层](https://docs.freebsd.org/en/books/handbook/book/#linuxemu)**

说明 FreeBSD 的 Linux® 兼容功能。还提供了许多流行 Linux® 应用程序（如 Oracle® 和 Mathematica®）的详细安装说明。

- **[WINE](https://docs.freebsd.org/en/books/handbook/book/#wine)**

说明 WINE 并提供详细的安装说明。还说明了 WINE 的操作方式、如何安装 GUI 助手、在 FreeBSD 上运行 Windows® 应用程序以及其他提示和解决方案。

- **[配置与调优](https://docs.freebsd.org/en/books/handbook/book/#config-tuning)**

说明供系统管理员调整 FreeBSD 系统以获得最佳性能的参数。还说明了 FreeBSD 中使用的各种配置文件以及它们的位置。

- **[FreeBSD 引导过程](https://docs.freebsd.org/en/books/handbook/book/#boot)**

说明 FreeBSD 引导过程，并解释如何使用配置选项控制此过程。

- **[安全](https://docs.freebsd.org/en/books/handbook/book/#security)**

说明许多不同的工具，可帮助保持 FreeBSD 系统的安全性，包括 Kerberos、IPsec 和 OpenSSH。

- **Jail**

说明 Jail 框架以及 Jail 相对于 FreeBSD 传统 chroot 支持的改进。

- **[强制访问控制](https://docs.freebsd.org/en/books/handbook/book/#mac)**

解释强制访问控制（MAC）是什么，以及如何使用此机制保护 FreeBSD 系统。

- **安全事件审计**

说明 FreeBSD 事件审计是什么，如何安装、配置以及如何检查或监视审计日志。

- **[存储](https://docs.freebsd.org/en/books/handbook/book/#disks)**

说明如何使用 FreeBSD 管理存储介质和文件系统**。这包括物理磁盘、RAID 阵列、光盘和磁带介质、内存支持的磁盘以及网络文件系统。

- **[GEOM：模块化磁盘转换框架](https://docs.freebsd.org/en/books/handbook/book/#geom)**

说明 FreeBSD 中 GEOM 框架是什么以及如何配置各种支持的 RAID 级别。

- **[OpenZFS 存储平台](https://docs.freebsd.org/en/books/handbook/book/#zfs)**

说明 OpenZFS 存储平台**，并提供有关在 FreeBSD 下运行 OpenZFS 的快速入门指南和高级主题的信息。

- **[其他文件系统](https://docs.freebsd.org/en/books/handbook/book/#filesystems)**

检查 FreeBSD 下对非本地文件系统的支持**，如 ext2、ext3 和 ext4。

- **[虚拟化](https://docs.freebsd.org/en/books/handbook/book/#virtualization)**

说明虚拟化系统提供了什么以及如何与 FreeBSD 一起使用它们。

- **[本地化——i18n/L10n 使用与设置](https://docs.freebsd.org/en/books/handbook/book/#l10n)**

说明如何在非英语语言环境中使用 FreeBSD。涵盖系统和应用程序级本地化。

- **[更新和升级 FreeBSD](https://docs.freebsd.org/en/books/handbook/book/#updating-upgrading)**

解释 FreeBSD-STABLE、FreeBSD-CURRENT 和 FreeBSD 发布之间的差异。说明哪些用户将受益于跟踪开发系统，并概述该过程。介绍用户可能采取的方法来将其系统更新到最新的安全版本。

- **[DTrace](https://docs.freebsd.org/en/books/handbook/book/#dtrace)**

说明如何配置和使用 Sun™ 在 FreeBSD 上的 DTrace 工具。动态跟踪可以通过进行实时系统分析来帮助定位性能问题。

- **[USB 设备模式 / USB OTG](https://docs.freebsd.org/en/books/handbook/book/#preface-overview:~:text=time%20system%20analysis.-,USB%20Device%20Mode%20/%20USB%20OTG,-Explains%20the%20use)**

解释在 FreeBSD 上使用 USB 设备模式和 USB On The Go (USB OTG)。

- **[PPP](https://docs.freebsd.org/en/books/handbook/book/#ppp-and-slip)**

说明如何使用 PPP 连接到 FreeBSD 上的远程系统。

- **[电子邮件](https://docs.freebsd.org/en/books/handbook/book/#mail)**

解释电子邮件服务器的不同组件，并深入探讨了最流行的邮件服务器软件的简单配置主题：sendmail。

- **[网络服务](https://docs.freebsd.org/en/books/handbook/book/#network-servers)**

提供了设置 FreeBSD 机器作为网络文件系统服务器、域名系统服务器、网络信息系统服务器或时间同步服务器的详细说明和示例配置文件。

- **[防火墙](https://docs.freebsd.org/en/books/handbook/book/#firewalls)**
  
阐释基于软件的防火墙背后的哲学，并提供有关 FreeBSD 可用的不同防火墙配置的详细信息。

- **[高级网络](https://docs.freebsd.org/en/books/handbook/book/#advanced-networking)**

说明许多网络主题，包括在 LAN 上与其他计算机共享 Internet 连接、高级路由主题、无线网络、Bluetooth®、ATM、IPv6 等。

- **[获取 FreeBSD](https://docs.freebsd.org/en/books/handbook/book/#mirrors)**

列出在 CDROM 或 DVD 上获取 FreeBSD 媒体的不同来源以及允许您下载和安装 FreeBSD 的 Internet 上的不同站点。

- **[书目](https://docs.freebsd.org/en/books/handbook/book/#bibliography)**

这本书涉及许多不同的主题，可能会让您渴望获得更详细的解释**。参考文献中列出了在文本中引用的许多优秀的书籍。

- **[互联网资源](https://docs.freebsd.org/en/books/handbook/book/#eresources)**

说明了 FreeBSD 用户发布问题和参与有关 FreeBSD 的技术讨论的许多论坛。

- **OpenPGP 密钥**

列出了几位 FreeBSD 开发人员的 PGP 指纹**。
