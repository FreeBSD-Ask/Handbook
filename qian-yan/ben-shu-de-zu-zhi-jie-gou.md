# 本书的组织结构

全书在逻辑上分为五个独立的部分。第一部分是 **快速开始**，涉及 FreeBSD 的安装和基本用法。期望读者按顺序阅读这些章节（可跳过已熟悉的话题）。第二部分是 **常见任务**，涉及一些 FreeBSD 的常用功能。第二及后续所有部分都可以不按顺序阅读。每章都以简洁的概述开头，说明该章涉及的内容以及读者应该已经了解的知识。这样设计是为了让跳读的读者也能够找到感兴趣的章节。第三部分是 **系统管理**，涉及管理主题。第四部分是 **网络通信**，涉及网络和服务器主题。第五部分是包含参考信息的附录。

**[简介](di-1-zhang-jian-jie/1.1.-gai-shu)**

为新用户介绍 FreeBSD。它说明了 FreeBSD 项目的历史、目标和开发模型。

**[安装 FreeBSD](di-2-zhang-an-zhuang-freebsd/2.1.-gai-shu)**

指导用户使用 bsdinstall 完成 FreeBSD 9.*x* 及更高版本的整个安装过程。

**[FreeBSD 基础](di-3-zhang-freebsd-ji-chu/3.1.-gai-shu)**

涉及 FreeBSD 操作系统的基础命令和功能。如果你熟悉 Linux® 或其他版本的 UNIX®，那么你可以跳过本章节。

**[安装应用程序：软件包和 Ports](di-4-zhang-an-zhuang-ying-yong-cheng-xu-ruan-jian-bao-he-ports/4.1.-gai-shu)**

涉及使用 FreeBSD 创新的 "Ports" 和标准二进制包来安装第三方软件的方法。

**[X Window 系统](../di-5-zhang-xwindow-xi-tong/5.1.-gai-shu.md)**

介绍 X Window 系统，并说明如何在 FreeBSD 上使用 X11。还涉及常见的桌面环境，如 KDE 和 GNOME。

**[FreeBSD 中的 Wayland](di-6-zhang-freebsd-zhong-de-wayland/6.1.-wayland-jian-jie)**

介绍 Wayland 显示服务器以及如何在 FreeBSD 上使用 Wayland。还涉及常见的混成器，如 Wayfire、Hikari 和 Sway。

**[网络](di-7-zhang-wang-luo/7.1.-gai-shu)**

涵盖基本的有线和无线网络配置，包括主机名、DNS 和故障排除。

**[桌面环境](../di-8-zhang-zhuo-mian-huan-jing/8.1.-gai-shu.md)**

列出了一些常见的桌面应用程序，例如网络浏览器和办公软件套件，并说明如何在 FreeBSD 上进行安装。

**[多媒体](di-9-zhang-duo-mei-ti/9.1.-gai-shu)**

展示如何为你的系统设置声音和视频播放功能。还介绍了一些示例音频和视频应用程序。

**[配置 FreeBSD 内核](di-10-zhang-pei-zhi-freebsd-nei-he/10.1.-gai-shu)**

说明为什么你可能需要配置新内核，并为配置、构建和安装定制内核提供了详细的指导。

**[打印](di-11-zhang-da-yin/11.1.-kuai-su-ru-men)**

说明在 FreeBSD 上管理打印机，包括有关横幅页面、打印机记账和初始设置的信息。

**[Linux® 二进制兼容层](di-12-zhang-linux-er-jin-zhi-jian-rong-ceng/12.1.-gai-shu)**

说明了 FreeBSD 的 Linux® 兼容层功能。还为许多常用的 Linux® 应用程序（如 Oracle®、Mathematica®）提供了详细的安装说明。

**[WINE](../di-13-zhang-wine/13.1.-gai-shu.md)**

说明了什么是 WINE 以及详细的安装教程。还涉及了 WINE 的操作方式，如何安装 GUI 助手，如何在 FreeBSD 上运行 Windows® 应用程序，并包含了其他注意事项和解决方案。

**[配置与优化](di-14-zhang-pei-zhi-yu-you-hua/14.1.-gai-shu)**

说明了系统管理员可用于调整 FreeBSD 系统以获得最佳性能的各种参数。还涉及了 FreeBSD 中使用的各种配置文件以及它们的位置。

**[FreeBSD 的引导过程](di-15-zhang-freebsd-de-yin-dao-guo-cheng/15.1.-gai-shu)**

说明了 FreeBSD 引导过程，并解释了如何通过配置选项控制此过程。

**[安全](di-16-zhang-an-quan/16.1.-gai-shu)**

说明了许多可用于帮助保持 FreeBSD 系统安全的工具，包括 Kerberos、IPsec 和 OpenSSH。

**[jail 与容器](di-17-zhang-jail/17.1.-gai-shu)**

说明了 FreeBSD 中 jail 框架的功能，以及 jail 相较于传统的 chroot 所做的改进。

**[强制访问控制](../di-18-zhang-qiang-zhi-fang-wen-kong-zhi/18.1.-gai-shu.md)**

说明了什么是强制访问控制（MAC），以及如何使用这种机制来保护 FreeBSD 系统。

**[安全事件审计](di-19-zhang-an-quan-shi-jian-shen-ji/19.1.-gai-shu)**

说明了什么是 FreeBSD 事件审计，如何安装、配置，以及如何检查和监控审计日志。

**[存储](di-20-zhang-cun-chu/20.1.-gai-shu)**

说明了如何使用 FreeBSD 管理存储介质和文件系统。包括物理磁盘、RAID 阵列、光盘和磁带介质、内存盘和网络文件系统。

**[GEOM：模块化磁盘转换框架](../di-21-zhang-geom-mo-kuai-hua-ci-pan-zhuan-huan-kuang-jia/21.1.-gai-shu.md)**

说明了在 FreeBSD 中什么是 GEOM 框架，以及如何配置各种受支持级别的 RAID。

**[Z 文件系统（ZFS）](../di-22-zhang-z-wen-jian-xi-tong-zfs/22.1.-shi-shi-mo-shi-zfs-yu-zhong-bu-tong.md)**

说明了 Z 文件系统，并提供了在 FreeBSD 下运行 ZFS 的快速入门指南和高级主题信息。

**[其他文件系统](../di-23-zhang-qi-ta-wen-jian-xi-tong/23.1.-gai-shu.md)**

检查 FreeBSD 对非原生文件系统（如 ext2、ext3 和 ext4）的支持。

**[虚拟化](../di-24-zhang-xu-ni-hua/24.1.-gai-shu.md)**

说明了虚拟化系统提供的内容，以及如何在 FreeBSD 中使用虚拟化。

**[本地化——i18n/L10n 的使用和设置](../di-25-zhang-ben-di-hua-i18nl10n-de-shi-yong-he-she-zhi/25.1.-gai-shu.md)**

说明了如何配置 FreeBSD 使用除英语以外的其他语言，涉及系统和应用程序级别的本地化。

**[FreeBSD 更新与升级](di-26-zhang-freebsd-geng-xin-yu-sheng-ji/26.1.-gai-shu)**

解释了 FreeBSD-STABLE、FreeBSD-CURRENT 和 FreeBSD-RELEASE 间的区别。说明了哪些用户可以从跟踪开发系统中获益，并概述了该过程。涵盖了几种将系统更新到最新安全发行版本的方法。

**[DTrace](di-27-zhang-dtrace/27.1.-gai-shu)**

介绍了如何在 FreeBSD 上配置和使用 Sun™ 开发的 DTrace 工具。动态跟踪可执行实时系统分析，用于帮助定位性能问题。

**[USB 设备模式/USB OTG](di-28-zhang-usb-she-bei-mo-shi-usb-otg/28.1.-gai-shu)**

介绍了在 FreeBSD 上使用 USB 设备模式和 USB On-The-Go（USB OTG）。

**[串行通信](di-29-zhang-chuan-hang-tong-xin/29.1.-gai-shu)**

介绍了如何在 FreeBSD 中使用串行通信。

**[PPP](../di-30-zhang-ppp/30.1.-gai-shu.md)**

介绍了如何在 FreeBSD 中使用 PPP 连接远程设备。

**[电子邮件](di-31-zhang-dian-zi-you-jian/31.1.-gai-shu)**

介绍了电子邮件服务器的构成和组件，并深入探讨了最常见的邮件服务器软件：sendmail 的简单配置话题。

**[网络服务器](di-32-zhang-wang-luo-fu-wu-qi/32.1.-gai-shu)**

提供了详细的说明和示例配置文件，以将你的 FreeBSD 设备配置成网络文件系统服务器、域名服务器、网络信息系统服务器和时间同步服务器。

**[防火墙](di-33-zhang-fang-huo-qiang/33.1.-gai-shu)**

解释了软件防火墙背后的理念，并提供了适用于 FreeBSD 的多种防火墙的详细配置信息。

**[高级网络](di-34-zhang-gao-ji-wang-luo/34.1.-gai-shu)**

涉及许多网络主题，包括在局域网上与其他计算机共享互联网连接、高级路由主题、无线网络、蓝牙、ATM、IPv6 等。

**[获取 FreeBSD](../fu-lu-a.-huo-qu-freebsd/a.1.-jing-xiang-zhan.md)**

列出了获取 FreeBSD 光盘和 DVD 的多种方法，以及多个能让你在互联网上下载并安装 FreeBSD 的网站。

**[书目](fu-lu-b.-shu-mu/b.1.-freebsd-xiang-guan-shu-ji)**

由于本书涉及许多不同主题，你可能需要对某些主题的进一步解释。书目列出了许多在文中引用的优秀书籍。

**[网络资源](fu-lu-c.-wang-luo-zi-yuan/c.1.-wang-zhan)**

涉及了供 FreeBSD 用户提出问题并参与有关 FreeBSD 的技术交流的论坛。

**[OpenPGP 密钥](fu-lu-d.-openpgp-mi-yue/d.1.-guan-fang-cheng-yuan)**

列出了几位 FreeBSD 开发人员的 PGP 指纹。
