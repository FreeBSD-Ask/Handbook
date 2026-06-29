# A.2.使用 Git

## A.2.1. 介绍

自 2020 年 12 月起，FreeBSD 以 git 作为主版本控制系统，用于存放 FreeBSD 所有基础源代码及文档。自 2021 年 4 月起，FreeBSD 以 git 作为唯一版本控制系统，用于存放 FreeBSD 全部 Ports。

> **注意**
>
> Git 主要是面向开发者的工具。普通用户可能更倾向于使用 `freebsd-update`（[“FreeBSD Update”](https://docs.freebsd.org/en/books/handbook/cutting-edge/#updating-upgrading-freebsdupdate)）来更新 FreeBSD 基本系统。

本节介绍如何在 FreeBSD 系统上安装 Git，并用它创建 FreeBSD 源代码仓库的本地副本。

### A.2.2. 安装

Git 可以通过 Ports 安装，也可以作为软件包安装：

```sh
# pkg install git
```

### A.2.3. 运行 Git

要将源码的干净副本获取到本地目录，可使用 `git clone`。这一目录称为*工作树*。

Git 使用 URL 来指代仓库。共有三个不同的仓库：`src` 存放 FreeBSD 系统源代码，`doc` 存放文档，`ports` 存放 FreeBSD Ports。三个仓库均可通过两种协议访问：HTTPS 和 SSH。例如，URL `https://git.FreeBSD.org/src.git` 指定的是 `src` 仓库的主分支，使用 `https` 协议。

表 1. FreeBSD Git 仓库 URL 表

| 项目 | Git URL |
| ---- | ------- |
| 通过 HTTPS 访问只读 src 仓库 | [`https://git.FreeBSD.org/src.git`](https://git.freebsd.org/src.git) |
| 通过 anon-ssh 访问只读 src 仓库 | `ssh://anongit@git.FreeBSD.org/src.git` |
| 通过 HTTPS 访问只读 doc 仓库 | [`https://git.FreeBSD.org/doc.git`](https://git.freebsd.org/doc.git) |
| 通过 anon-ssh 访问只读 doc 仓库 | `ssh://anongit@git.FreeBSD.org/doc.git` |
| 通过 HTTPS 访问只读 ports 仓库 | [`https://git.FreeBSD.org/ports.git`](https://git.freebsd.org/ports.git) |
| 通过 anon-ssh 访问只读 ports 仓库 | `ssh://anongit@git.FreeBSD.org/ports.git` |

项目成员维护的外部镜像同样可用，请参阅[外部镜像](#a.2.6.-外部镜像)一节。

克隆 FreeBSD 系统源代码仓库的副本：

```sh
# git clone -o freebsd https://git.FreeBSD.org/src.git /usr/src
```

`-o freebsd` 选项指定源头；按照 FreeBSD 文档惯例，源头默认为 `freebsd`。初始检出需要下载远程仓库的完整分支，可能耗时较长，请耐心等待。

初始时，工作树包含 `main` 分支的源代码，对应 CURRENT。如需切换到 13-STABLE：

```sh
# cd /usr/src
# git checkout stable/13
```

工作树可通过 `git pull` 更新。要更新上例中创建的 `/usr/src`，使用：

```sh
# cd /usr/src
# git pull --rebase
```

更新比首次检出快得多，仅传输发生变更的文件。

### A.2.4. 基于 Web 的仓库浏览器

FreeBSD 项目使用 cgit 作为基于 Web 的仓库浏览器：<https://cgit.FreeBSD.org/>。

### A.2.5. 面向开发者

关于仓库写权限，请参阅 [Committer's Guide](https://docs.freebsd.org/en/articles/committers-guide/#git-mini-primer)。

### A.2.6. 外部镜像

这些镜像不托管在 FreeBSD.org 上，但仍由项目成员维护。欢迎用户和开发者从这些镜像拉取或浏览仓库。`doc` 和 `src` 的 GitHub 仓库接受拉取请求；除此以外，这些镜像对应的项目工作流仍在讨论中。

Codeberg

* doc：<https://codeberg.org/FreeBSD/freebsd-doc>
* ports：[https://codeberg.org/FreeBSD/freebsd-ports](https://codeberg.org/FreeBSD/freebsd-ports)
* src：<https://codeberg.org/FreeBSD/freebsd-src>

GitHub

* doc：<https://github.com/freebsd/freebsd-doc>
* ports：[https://github.com/freebsd/freebsd-ports](https://github.com/freebsd/freebsd-ports)
* src：<https://github.com/freebsd/freebsd-src>

GitLab

* doc：<https://gitlab.com/FreeBSD/freebsd-doc>
* ports：<https://gitlab.com/FreeBSD/freebsd-ports>
* src：<https://gitlab.com/FreeBSD/freebsd-src>

### A.2.7. 邮件列表

FreeBSD 项目中讨论 git 通用用法及问题的邮件列表是 [freebsd-git](https://lists.freebsd.org/subscription/freebsd-git)。更多详情（包括提交记录邮件列表）请参阅[邮件列表](https://docs.freebsd.org/en/books/handbook/handbook/eresources/#eresources-mail)一章。

### A.2.8. SSH 主机密钥

* gitrepo.FreeBSD.org 主机密钥指纹：

  * ECDSA 密钥指纹：`SHA256:seWO5D27ySURcx4bknTNKlC1mgai0whP443PAKEvvZA`
  * ED25519 密钥指纹：`SHA256:lNR6i4BEOaaUhmDHBA1WJsO7H3KtvjE2r5q4sOxtIWo`
  * RSA 密钥指纹：`SHA256:f453CUEFXEJAXlKeEHV+ajJfeEfx9MdKQUD7lIscnQI`
* git.FreeBSD.org 主机密钥指纹：

  * ECDSA 密钥指纹：`SHA256:/UlirUAsGiitupxmtsn7f9b7zCWd0vCs4Yo/tpVWP9w`
  * ED25519 密钥指纹：`SHA256:y1ljKrKMD3lDObRUG3xJ9gXwEIuqnh306tSyFd1tuZE`
  * RSA 密钥指纹：`SHA256:jBe6FQGoH4HjvrIVM23dcnLZk9kmpdezR/CvQzm7rJM`

这些密钥指纹也会作为 SSHFP 记录发布在 DNS 中。
