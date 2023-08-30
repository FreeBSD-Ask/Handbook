# 本书的组织结构

本书在逻辑上被分为五个不同的部分：第一部分，_入门_，包括 FreeBSD 的安装和基本使用。希望读者能按顺序阅读这些章节，但可以跳过你熟悉的章节。第二部分，_常见任务_，涵盖了 FreeBSD 的一些常用功能。这一节以及后面的所有章节都可以不按顺序阅读。每一章的开头都有一个简洁的概述，说明了这一章的内容和读者应该已知的内容。这样做的目的是让普通读者能够跳过这些已知章节，找到感兴趣的章节。第三部分，_系统管理_，包括管理主题。第四部分，_网络通信_，包括网络和服务器主题。第五部分包含了参考信息的附录。

**_[简介](https://docs.freebsd.org/en/books/handbook/introduction/index.html#introduction)_**

向新用户介绍 FreeBSD。并简要说明了 FreeBSD 项目的历史，目标和开发模式。

**_[安装 FreeBSD](https://docs.freebsd.org/en/books/handbook/bsdinstall/index.html#bsdinstall)_**

引导用户使用 bsdinstall 完成 FreeBSD 9.x 及以后版本的完整安装过程。

**_[FreeBSD 基础](https://docs.freebsd.org/en/books/handbook/bsdinstall/index.html#bsdinstall)_**

介绍了 FreeBSD 操作系统的基本命令和功能。如果你熟悉 Linux® 或其他 UNIX®，那么你可以跳过这一章。

**_[安装应用程序: 软件包和 Ports](https://docs.freebsd.org/en/books/handbook/ports/index.html#ports)_**

包含了如何使用 FreeBSD 创新的“ports”和标准二进制软件包来安装第三方软件。

**_[X Window](https://docs.freebsd.org/en/books/handbook/x11/index.html#x11)_**

介绍了常见的 X Window 系统，特别是在 FreeBSD 上使用的 X11。还介绍了常见的桌面环境，如 KDE 和 GNOME。

**_[Wayland](https://docs.freebsd.org/en/books/handbook/book/#wayland)_**

介绍了 Wayland 显示服务器的一般情况，特别是在 FreeBSD 上使用的 Wayland。还介绍了常见的合成器，如 Wayfire、Hikari 和 Sway。

**_[桌面应用程序](https://docs.freebsd.org/en/books/handbook/desktop/index.html#desktop)_**

列出了一些常见的桌面应用程序，如网络浏览器和生产力工具，并介绍了如何在 FreeBSD 上安装它们。

**_[多媒体](https://docs.freebsd.org/en/books/handbook/multimedia/index.html#multimedia)_**

演示了如何为你的系统设置声音和视频播放支持。还列出了一些音频和视频应用。

**_[配置 FreeBSD 内核](https://docs.freebsd.org/en/books/handbook/kernelconfig/index.html#kernelconfig)_**

介绍了为什么你可能需要配置一个新的内核，并提供了配置、编译和安装定制内核的详细说明。

**_[打印](https://docs.freebsd.org/en/books/handbook/printing/index.html#printing)_**

介绍了在 FreeBSD 上管理打印机的情况，包括关于横幅页面、打印审计和初始设置的信息。

**_[Linux® 二进制兼容层](https://docs.freebsd.org/en/books/handbook/linuxemu/index.html#linuxemu)_**

**_[WINE](https://docs.freebsd.org/en/books/handbook/book/#wine)_**

介绍了 WINE 并提供了详细的安装说明。还说明了 WINE 的操作方式，如何安装 GUI 助手，如何在 FreeBSD 上运行 Windows® 应用程序，并提供了其他提示和解决方案。

介绍了 FreeBSD 的 Linux® 兼容层。还提供了许多流行的 Linux® 应用程序（如 Oracle® 和 Mathematica®）的详细安装说明。

**_[配置与优化](https://docs.freebsd.org/en/books/handbook/config/index.html#config-tuning)_**

介绍了系统管理员可以用来优化 FreeBSD 系统的参数，以获得最佳性能。还介绍了 FreeBSD 中使用的各种配置文件以及在何处可以找到它们。

**_[FreeBSD 的引导过程](https://docs.freebsd.org/en/books/handbook/boot/index.html#boot)_**

介绍了 FreeBSD 的引导过程，并解释了如何通过配置选项来控制这个过程。

**_[安全](https://docs.freebsd.org/en/books/handbook/security/index.html#security)_**

列举了许多不同的工具，包括 Kerberos、IPsec 和 OpenSSH，以帮助确保你的 FreeBSD 系统安全。

**_[Jail](https://docs.freebsd.org/en/books/handbook/jails/index.html#jails)_**

介绍了 jail 框架，以及 jail 相对于 FreeBSD 传统的 chroot 支持所做的改进。

**_[强制访问控制](https://docs.freebsd.org/en/books/handbook/mac/index.html#mac)_**

解释了什么是强制访问控制（MAC），以及如何利用这一机制来保护 FreeBSD 系统。

**_[安全事件审计](https://docs.freebsd.org/en/books/handbook/audit/index.html#audit)_**

介绍了什么是 FreeBSD 事件审计，如何安装，配置，以及如何审计和监控审计跟踪。

**_[存储](https://docs.freebsd.org/en/books/handbook/disks/index.html#disks)_**

介绍了如何用 FreeBSD 管理存储设备和文件系统。这包括物理磁盘、RAID 阵列、光学介质和磁带、内存支持的磁盘以及网络文件系统。

**_[GEOM：模块化磁盘转换框架](https://docs.freebsd.org/en/books/handbook/geom/index.html#geom)_**

介绍了什么是 FreeBSD 中的 GEOM 框架，以及如何配置各种支持的 RAID 级别。

**_[OpenZFS 存储平台](https://docs.freebsd.org/en/books/handbook/book/#zfs)_**

介绍了 OpenZFS 存储平台，并提供了快速入门指南和有关在 FreeBSD 下运行 OpenZFS 的高级主题的信息。

**_[其他文件系统](https://docs.freebsd.org/en/books/handbook/filesystems/index.html#filesystems)_**

检查对 FreeBSD 下的非原生文件系统的支持，如 ext2、ext3 和 ext4。

**_[虚拟化](https://docs.freebsd.org/en/books/handbook/virtualization/index.html#virtualization)_**

介绍了虚拟化系统提供的功能，以及如何在 FreeBSD 中使用它们。

**_[本地化——i18n/L10n 的使用和设置](https://docs.freebsd.org/en/books/handbook/l10n/index.html#l10n)_**

介绍了如何用英语以外的语言使用 FreeBSD。涵盖了系统和应用层面的本地化。

**_[更新与升级 FreeBSD](https://docs.freebsd.org/en/books/handbook/cutting-edge/index.html#updating-upgrading)_**

阐述了 FreeBSD-STABLE、FreeBSD-CURRENT 和 FreeBSD-RELEASE 之间的区别。说明了哪些用户会从跟踪开发系统中受益，并概述了这个过程。说明了用户可以采取的方法来更新他们的系统到最新的安全版本。

**_[DTrace](https://docs.freebsd.org/en/books/handbook/dtrace/index.html#dtrace)_**

介绍了如何在 FreeBSD 中配置和使用 Sun™ 的 DTrace 工具。动态跟踪可以通过进行实时的系统分析来帮助定位性能问题。

**_[USB Device Mode / USB OTG](https://docs.freebsd.org/en/books/handbook/book/#usb-device-mode)_**

解释 FreeBSD 上 USB Device Mode 和 USB On The Go (USB OTG) 的使用。

**_[PPP](https://docs.freebsd.org/en/books/handbook/ppp-and-slip/index.html#ppp-and-slip)_**

介绍了如何在 FreeBSD 使用 PPP 来连接远程系统。

**_[电子邮件](https://docs.freebsd.org/en/books/handbook/mail/index.html#mail)_**

解释了电子邮件服务器的不同组成部分，并深入探讨了最流行的邮件服务器软件的简单配置主题：sendmail。

**_[网络服务器](https://docs.freebsd.org/en/books/handbook/network-servers/index.html#network-servers)_**

提供了详细的说明和配置文件的例子，以便将你的 FreeBSD 机器设置为网络文件系统服务器、域名服务器、网络信息系统服务器或时间同步服务器。

**_[防火墙](https://docs.freebsd.org/en/books/handbook/firewalls/index.html#firewalls)_**

解释了基于软件的防火墙背后的理念，并提供了关于配置不同的 FreeBSD 防火墙的详细说明。

**_[高级网络](https://docs.freebsd.org/en/books/handbook/advanced-networking/index.html#advanced-networking)_**

介绍了许多网络主题，包括与局域网中的其他计算机共享互联网连接、高级路由主题、无线网络、Bluetooth®、ATM、IPv6，以及更多。

**_[获取 FreeBSD](https://docs.freebsd.org/en/books/handbook/mirrors/index.html#mirrors)_**

列举了获得 FreeBSD CDROM 或 DVD 的不同方式，以及在互联网上可让你下载 FreeBSD 的网站。

**_[书目](https://docs.freebsd.org/en/books/handbook/bibliography/index.html#bibliography)_**

本书涉及到许多不同的主题，可能会让你渴望得到更详细的解释。书目中列出了许多在文中被引用的优秀书籍。

**_[网络资源](https://docs.freebsd.org/en/books/handbook/eresources/index.html#eresources)_**

介绍了许多可供 FreeBSD 用户发布问题和进行 FreeBSD 技术交流的论坛。

**_[OpenPGP 密钥](https://docs.freebsd.org/en/books/handbook/pgpkeys/index.html#pgpkeys)_**

列出了一些 FreeBSD 开发者的 PGP 公钥。
