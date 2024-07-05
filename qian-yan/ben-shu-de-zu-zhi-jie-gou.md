# 本书的组织结构

这本书在逻辑上被分为五个独立的部分。第一部分是入门，涵盖了 FreeBSD 的安装和基本用法。预设读者会按顺序阅读这些章节，但读者可以跳过已经熟悉的话题章节。第二部分是常见任务，涵盖了 FreeBSD 的一些常用功能。这部分和所有后续部分都可以以任何顺序进行阅读。每个章节都以简洁的概述开头，说明了本章包含的内容以及读者预期应该已经了解的内容。这样设计是为了让泛读的读者能够找到感兴趣的章节。第三部分是系统管理，涵盖了管理主题。第四部分是网络通信，涵盖了网络和服务器主题。第五部分包含参考信息的附录。

*[简介](https://docs.freebsd.org/en/books/handbook/introduction/#introduction)*

给新用户介绍 FreeBSD。它诉说了 FreeBSD 项目的历史、目标和开发模型。

*[安装 FreeBSD](https://docs.freebsd.org/en/books/handbook/bsdinstall/#bsdinstall)*

引导用户使用 bsdinstall，来完成 FreeBSD 9.x 及更高版本的完整安装过程。

*[FreeBSD 基础](https://docs.freebsd.org/en/books/handbook/basics/#basics)*

涵盖了 FreeBSD 操作系统的基本命令和功能。如果你熟悉 Linux® 或其他 UNIX® 版本，那么你大可以跳过本章节。

*[安装应用程序：软件包和端口](https://docs.freebsd.org/en/books/handbook/ports/#ports)*

介绍使用 FreeBSD 创新的“Ports”和标准二进制包来安装第三方软件。

*[X Window 系统](https://docs.freebsd.org/en/books/handbook/x11/#x11)*

描述了 X Window 系统一般情况以及在 FreeBSD 上使用 X11。还描述了常见的桌面环境，如 KDE 和 GNOME。

*[Wayland](https://docs.freebsd.org/en/books/handbook/wayland/#wayland)*

描述了 Wayland 显示服务器一般情况以及在 FreeBSD 上使用 Wayland。还描述了常见的混成器，如 Wayfire、Hikari 和 Sway。

*[桌面应用程序](https://docs.freebsd.org/en/books/handbook/desktop/#desktop)*

列出一些常见的桌面应用程序，例如网络浏览器和办公软件套件，并描述如何在 FreeBSD 上安装它们。

*[多媒体](https://docs.freebsd.org/en/books/handbook/multimedia/#multimedia)*

展示如何为你的系统设置音频和视频播放支持。还描述了一些示例音频和视频应用程序。

*[配置 FreeBSD 内核](https://docs.freebsd.org/en/books/handbook/kernelconfig/#kernelconfig)*

解释为什么你可能需要自定义一个新的内核，并为配置、构建和安装自定义内核提供了详细的指导。

*[打印](https://docs.freebsd.org/en/books/handbook/printing/#printing)*

描述在 FreeBSD 上管理打印机，包括有关横幅页面、打印机记账和初始设置的信息。

*[Linux® 二进制兼容性](https://docs.freebsd.org/en/books/handbook/linuxemu/#linuxemu)*

说明了 FreeBSD 的 Linux® 兼容功能。还为许多常用的 Linux® 应用程序提供了详细的安装说明，如 Oracle® 和 Mathematica®。

*[WINE](https://docs.freebsd.org/en/books/handbook/wine/#wine)*

描述了 WINE 并提供了详细的安装说明。还描述了 WINE 的操作方式，如何安装 GUI 助手，如何在 FreeBSD 上运行 Windows®应用程序，并提供其他提示和解决方案。

*[配置和调整](https://docs.freebsd.org/en/books/handbook/config/#config-tuning)*

描述了系统管理员可用于调整 FreeBSD 系统以获得最佳性能的参数。还描述了 FreeBSD 中使用的各种配置文件以及它们的位置。

*[FreeBSD 引导过程](https://docs.freebsd.org/en/books/handbook/boot/#boot)*

描述了 FreeBSD 启动过程，并解释了如何通过配置选项控制此过程。

*[安全性](https://docs.freebsd.org/en/books/handbook/security/#security)*

描述了许多可用于帮助保持你的 FreeBSD 系统安全的工具，包括 Kerberos、IPsec 和 OpenSSH。

*[jail](https://docs.freebsd.org/en/books/handbook/jails/#jails)*

描述了 FreeBSD 中 jail 框架的功能，以及 jail 相较于传统 chroot 支持的改进。

*[强制访问控制](https://docs.freebsd.org/en/books/handbook/mac/#mac)*

说明了强制访问控制（MAC）是什么，以及如何使用这种机制来保护 FreeBSD 系统。

*[安全事件审计](https://docs.freebsd.org/en/books/handbook/audit/#audit)*

描述了 FreeBSD 事件审计是什么，如何安装，配置以及如何检查或监视审计日志。

*[存储](https://docs.freebsd.org/en/books/handbook/disks/#disks)*

描述如何使用 FreeBSD 管理存储介质和文件系统。这包括物理磁盘、RAID 阵列、光盘和磁带介质、内存支持的磁盘和网络文件系统。

*[GEOM：模块化磁盘转换框架](https://docs.freebsd.org/en/books/handbook/geom/#geom)*

描述了在 FreeBSD 中，什么是 GEOM 框架，以及如何配置各种级别受支持的 RAID。

*[OpenZFS 存储平台](https://docs.freebsd.org/en/books/handbook/zfs/#zfs)*

描述了 OpenZFS 存储平台，并提供了关于在 FreeBSD 下运行 OpenZFS 的快速入门指南和高级主题信息。

*[其他文件系统](https://docs.freebsd.org/en/books/handbook/filesystems/#filesystems)*

检查对 FreeBSD 下的非本机文件系统（如 ext2、ext3 和 ext4）的支持。

*[虚拟化](https://docs.freebsd.org/en/books/handbook/virtualization/#virtualization)*

描述虚拟化系统提供的内容，以及如何在 FreeBSD 中使用它们。

*[本地化 - i18n/L10n 的用途和设置](https://docs.freebsd.org/en/books/handbook/l10n/#l10n)*

描述如何在英语以外的语言中使用 FreeBSD。涵盖系统和应用程序级别的本地化。

*[更新和升级 FreeBSD](https://docs.freebsd.org/en/books/handbook/cutting-edge/#updating-upgrading)*

解释了 FreeBSD-STABLE、FreeBSD-CURRENT 和 FreeBSD 发布版之间的区别。描述了哪些用户可以从跟踪开发系统中获益，并概述了该过程。涵盖了用户可能采取的方法来将其系统更新到最新的安全发布版。

*[DTrace](https://docs.freebsd.org/en/books/handbook/dtrace/#dtrace)*

描述了如何在 FreeBSD 上配置和使用 Sun™的 DTrace 工具。动态跟踪可以帮助定位性能问题，通过进行实时系统分析。

*[USB 设备模式/USB OTG](https://docs.freebsd.org/en/books/handbook/usb-device-mode/#usb-device-mode)*

解释了在 FreeBSD 上使用 USB 设备模式和 USB On The Go (USB OTG)。

*[PPP](https://docs.freebsd.org/en/books/handbook/ppp-and-slip/#ppp-and-slip)*

描述如何使用 PPP 连接到 FreeBSD 中的远程系统。

*[电子邮件](https://docs.freebsd.org/en/books/handbook/mail/#mail)*

解释电子邮件服务器的不同组成部分，并深入讨论最流行的邮件服务器软件 sendmail 的简单配置主题。

*[网络服务器](https://docs.freebsd.org/en/books/handbook/network-servers/#network-servers)*

提供详细的说明和示例配置文件，以将你的 FreeBSD 机器设置为网络文件系统服务器、域名服务器、网络信息系统服务器或时间同步服务器。

*[防火墙](https://docs.freebsd.org/en/books/handbook/firewalls/#firewalls)*

解释了软件防火墙背后的哲学，并提供了关于可用于 FreeBSD 的不同防火墙配置的详细信息。

*[高级网络](https://docs.freebsd.org/en/books/handbook/advanced-networking/#advanced-networking)*

描述许多网络主题，包括在局域网上与其他计算机共享 Internet 连接、高级路由主题、无线网络、蓝牙、ATM、IPv6 等等。

*[获取 FreeBSD](https://docs.freebsd.org/en/books/handbook/mirrors/#mirrors)*

列出获取 FreeBSD 光盘或 DVD 的不同来源，以及允许你下载并安装 FreeBSD 的互联网上的不同站点。

*[参考书目](https://docs.freebsd.org/en/books/handbook/bibliography/#bibliography)*

这本书涉及许多不同主题，可能会让你渴望更详细的解释。参考书目列出了文中引用的许多优秀书籍。

*[互联网资源](https://docs.freebsd.org/en/books/handbook/eresources/#eresources)*

描述了供 FreeBSD 用户发布问题并参与有关 FreeBSD 的技术对话的许多论坛。

*[OpenPGP 密钥](https://docs.freebsd.org/en/books/handbook/pgpkeys/#pgpkeys)*

列出了几位 FreeBSD 开发人员的 PGP 指纹。
