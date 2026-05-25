# 第四版

当前版本的手册体现了工作组的累积努力，工作组一直在审查和更新手册中的所有内容。以下是自第四版手册以来的主要更新。

* 手册已从 [Docbook](https://docbook.org/) 转换为 [Hugo](https://gohugo.io/) 和 [AsciiDoctor](https://asciidoctor.org/)。
* 创建了 [FreeBSD 文档门户](https://docs.freebsd.org/)。
* [简介](../di-1-zhang-jian-jie/1.1.-gai-shu.md)章节已更新，改进了 FreeBSD 历史部分并修正了小的拼写错误。
* [安装](../di-2-zhang-an-zhuang-freebsd/2.1.-gai-shu.md)章节已更新，升级了概述，包含了安装程序的最新更改，刷新了图片，为图片添加了替代文本，并移除了对特定版本的引用。
* [基础](../di-3-zhang-freebsd-ji-chu/3.1.-gai-shu.md)章节已更新表格、命令输出，以及根据 man:hier 更新了目录结构。
* [Ports](../di-4-zhang-an-zhuang-ying-yong-cheng-xu-ruan-jian-bao-he-ports/4.1.-gai-shu.md)章节已更新，简化了软件包搜索，更新了软件示例（Nginx 替代了 Apache），改进了 pkg(8) 引导过程，并添加了配置和管理软件包的新说明，包括阻止和取消阻止。
* [X Window](../di-5-zhang-xwindow-xi-tong/5.1.-gai-shu.md)章节已更新以反映 FreeBSD 中图形系统的当前状态，移除了对旧 Intel 驱动程序、配置和 compiz 的过时引用，并将桌面环境说明（如 KDE Plasma 和 GNOME）移至桌面环境章节，因为这些环境现在除了 X11 外还支持 Wayland。
* 新增了 [Wayland](../di-6-zhang-freebsd-zhong-de-wayland/6.1.-wayland-jian-jie.md)章节，包含在 FreeBSD 上安装和配置 Wayland 的信息。
* [网络](../di-7-zhang-wang-luo/7.1.-gai-shu.md)章节已创建，涵盖基本的有线和无线网络配置，包括主机名、DNS 和故障排除。有线网络、无线和 IPv6 相关章节已迁移并更新，改进了命令输出，使用了 sysrc，并采用了更好的 AsciiDoc 语法。
* [桌面环境](../di-8-zhang-zhuo-mian-huan-jing/8.1.-gai-shu.md)章节已更新，升级了 KDE Plasma、GNOME、XFCE、MATE、Cinnamon 和 LXQT 的安装说明，扩展了浏览器选项，新增了开发工具部分，并更新了桌面办公、文档阅读器和财务部分。
* [多媒体](../di-9-zhang-duo-mei-ti/9.1.-gai-shu.md)章节已重构，更新了声音部分，新增了声音混音器、音频播放器和视频播放器的表格，添加了自动耳机切换的指导，新增了视频会议部分，并修订了图像扫描仪部分。
* [Linux 二进制兼容层](../di-12-zhang-linux-er-jin-zhi-jian-rong-ceng/12.1.-gai-shu.md)章节已改进，更新了使用 debootstrap 设置 Debian/Ubuntu 基本系统的说明。
* [配置与优化](../di-14-zhang-pei-zhi-yu-you-hua/14.1.-gai-shu.md)章节已更名以提高准确性，更新了服务管理、cron 和 periodic、syslog、电源管理和交换分区部分。新增了配置文件条目，并移除了过时的优化部分。
* [安全](../di-16-zhang-an-quan/16.1.-gai-shu.md)章节已更新，增强了基于 IPSec 的 VPN、账户安全、密码哈希、sudo/doas 和 OpenSSH/OpenSSL。新增了涉及 IDS、安全等级、文件标志位、Capsicum、NFSv4 ACL 和资源限制的章节。
* [jail](../di-17-zhang-jail/17.1.-gai-shu.md)章节已更新，包含了 jail 类型（厚 jail、瘦 jail、VNET 和 Linux Jail）的详细信息、主机系统配置、网络选项、jail 配置文件、设置过程、升级方法、资源限制，以及不同的 jail 管理器和容器方案。
* [电子邮件](../di-31-zhang-dian-zi-you-jian/31.1.-gai-shu.md)章节已更新，包含了 DMA 的信息、Sendmail 的升级、将 DMA 和 Sendmail 更改为使用不同 MTA 的说明，并移除了拨号和 Fetchmail 部分，同时重新组织了章节。
* [书目](../fu-lu-b.-shu-mu/b.1.-freebsd-xiang-guan-shu-ji.md)得到了大规模更新。
