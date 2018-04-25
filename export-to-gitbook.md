# 导出语雀文档为 GitBook 格式的本地文件

语雀可以支持将一个仓库的文档导出为 GitBook 的格式本地文件了哦！

> NOTE: 想反过来，将 GitBook 导入到语雀，请阅读：[从 GitBook 仓库 / GitLab Wiki 导入到语雀](import-from-gitbook)

## 功能特点

* 完整支持从语雀的一个仓库的文档导出成为一个 GitBook 的文件夹；

## 安装

### macOS

我们开发了一个叫 __lark2gitbook__ 的小工具，可以方便你导出语雀的文档数据。

确保你的 macOS 已经安装了 [Homebrew](https://brew.sh/)，然后使用 [Homebrew](https://brew.sh/) 安装 lark2gitbook

```bash
$ brew update
$ brew tap yuque/homebrew https://github.com/yuque/homebrew.git
$ brew install lark2gitbook

Updating Homebrew...
==> Installing lark2gitbook from yuque/homebrew
==> Downloading https://github.com/yuque/lark2gitbook/releases/download/1.0.0/lark2gitbook-darwin-amd64.zip
######################################################################## 100.0%
🍺  /usr/local/Cellar/lark2gitbook/1.0.0: 3 files, 5.4MB, built in 4 seconds
```

于是你就有了 __lark2gitbook__ 工具了。

### Windows

[https://github.com/yuque/lark2gitbook/releases](https://github.com/yuque/lark2gitbook/releases)

下载并解压获得 `lark2gitbook.exe`，请启动 CMD 来执行，这个程序是一个命令行工具。

```bash
C:/> lark2gitbook.exe -h
```

### Linux

[https://github.com/yuque/lark2gitbook/releases](https://github.com/yuque/lark2gitbook/releases)

解压并执行：

```bash
$ sudo mv lark2gitbook /usr/local/bin/
```

## 使用方法

在使用前，请适当看一下 lark2gitbook 的帮助信息：

> Windows 用户请启动 CMD，`lark2gitbook.exe` 是一个命令行程序，下面的地方请注意替换到对应的路径。

```bash
$ lark2gitbook -h
NAME:
   lark2gitbook - 语雀仓库导出为 GitBook 格式

USAGE:
   lark2gitbook [global options] command [command options] [arguments...]

VERSION:
   1.0.0

COMMANDS:
     help, h  Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --host value              目标空间域名，不同企业空间需要设定域名，默认: https://yuque.com
   --token value, -t value   你的语雀个人账号私钥，或配置环境变量 LARK_TOKEN [$LARK_TOKEN]
   --source value, -s value  需要导出的仓库的路径，例如: yuque/help
   --output value, -o value  导出文件保存路径，例如: ./output 或 ~/Downloads/mybook
   --help, -h                show help
   --version, -v             print the version
```

1. 从你的[语雀个人设置页面](https://lark.alipay.com/settings/token)找到 `TOKEN` 信息。
2. 你也可以设置 `LARK_TOKEN=xxxx` 的环境变量，避免每次都输入 `--token` 参数；

### 导出

```bash
$ lark2gitbook -t "kskskks" -s yuque/help
```

然后就会开始导入了，最后文件会导出到当前目录的 `./output` 里面。

## 升级

我们可能会持续优化这个工具，你只需要执行 `brew upgrade` 就可以升级到最新版本。

```bash
$ brew update && brew upgrade lark2gitbook
```

## 更新历史

### 1.0.1

* 修正 `--host` 参数的默认值；

### 1.0.0

* 新增 `--host` 参数，以支持企业空间的域名。
* 优化打印信息，用中文提示。

### 0.1.0

* 修正导出的 .md 文档缺少文档标题的问题；
* 支持 `LARK_TOKEN` 环境变量作为 token;

### 0.0.1

* First release.

