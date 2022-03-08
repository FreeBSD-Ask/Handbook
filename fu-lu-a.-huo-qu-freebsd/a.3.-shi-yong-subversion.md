# A.3.使用 Subversion

## A.3.1.简介

从 2020 年 12 月起，FreeBSD 使用 git 作为主要的版本控制系统来存储所有 FreeBSD 的源代码和文档。在 stable/11, stable/12 和相关的 releng 分支上的 git repo 的改动会被导出到 subversion 仓库中。这种输出将持续到这些分支的生命周期。从 2012 年 7 月到 2021 年 3 月，FreeBSD 使用 Subversion 作为唯一的版本控制系统来存储所有 FreeBSD 的 Ports Collection。从 2021 年 4 月起，FreeBSD 使用 git 作为存储所有 FreeBSD Ports Collection 的唯一版本控制系统。

**Subversion 通常是一个开发者工具。用户可能更喜欢使用 freebsd-update (“FreeBSD Update”) 来更新 FreeBSD 基本系统，以及 portsnap (“使用 Ports Collection”) 来更新 FreeBSD Ports Collection。在 2021 年 3 月之后，subversion的使用只针对传统的分支(stable/11和stable/12)。**

这一节演示了如何在 FreeBSD 系统上安装 Subversion 并使用它来创建 FreeBSD 版本库的本地副本。还包括了关于使用 Subversion 的其他信息。

## A.3.2.Svnlite

一个轻量级的 Subversion 版本已经作为 svnlite 安装在 FreeBSD 上。只有在需要 Python 或 Perl API，或者需要较高版本的 Subversion 时，才需要移植或软件包版本的 Subversion。

与正常的 Subversion 使用的唯一区别是，命令的名字是 svnlite。

## A.3.3.安装

如果 svnlite 不可用或者需要完整版的 Subversion，那么必须安装它。

Subversion 可以从 Ports Collection 中安装。

`# cd /usr/ports/devel/subversion`
`# make install clean`

Subversion 也可以作为一个软件包来安装。

`# pkg install subversion`

## A.3.4. 运行Subversion

要获取一个干净的源代码拷贝到本地目录中，请使用 svn。这个目录中的文件被称为本地工作副本。

**在第一次使用签出之前，移动或删除现有的目标目录。在现有的非svn目录上进行签出会导致现有文件和从版本库带入的文件之间的冲突。**

Subversion 使用 URL 来指定一个版本库，其形式为`protocol://hostname/path`。路径的第一个组成部分是要访问的 FreeBSD 代码库。有三个不同的版本库，base 是 FreeBSD 基本系统的源代码，ports 是 Ports Collection，doc 是文档。例如，URL https://svn.FreeBSD.org/base/head/ 使用 https 协议指定了 src 代码库的主分支。

从一个给定的版本库中签出，可以用这样的命令进行。

`# svn checkout https://svn.FreeBSD.org/repository/branch lwcdir`

其中:

- 仓库是项目仓库中的一个：base、ports 或 doc。
- 分支取决于所使用的版本库。ports 和 doc 主要在 head 分支中更新，而 base 则在 head 下维护最新的 -CURRENT 版本，在 stable/11 (11.x) 和 stable/12 (12.x) 下维护各自的最新版本 -STABLE 分支。
- lwcdir 是指定分支的内容应被放置的目标目录。对于 ports 来说，这通常是 `/usr/ports`，对于 base 来说是 /usr/src，而对于 doc 来说是 `/usr/doc`。

这个例子使用 HTTPS 协议从 FreeBSD 版本库中签出源代码树，将本地工作拷贝放在`/usr/src`中。如果`/usr/src`已经存在，但不是由 svn 创建的，记得在签出前重命名或删除它。

`# svn checkout https://svn.FreeBSD.org/base/head /usr/src`

因为初始签出必须下载远程版本库的完整分支，所以可能需要一些时间。请耐心等待。

在初始签出后，可以通过运行本地工作副本来更新。

`# svn update lwcdir`

要更新上面例子中创建的`/usr/src`，请使用。

`# svn update /usr/src`

更新比结账要快得多，只传输有变化的文件。

另一种在签出后更新本地工作拷贝的方法是由 `/usr/ports`、 `/usr/src` 和 `/usr/doc` 目录中的 Makefile 提供的。设置 SVN_UPDATE 并使用更新目标。例如，要更新 `/usr/src`。

`# cd /usr/src`
`# make update SVN_UPDATE=yes`

## A.3.5.镜像网站

FreeBSD 的 Subversion 存储库是:

`svn.FreeBSD.org`

这是一个可以公开访问的镜像网络，使用 GeoDNS 来选择合适的后端服务器。要通过浏览器查看 FreeBSD Subversion 仓库，请使用 [https://svnweb.FreeBSD.org/](https://svnweb.freebsd.org/)。

HTTPS 是首选协议，但需要安装 security/ca_root_nss 软件包，以便自动验证证书。

## A.3.6.了解更多信息 

关于使用 Subversion 的其他信息，请参见`Subversion`，标题为 Subversion 的版本控制，或 Subversion 文档。

