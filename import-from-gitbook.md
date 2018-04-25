# 从 GitBook 仓库 / GitLab Wiki 导入到语雀

语雀可以支持从 GitBook 仓库 / GitLab Wiki 直接导入数据了哦！

> 👹 NOTE: 想反过来，将语雀的数据导出到 GitBook，请阅读：[导出语雀文档为 GitBook 格式的本地文件](export-to-gitbook)


## 功能特点

* 完整支持从 GitBook 迁移到语雀，支持 `SUMMARY.md` 变为语雀的自定义目录；
* 支持从 GitLab Wiki 导入到语雀（需要自行编辑目录），请确定 GitLab Wiki 上的内容是 Markdown 编写，并且能在 GitLab Wiki 上正确浏览；
* 理论上支持任意类型的 Git 仓库（里面含有 `\*.md`, `\*.markdown` 文件的）导入到语雀；
* 只支持 Markdown 的文档迁移，其他格式暂时不行。


**几个已经导入好的例子**

* [Crystal Book](https://yuque.com/opensource-books/crystal-book)
* [Rust 程序设计语言](https://yuque.com/opensource-books/trpl-zh-cn)


## 安装
### macOS 安装

我们开发了一个叫 **gitbook2lark** 的小工具，可以方便你导入数据到语雀。

确保你的 macOS 已经安装了 [Homebrew](https://brew.sh/)，然后使用 [Homebrew](https://brew.sh/) 安装 gitbook2lark

```bash
$ brew update
$ brew tap yuque/homebrew https://github.com/yuque/homebrew.git
$ brew install gitbook2lark

Updating Homebrew...
==> Installing gitbook2lark yuque/homebrew
==> Downloading https://github.com/yuque/gitbook2lark/releases/download/0.3.0/gitbook2lark-darwin-amd64.zip
######################################################################## 100.0%
🍺  /usr/local/Cellar/gitbook2lark/0.3.0: 3 files, 726.3KB, built in 1 second
```

于是你就有了 **gitbook2lark** 工具了。

### Windows 安装
[https://github.com/yuque/gitbook2lark/releases](https://github.com/yuque/gitbook2lark/releases)

下载并解压获得 gitbook2lark.exe，请启动 CMD 来执行，这个程序是一个命令行工具。

### Linux 安装
[https://github.com/yuque/gitbook2lark/releases](https://github.com/yuque/gitbook2lark/releases)

下载并解压，将 `gitbook2lark` 放入 `/usr/local/bin/` 下

## 使用方法

在使用前，请适当看一下 gitbook2lark (Windows 用户是 gitbook2lark.exe)的帮助信息：

```bash
$ gitbook2lark -h
NAME:
   gitbook2lark - 将 GitBook 的仓库导入到语雀的文档仓库里面。

USAGE:
   gitbook2lark [global options] command [command options] [arguments...]

VERSION:
   0.3.0

COMMANDS:
     help, h  Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --host value              目标空间域名，不同企业空间需要设定域名，默认: https://yuque.com
   --token value, -t value   你的语雀个人账号私钥，或配置环境变量 LARK_TOKEN [$LARK_TOKEN]
   --source value, -s value  GitBook 源的 Git 仓库 URL 地址, 例如: https://github.com/foo/bar.git
   --output value, -o value  需要导入的目标仓库的路径，例如: lark/help
   --help, -h                show help
   --version, -v             print the version
```

1. 从你的[语雀个人设置页面](https://lark.alipay.com/settings/privateToken)找到 `TOKEN` 信息。
2. 在语雀上手工创建好一个空的仓库，用于接收导入的数据。


### 迁移 GitBook

```bash
$ gitbook2lark -t "kskskks" -s https://github.com/KaiserY/rust-book-chinese.git -o lark/rust-book-chinese
```

然后就会开始导入了。

### 迁移 GitLab / GitHub Wiki

自从 0.2.0 版本开始，这个工具也可以支持将 GitLab Wiki 了哦！

以这个仓库为例：

* [https://github.com/moby/moby/wiki](https://github.com/moby/moby/wiki)


打开上面的链接，你可以看到:

![屏幕快照 2018-01-08 14.20.40.png | left | 510x142](https://lark-assets-prod.oss-cn-hangzhou.aliyuncs.com/2018/png/f6ad6292-bace-4eaa-8a52-7506e7241ba8.png "")



然后我们可以:

```bash
$ gitbook2lark -t "kskskks" -s https://github.com/moby/moby.wiki.git -o moby/moby-wiki
```

## 升级

我们可能会持续优化这个工具，你只需要执行 `brew upgrade` 就可以升级到最新版本。

```bash
$ brew upgrade gitbook2lark
```

## 更新历史

### 0.4.1

* 修正 `--host` 参数不是 HTTPS 协议导致的一系列错误信息， 并自动修正非 HTTPS 的请求；
* 默认 <span style="background-color:rgb(250, 250, 250);"><span style="color:rgb(89, 89, 89);">`--host`</span></span> 改为 https://yuque.com


### 0.4.0

* 导入的时候会转换文档正文内指向其他内容的链接（相对链接）到正确的路径；
* 当发现知识库不存在时，将会自动创建；
* 当 Token 不正确的时候给出提示信息；
* 改进其他错误提示信息；


### 0.3.1

* 修正 `--host` 参数缺少默认值的问题;


### 0.3.0

* 采用 Go 语言重新编写实现，避免环境依赖，开始支持 Windows、Linux 平台；
* 新增 `--host` 参数，以支持导入到企业空间域名下；
* 优化导入过程的打印信息；


### 0.2.3

* 修正文件路径 `\_` 字符被错误替换为 `-` 的问题。


### 0.2.2

* 修正目录里面文档 slug 包含多余的仓库前缀的问题；
* 不再将目录的缩进替换成 SoftTab，而是保持原有的，例如 Tab；


### 0.2.1

* 修正并发的实现，以达到真正并发创建文档，并发数量 50，效率大幅提升.


### 0.2.0

* 不再要求必须有 `SUMMARY.md`，以便于支持 GitLab 的 Wiki 导入；
* 当 title 无法解析出来的时候，用文件名作为 title；
* 增加 `.markdown` 扩展名的支持；


### 0.1.2

* 优化标题处理，正文里面去掉 Heading 1。


### 0.1.1

* 用并发的方式上传文档，提高导入效率。
* 执行结果日志输出优化。


### 0.1.0

* First release.


