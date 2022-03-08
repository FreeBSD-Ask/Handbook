#  A.2.使用Git

## A.2.1.简介

从2020年12月起，FreeBSD 使用 git 作为主要的版本控制系统来存储所有 FreeBSD 的基本源代码和文档。从 2021 年 4 月起，FreeBSD 使用 git 作为唯一的版本控制系统来存储所有的 FreeBSD 的 port 集。

**Git 通常是一个开发者工具。用户可能更喜欢使用 freebsd-update (“FreeBSD Update”) 来更新 FreeBSD 基本系统，以及 portsnap ("Using the Ports Collection") 来更新 FreeBSD Ports Collection。**

这一节演示了如何在 FreeBSD 系统上安装 Git 并使用它来创建 FreeBSD 源代码仓库的本地拷贝。

## A.2.2.安装

Git 可以从 Ports Collection 中安装，也可以作为一个软件包安装。

`# pkg install git`

## A.2.3.运行Git

要取一个干净的源码拷贝到本地目录，请使用 `git clone`。这个目录下的文件被称为工作树。

Git 使用 URL 来指定一个仓库。有三个不同的仓库，src 是指 FreeBSD 系统的源代码，doc 是指文档，而 ports 则是指 FreeBSD Ports Collection。这三个库都可以通过两种不同的协议到达。HTTPS 和 SSH。例如，URL https://git.FreeBSD.org/src.git 指定了 src 仓库的主分支，并使用了 https 协议。

表1. FreeBSD Git 仓库的 URL 表

|             **Item**              |                         **Git URL**                          |
| :-------------------------------: | :----------------------------------------------------------: |
|   Read-only src repo via HTTPS    | [https://git.FreeBSD.org/src.git](https://git.freebsd.org/src.git) |
|  Read-only src repo via anon-ssh  |            ssh://anongit@git.FreeBSD.org/src.git             |
|   Read-only doc repo via HTTPS    | [https://git.FreeBSD.org/doc.git](https://git.freebsd.org/doc.git) |
|  Read-only doc repo via anon-ssh  |            ssh://anongit@git.FreeBSD.org/doc.git             |
|  Read-only ports repo via HTTPS   | [https://git.FreeBSD.org/ports.git](https://git.freebsd.org/ports.git) |
| Read-only ports repo via anon-ssh |           ssh://anongit@git.FreeBSD.org/ports.git            |

由项目成员维护的外部镜像也可以使用，请参考外部镜像部分。

要克隆一份 FreeBSD 系统源代码库的副本。

```
# git clone -o freebsd https://git.FreeBSD.org/src.git /usr/src
```
-o freebsd 选项指定了起源；根据 FreeBSD 文档的惯例，起源被假定为 freebsd。因为初始签出必须下载远程仓库的完整分支，所以可能需要一些时间。请耐心等待。

最初，工作树包含主分支的源代码，对应的是 CURRENT。要切换到 13-STABLE，而不是

```
# cd /usr/src
# git checkout stable/13
```
工作树可以用 git pull 更新。要更新上面的例子中创建的`/usr/src`，请使用。

```
# cd /usr/src
# git pull --rebase
```
更新比结账要快得多，只传输有变化的文件。

## A.2.4.基于网络的资源库浏览器

FreeBSD 项目使用 cgit 作为基于网络的版本库浏览器：https://cgit.FreeBSD.org/。

## A.2.5. 对于开发商来说

关于对存储库的写入权限的信息，请参见《提交人指南》。

## A.2.6. 外部镜面

这些镜像并不在 FreeBSD.org 中托管，但仍由项目成员维护。我们欢迎用户和开发人员拉取或浏览这些镜像上的仓库。目前正在接受对 doc GitHub 仓库的拉取请求；除此之外，项目与这些镜像的工作流程仍在讨论中。

Codeberg

- doc: https://codeberg.org/FreeBSD/freebsd-doc
- ports: https://codeberg.org/FreeBSD/freebsd-ports
- src: https://codeberg.org/FreeBSD/freebsd-src

GitHub

- doc: https://github.com/freebsd/freebsd-doc
- ports: https://github.com/freebsd/freebsd-ports
- src: https://github.com/freebsd/freebsd-src

GitLab

- doc: https://gitlab.com/FreeBSD/freebsd-doc
- ports: https://gitlab.com/FreeBSD/freebsd-ports
- src: https://gitlab.com/FreeBSD/freebsd-src

## A.2.7. 邮件列表

在FreeBSD项目中，关于 git 的一般使用和问题的主要邮件列表是 freebsd-git。更多细节，包括提交信息列表，请参见邮件列表章节。

## A.2.8. SSH主机密钥

- gitrepo.FreeBSD.org host key fingerprints:
  - ECDSA key fingerprint is `SHA256:seWO5D27ySURcx4bknTNKlC1mgai0whP443PAKEvvZA`
  - ED25519 key fingerprint is `SHA256:lNR6i4BEOaaUhmDHBA1WJsO7H3KtvjE2r5q4sOxtIWo`
  - RSA key fingerprint is `SHA256:f453CUEFXEJAXlKeEHV+ajJfeEfx9MdKQUD7lIscnQI`
- git.FreeBSD.org host key fingerprints:
  - ECDSA key fingerprint is `SHA256:/UlirUAsGiitupxmtsn7f9b7zCWd0vCs4Yo/tpVWP9w`
  - ED25519 key fingerprint is `SHA256:y1ljKrKMD3lDObRUG3xJ9gXwEIuqnh306tSyFd1tuZE`
  - RSA key fingerprint is `SHA256:jBe6FQGoH4HjvrIVM23dcnLZk9kmpdezR/CvQzm7rJM`

这些也作为 SSHFP 记录在 DNS 中公布。
