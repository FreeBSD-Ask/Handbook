# 本书中使用的一些约定

为了提供一致的、易于阅读的文本，全书遵循了几个惯例：

## 排版规则

_斜体_

首次使用文件名、网址、强调文字和技术术语时都使用 _斜体_。

`等宽`

错误信息、命令、环境变量、ports 名称、主机名、用户名、组名、设备名称、变量和代码片段使用`等宽`字体。

**粗体**

**粗体**字用于应用程序、命令和按键。

## 用户输入

按键用**粗体**显示，以便从其他文本中脱颖而出。要同时输入的组合键在键之间用“+”表示，例如：

`Ctrl`+`Alt`+`Del`

意味着用户应该同时输入`Ctrl`、`Alt`和`Del`键。

要依次输入的键会用逗号隔开，例如：`Ctrl+X，Ctrl+S`：

`Ctrl+X, Ctrl+S`

意味着用户应该同时输入`Ctrl`和`X`键，然后再同时输入`Ctrl`和`S`键。

## 示例

以 **C:>** 开头的例子表示 MS-DOS® 命令。除非另有说明，这些命令可以在现代 Microsoft® Windows® 环境中的“命令提示符”窗口中执行。

```shell-session
C:\> tools\fdimage floppies\kern.flp A:
```

以 _#_ 开头的例子表示在 FreeBSD 中必须以超级用户身份调用的命令。你可以以 root 身份登录来输入命令，或者以你的正常账户登录并使用 [su(1)](https://www.freebsd.org/cgi/man.cgi?query=su&sektion=1&format=html) 来获得超级用户的权限。

```shell-session
# dd if=kern.flp of=/dev/fd0
```

以 % 开头的例子表示应该从普通用户账户调用的命令。除非另有说明，用于设置环境变量和其他 shell 命令使用 C shell 语法。

```shell-session
% top
```
