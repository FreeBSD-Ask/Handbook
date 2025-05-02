# A.3.使用 Subversion

### A.3.1. 介绍

截至 2020 年 12 月，FreeBSD 使用 git 作为存储所有 FreeBSD 源代码和文档的主要版本控制系统。从 git 存储库中的 stable/11，stable/12 和相关的 releng 分支导出的更改被导出到 Subversion 存储库。这种导出将持续到这些分支的生命周期结束。从 2012 年 7 月到 2021 年 3 月，FreeBSD 使用 Subversion 作为存储所有 FreeBSD ports 的唯一版本控制系统。截至 2021 年 4 月，FreeBSD 使用 git 作为存储所有 FreeBSD ports 的唯一版本控制系统。

|  | Subversion 一般是开发人员工具。用户可能更喜欢使用 freebsd-update （“FreeBSD Update”）来更新 FreeBSD 基本系统，以及 git （“使用ports ”）来更新 FreeBSD ports 。在 2021 年 3 月之后，Subversion 仅用于传统分支（ stable/11 和 stable/12 ）。|
| -- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

本部分演示了在 FreeBSD 系统上安装 Subversion 并使用它创建 FreeBSD 存储库的本地副本。还包括有关使用 Subversion 的其他信息。

### A.3.2. Svnlite

一个轻量级版本的 Subversion 已经作为 svnlite 安装在 FreeBSD 上。只有在需要 Python 或 Perl API，或需要更新版本的 Subversion 时，才需要 port 或 软件包版本的 Subversion。

与普通的 Subversion 使用的唯一区别是命令名称是 svnlite。

### 安装

如果 svnlite 不可用或需要完整版本的 Subversion，则必须安装它。

Subversion 可以从 Ports 安装：

```sh
# cd /usr/ports/devel/subversion
# make install clean
```

Subversion 也可以作为一个软件包安装：

```sh
# pkg install subversion
```

### 运行 Subversion

要将源文件的干净副本抓取到本地目录中，请使用 svn。该目录中的文件称为本地工作副本。

|  | 在首次使用 checkout 之前，移动或删除现有的目标目录。对现有的非 svn 目录进行检出可能会导致现有文件与从存储库中带来的文件发生冲突。|
| -- | ----------------------------------------------------------------------------------------------------------------------------------- |

Subversion 使用 URL 来指定存储库，格式为 protocol://hostname/path。路径的第一个组件是要访问的 FreeBSD 存储库。有三个不同的存储库，base 用于 FreeBSD 基本系统源代码，ports 用于 Ports ，doc 用于文档。例如，URL <https://svn.FreeBSD.org/base/head/> 指定了 src 存储库的主分支，使用 https 协议。

从给定存储库执行检出的命令如下：

```sh
# svn checkout https://svn.FreeBSD.org/repository/branch lwcdir
```

 在哪里：

* 存储库是项目存储库之一： base，ports 或 doc。
* 分支取决于所使用的存储库。ports 和 doc 主要在 head 分支上进行更新，而 base 在 head 下维护最新版本的-CURRENT，以及相应的-STABLE 分支的最新版本在 stable/11 （11.x）和 stable/12 （12.x）下。
* lwcdir 是指应将指定分支的内容放置的目标目录。通常为 /usr/ports 对于 ports，/usr/src 对于 base，以及 /usr/doc 对于 doc。

此示例使用 HTTPS 协议从 FreeBSD 仓库签出源树，并将本地工作副本放置在 /usr/src。如果 /usr/src 已经存在但不是由 svn 创建的，请记得在签出前重命名或删除它。

```sh
# svn checkout https://svn.FreeBSD.org/base/head /usr/src
```

由于初始签出需要下载远程仓库的完整分支，可能会花一些时间，请耐心等待。

初次检出后，可以通过运行以下命令来更新本地工作副本：

```sh
# svn update lwcdir
```

要更新上面示例中创建的 /usr/src，请使用：

```sh
# svn update /usr/src
```

更新速度比检出快得多，只传输已更改的文件。

通过 Makefile 提供 /usr/ports、/usr/src 和 /usr/doc 目录中的 /usr/src，/usr/ports 的本地工作副本的更新方法。设置 SVN_UPDATE 并使用 update 目标。例如，要更新 /usr/src：

```sh
# cd /usr/src
# make update SVN_UPDATE=yes
```

### A.3.5. Subversion 镜像站点

FreeBSD Subversion 仓库是：

```sh
svn.FreeBSD.org
```

这是一个使用 GeoDNS 选择适当后端服务器的公开访问镜像网络。要通过浏览器查看 FreeBSD Subversion 仓库，请使用 <https://svnweb.FreeBSD.org/。>

HTTPS 是首选协议，但需要安装 security/ca_root_nss 包以自动验证证书。

### A.3.6. 了解更多信息

关于使用 Subversion 的其他信息，请参阅名为《Subversion 版本控制》的“Subversion 书”或 Subversion 文档。
