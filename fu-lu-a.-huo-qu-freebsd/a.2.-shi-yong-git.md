# A.2.使用 Git

### A.2.1. 介绍

截至 2020 年 12 月，FreeBSD 使用 git 作为存储所有 FreeBSD 基础源代码和文档的主要版本控制系统。截至 2021 年 4 月，FreeBSD 使用 git 作为存储所有 FreeBSD ports 的唯一版本控制系统。

|  | Git 通常是开发者工具。用户可能更喜欢使用 freebsd-update （“FreeBSD Update”）来更新 FreeBSD 基本系统。|
| -- | --------------------------------------------------------------------------------------------------------- |

本节演示了如何在 FreeBSD 系统上安装 Git 并使用它创建 FreeBSD 源代码存储库的本地副本。

### A.2.2. 安装

Git 可以从 Ports 中安装，或者作为软件包安装：

```
# pkg install git
```

### A.2.3. 运行 Git

要将源代码的干净副本提取到本地目录中，请使用 git clone。这些文件的目录称为工作树。

Git 使用 URL 来指定存储库。有三个不同的存储库，src 用于 FreeBSD 系统源代码，doc 用于文档，ports 用于 FreeBSD Ports 。所有三个存储库都可以通过两种不同的协议访问：HTTPS 和 SSH。例如，URL <https://git.FreeBSD.org/src.git> 指定了 src 存储库的主分支，使用 https 协议。

表 1. FreeBSD Git 存储库 URL 表

| Item                                | Git URL |
| ------------------------------------- | --------- |
| Read-only src repo via HTTPS        | [`https://git.FreeBSD.org/src.git`](https://git.freebsd.org/src.git)        |
| 通过 anon-ssh 访问只读源代码存储库  | `ssh://anongit@git.FreeBSD.org/src.git`        |
| 通过 HTTPS 访问只读文档存储库       | [`https://git.FreeBSD.org/doc.git`](https://git.freebsd.org/doc.git)        |
| 通过 anon-ssh 访问只读文档存储库    | `ssh://anongit@git.FreeBSD.org/doc.git`        |
| 通过 HTTPS 读取只读 ports 存储库    | [`https://git.FreeBSD.org/ports.git`](https://git.freebsd.org/ports.git)        |
| 通过 anon-ssh 读取只读 ports 存储库 | `ssh://anongit@git.FreeBSD.org/ports.git`        |

项目成员维护的外部镜像也可用；请参考外部镜像部分。

克隆 FreeBSD 系统源代码存储库的副本：

```
# git clone -o freebsd https://git.FreeBSD.org/src.git /usr/src
```

-o freebsd 选项指定源头；按照 FreeBSD 文档规定，源头默认为 freebsd。由于初始的检出必须下载远程存储库的完整分支，可能需要一些时间。请耐心等待。

最初，工作树包含 main 分支的源代码，对应于 CURRENT。要改为使用 13-STABLE：

```
# cd /usr/src
# git checkout stable/13
```

工作树可以使用 git pull 进行更新。要更新上面示例中创建的 /usr/src，请使用：

```
# cd /usr/src
# git pull --rebase
```

更新比检出快得多，只传输已更改的文件。

### A.2.4. 基于 Web 的仓库浏览器

FreeBSD 项目使用 cgit 作为基于 web 的存储库浏览器：<https://cgit.FreeBSD.org/。>

### A.2.5. 对于开发人员

有关对存储库的写访问权限的信息，请参阅 Committer’s Guide。

### A.2.6. 外部镜像

这些镜像并非托管在 FreeBSD.org 上，但仍由项目成员维护。用户和开发人员可以拉取或浏览这些镜像上的存储库。对 doc 和 src GitHub 存储库的拉取请求正在接受；否则，与这些镜像的项目工作流程仍在讨论中。

Codeberg

* 文档: <https://codeberg.org/FreeBSD/freebsd-doc>
* ports: [https://codeberg.org/FreeBSD/freebsd-ports](https://codeberg.org/FreeBSD/freebsd-ports)
* 源码: <https://codeberg.org/FreeBSD/freebsd-src>

GitHub

* 文档: <https://github.com/freebsd/freebsd-doc>
* ports: [https://github.com/freebsd/freebsd-ports](https://github.com/freebsd/freebsd-ports)
* 源码：<https://github.com/freebsd/freebsd-src>

GitLab

* 文档：<https://gitlab.com/FreeBSD/freebsd-doc>
* ports：<https://gitlab.com/FreeBSD/freebsd-ports>
* src：<https://gitlab.com/FreeBSD/freebsd-src>

### A.2.7. 邮件列表

FreeBSD 项目中用于一般使用和关于 git 的问题的主邮件列表是 freebsd-git。有关更多详细信息，包括提交消息列表，请参阅邮件列表章节。

### A.2.8. SSH 主机密钥

* gitrepo.FreeBSD.org 主机密钥指纹:

  * ECDSA 密钥指纹是 SHA256:seWO5D27ySURcx4bknTNKlC1mgai0whP443PAKEvvZA
  * ED25519 密钥指纹是 SHA256:lNR6i4BEOaaUhmDHBA1WJsO7H3KtvjE2r5q4sOxtIWo
  * RSA 密钥指纹是 SHA256:f453CUEFXEJAXlKeEHV+ajJfeEfx9MdKQUD7lIscnQI
* git.FreeBSD.org 主机密钥指纹：

  * ECDSA 密钥指纹为 SHA256:/UlirUAsGiitupxmtsn7f9b7zCWd0vCs4Yo/tpVWP9w
  * ED25519 密钥指纹为 SHA256:y1ljKrKMD3lDObRUG3xJ9gXwEIuqnh306tSyFd1tuZE
  * RSA 密钥指纹为 SHA256:jBe6FQGoH4HjvrIVM23dcnLZk9kmpdezR/CvQzm7rJM

这些也会作为 SSHFP 记录发布在 DNS 中。
