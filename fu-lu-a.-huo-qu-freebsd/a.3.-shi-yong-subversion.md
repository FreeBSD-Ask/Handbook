# A.3.使用 Subversion


## A.3.1. 介绍

截至 2020 年 12 月，FreeBSD 使用 git 作为存储所有 FreeBSD 源代码和文档的主要版本控制系统。从 git 存储库中的 `stable/11`、`stable/12` 和相关的 releng 分支导出的更改将被导出到 Subversion 存储库。这种导出将在这些分支的生命周期内继续进行。从 2012 年 7 月到 2021 年 3 月，FreeBSD 使用 Subversion 作为存储所有 FreeBSD Ports 的唯一版本控制系统。截至 2021 年 4 月，FreeBSD 使用 git 作为存储所有 FreeBSD Ports 的唯一版本控制系统。

> **注意**
>
> Subversion 通常是开发者工具。用户可能更喜欢使用 `freebsd-update`（[“FreeBSD Update”](https://docs.freebsd.org/en/books/handbook/cutting-edge/#updating-upgrading-freebsdupdate)）来更新 FreeBSD 基本系统，使用 `git`（[“Using the Ports Collection”](https://docs.freebsd.org/en/books/handbook/ports/#ports-using)）来更新 FreeBSD Ports Collection。自 2021 年 3 月以后，Subversion 的使用仅限于遗留分支（`stable/11` 和 `stable/12`）。

本节演示了如何在 FreeBSD 系统上安装 Subversion 并使用它创建一个 FreeBSD 存储库的本地副本。还包含有关使用 Subversion 的其他信息。

## A.3.2. Svnlite

FreeBSD 上已经安装了 Subversion 的轻量级版本，称为 `svnlite`。只有在需要 Python 或 Perl API，或者需要 Subversion 的较新版本时，才需要安装 Subversion 的 Port 或包版本。

与常规 Subversion 使用的唯一区别是命令名称为 `svnlite`。

## A.3.3. 安装

如果 `svnlite` 不可用或需要完整版本的 Subversion，则必须安装它。

可以从 Ports Collection 安装 Subversion：

```
# cd /usr/ports/devel/subversion
# make install clean
```

也可以将 Subversion 安装为一个包：

```
# pkg install subversion
```

## A.3.4. 运行 Subversion

要在本地目录中获取源代码的干净副本，请使用 `svn`。此目录中的文件称为*本地工作副本*。

> **警告**
>
> 在第一次使用 `checkout` 之前，移动或删除现有目标目录。在现有的非 `svn` 目录上执行 checkout 可能会导致现有文件与从存储库中带来的文件之间的冲突。

Subversion 使用 URL 来指定存储库，采用 _protocol://hostname/path_ 的形式。路径的第一个组件是要访问的 FreeBSD 存储库。有三个不同的存储库，`base` 用于 FreeBSD 基本系统源代码，`ports` 用于 Ports Collection，`doc` 用于文档。例如，URL `<a href="https://svn.freebsd.org/base/head/" class="bare">https://svn.FreeBSD.org/base/head/</a>` 指定了 src 存储库的主分支，使用 `https` 协议。

从给定存储库执行 checkout 的命令如下：

```
# svn checkout https://svn.FreeBSD.org/repository/branch lwcdir
```

其中：

- _repository_ 是 Project 存储库之一：`base`、`ports` 或 `doc`。
- _branch_ 取决于所使用的存储库。`ports` 和 `doc` 主要在 `head` 分支上进行更新，而 `base` 在 `head` 下维护了 -CURRENT 的最新版本，以及在 `stable/11`（11._x_）和 `stable/12`（12._x_）下维护了相应的最新版本。
- _lwcdir_ 是应将指定分支的内容放置的目标目录。通常是 `ports` 的 **/usr/ports**，`base` 的 **/usr/src**，以及 `doc` 的 **/usr/doc**。

此示例使用 HTTPS 协议从 FreeBSD 存储库中检出 Source Tree，将本地工作副本放置在 **/usr/src** 中。如果 **/usr/src** 已经存在但不是由 `svn` 创建的，请记得在 checkout 之前重命名或删除它。

```
# svn checkout https://svn.FreeBSD.org/base/head /usr/src
```

由于初始 checkout 必须下载远程存储库的完整分支，可能需要一些时间，请耐心等待。

在初始 checkout 后，可以通过运行以下命令更新本地工作副本：

```
# svn update lwcdir
```

要更新上面示例中创建的 **/usr/src**，请使用：

```
# svn update /usr/src
```

更新比 checkout 快得多，只传输已更改的文件。

在 checkout 后更新本地工作副本的另一种方法由 **Makefile** 提供在 **/usr/ports**、**/usr/src** 和 **/usr/doc** 目录中。设置 `SVN_UPDATE` 并使用 `update` 目标。例如，要更新 **/usr/src**：

```
# cd /usr/src
# make update SVN_UPDATE=yes
```

## A.3.5. Subversion 镜像站

FreeBSD Subversion 存储库是：

```
svn.FreeBSD.org
```

这是一个通过 GeoDNS 选择适当的后端服务器的公共可访问的镜像网络。要通过浏览器查看 FreeBSD Subversion 存储库，请使用 [https://svnweb.FreeBSD.org/](https://svnweb.freebsd.org/)。

HTTPS 是首选协议，但必须安装 **security/ca_root_nss** 包以自动验证证书。

## A.3.6. 获取更多信息

有关使用 Subversion 的其他信息，请参阅名为 [Version Control with Subversion](http://svnbook.red-bean.com/) 的“Subversion 书”或 [Subversion Documentation](http://subversion.apache.org/docs/)。
