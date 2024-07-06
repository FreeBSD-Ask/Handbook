# 本书的组织结构

全书在逻辑上被分为五个独立的部分。第一部分是 **入门**，涵盖了 FreeBSD 的安装和基本用法。预设读者会按顺序阅读这些章节（可跳过已熟悉的话题）。第二部分是 **常见任务**，涵盖了一些 FreeBSD 的常用功能。第二及后续所有部分都可以乱序阅读。每章都以简洁的概述开头，讲解本章的内容以及读者应该掌握的知识。这样设计是为了让跳读的读者也能够找到感兴趣的章节。第三部分是 **系统管理**，涵盖了管理主题。第四部分是 **网络通信**，涵盖了网络和服务器主题。第五部分是包含了参考信息的附录。

**[简介](https://docs.freebsd.org/en/books/handbook/introduction/#introduction)**

为新用户讲解 FreeBSD。它涉及 FreeBSD 项目的历史、目标和开发模型。

**[安装 FreeBSD](https://docs.freebsd.org/en/books/handbook/bsdinstall/#bsdinstall)**

指导用户使用 bsdinstall 实现 FreeBSD 9.x（及更高版本）的完整安装。

**[FreeBSD 基础](https://docs.freebsd.org/en/books/handbook/basics/#basics)**

涵盖了 FreeBSD 操作系统的基础命令和功能。如果你熟悉 Linux® 或其他版本的 UNIX®，那么你大可以跳过本章节。

**[安装应用程序：软件包和 Ports](https://docs.freebsd.org/en/books/handbook/ports/#ports)**

涉及使用 FreeBSD 创新的“Ports”和单个二进制包来安装第三方软件的方法。

**[X Window 系统](https://docs.freebsd.org/en/books/handbook/x11/#x11)**

涉及 X Window 系统简介，以及如何在 FreeBSD 上使用 X11。还包含了常见的桌面环境，如 KDE 和 GNOME。

**[Wayland](https://docs.freebsd.org/en/books/handbook/wayland/#wayland)**

撰写了 Wayland 显示服务器大概情况，以及如何在 FreeBSD 上使用 Wayland。还讲解了常见的混成器，如 Wayfire、Hikari 和 Sway。

**[桌面应用程序](https://docs.freebsd.org/en/books/handbook/desktop/#desktop)**

列出了一些常见的桌面应用程序，例如网络浏览器和办公软件套件，并讲解如何在 FreeBSD 上进行安装。

**[多媒体](https://docs.freebsd.org/en/books/handbook/multimedia/#multimedia)**

展示如何为你的系统设置音频和视频播放功能。还讲解了一些示例音频和视频应用程序。

**[配置 FreeBSD 内核](https://docs.freebsd.org/en/books/handbook/kernelconfig/#kernelconfig)**

解释为什么你可能需要自定义新内核，并为配置、构建和安装自定义内核提供了详细的指导。

**[打印](https://docs.freebsd.org/en/books/handbook/printing/#printing)**

阐述在 FreeBSD 上管理打印机，包括有关横幅页面、打印机记账和初始设置的信息。

**[Linux® 二进制兼容层](https://docs.freebsd.org/en/books/handbook/linuxemu/#linuxemu)**

讲解了 FreeBSD 的 Linux® 兼容层功能。还为许多常用的 Linux® 应用程序（如 Oracle®、Mathematica®）提供了详细的安装说明。

**[WINE](https://docs.freebsd.org/en/books/handbook/wine/#wine)**

解释了什么是 WINE 以及详细的安装教程。还涉及了 WINE 的操作方式，如何安装 GUI 助手，如何在 FreeBSD 上运行 Windows® 应用程序，并包含了其他注意事项和解决方案。

**[配置和优化](https://docs.freebsd.org/en/books/handbook/config/#config-tuning)**

讲解了系统管理员可用于调整 FreeBSD 系统以获得最佳性能的参数。还涉及了 FreeBSD 中使用的各种配置文件以及它们的位置。

**[FreeBSD 引导过程](https://docs.freebsd.org/en/books/handbook/boot/#boot)**

讲解了 FreeBSD 引导过程，并解释了如何通过配置选项控制此过程。

**[安全](https://docs.freebsd.org/en/books/handbook/security/#security)**

讲解了许多可用于帮助保持 FreeBSD 系统安全的工具，包括 Kerberos、IPsec 和 OpenSSH。

**[jail](https://docs.freebsd.org/en/books/handbook/jails/#jails)**

讲解了 FreeBSD 中 jail 框架的功能，以及 jail 相较于传统的 chroot 所做的改进。

**[强制访问控制](https://docs.freebsd.org/en/books/handbook/mac/#mac)**

讲解了什么是强制访问控制（MAC），以及如何使用这种机制来保护 FreeBSD 系统。

**[安全事件审计](https://docs.freebsd.org/en/books/handbook/audit/#audit)**

讲解了什么是 FreeBSD 事件审计，如何安装，配置以及如何检查和监控审计日志。

**[存储](https://docs.freebsd.org/en/books/handbook/disks/#disks)**

讲解了如何使用 FreeBSD 管理存储介质和文件系统。例如物理磁盘、RAID 阵列、光盘和磁带介质、内存盘和网络文件系统。

**[GEOM：模块化磁盘转换框架](https://docs.freebsd.org/en/books/handbook/geom/#geom)**

讲解了在 FreeBSD 中，什么是 GEOM 框架，以及如何配置各种受支持级别的 RAID。

**[OpenZFS 存储平台](https://docs.freebsd.org/en/books/handbook/zfs/#zfs)**

讲解了 OpenZFS 存储平台，并提供了有关在 FreeBSD 下运行 OpenZFS 的快速入门指南和高级主题信息。

**[其他文件系统](https://docs.freebsd.org/en/books/handbook/filesystems/#filesystems)**

检查对 FreeBSD 下的非原生文件系统（如 ext2、ext3 和 ext4）的支持。

**[虚拟化](https://docs.freebsd.org/en/books/handbook/virtualization/#virtualization)**

讲解了虚拟化系统提供的内容，以及如何在 FreeBSD 中使用虚拟化。

**[本地化——i18n/L10n 的使用和配置](https://docs.freebsd.org/en/books/handbook/l10n/#l10n)**

讲解了如何配置 FreeBSD 使用除英语以外的其他语言，涵盖系统和应用程序级别的本地化。

**[更新和升级 FreeBSD](https://docs.freebsd.org/en/books/handbook/cutting-edge/#updating-upgrading)**

解释了 FreeBSD-STABLE、FreeBSD-CURRENT 和 FreeBSD 发布版之间的区别。讲解了何者可以从跟踪开发系统中获益，并概述了该过程。涵盖了用户将其系统更新到最新安全发行版本的几种方法。

**[DTrace](https://docs.freebsd.org/en/books/handbook/dtrace/#dtrace)**

介绍了如何在 FreeBSD 上配置和使用 Sun™ 开发的 DTrace 工具。动态跟踪可执行实时系统分析，用于帮助定位性能问题。

**[USB 设备模式/USB OTG](https://docs.freebsd.org/en/books/handbook/usb-device-mode/#usb-device-mode)**

介绍了在 FreeBSD 上使用 USB 设备模式和 USB On-The-Go（USB OTG）。

**[PPP](https://docs.freebsd.org/en/books/handbook/ppp-and-slip/#ppp-and-slip)**

介绍了如何在 FreeBSD 中使用 PPP 连接远程设备。

**[电子邮件](https://docs.freebsd.org/en/books/handbook/mail/#mail)**

介绍了电子邮件服务器的构成和组件，并深入探讨了最常见的邮件服务器软件：sendmail 的简单配置话题。

**[网络服务器](https://docs.freebsd.org/en/books/handbook/network-servers/#network-servers)**

提供了详细的讲解和示例配置文件，以将你的 FreeBSD 设备配置成网络文件系统服务器、域名服务器、网络信息系统服务器和时间同步服务器。

**[防火墙](https://docs.freebsd.org/en/books/handbook/firewalls/#firewalls)**

阐释了软件防火墙背后的哲学，并提供了适用于 FreeBSD 的多种防火墙的详细配置信息。

**[高级网络](https://docs.freebsd.org/en/books/handbook/advanced-networking/#advanced-networking)**

涉及许多网络主题，包括在局域网上与其他计算机共享互联网连接、高级路由主题、无线网络、蓝牙、ATM、IPv6 等。

**[获取 FreeBSD](https://docs.freebsd.org/en/books/handbook/mirrors/#mirrors)**

列出了得到 FreeBSD 光盘和 DVD 的多种方法，以及多个能让你在互联网上下载并安装 FreeBSD 的网站。

**[书目](https://docs.freebsd.org/en/books/handbook/bibliography/#bibliography)**

全书涉及多个主题，有可能让你渴望更深层次的解释。在书目列出了许多在文中引用的优秀书籍。

**[互联网资源](https://docs.freebsd.org/en/books/handbook/eresources/#eresources)**

涉及了供 FreeBSD 用户报告问题并参与有关 FreeBSD 的技术交流的论坛。

**[OpenPGP 密钥](https://docs.freebsd.org/en/books/handbook/pgpkeys/#pgpkeys)**

列出了几位 FreeBSD 开发人员的 PGP 指纹。
