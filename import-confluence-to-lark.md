# Confluence 迁移到语雀

> 👺 本文是针对 Confluence 5.4 的维护人员、IT 编写的，目前 Confluence 迁移只能支持他们来操作。


## 系统需求
* Confluence 5.4
* Confluence 的 MySQL 数据库配置信息
* macOS / Linux / Windows 命令行操作


## 功能
* 输入一个 Confluence 文档节点编号，自动将节点组织成为语雀的目录结构；
* 图片、附件自动迁移到语雀的服务里面；


## 下载安装
本工具是支持跨平台的，目前支持 macOS, Windows, Linux。

[https://github.com/yuque/confluence2lark/releases](https://github.com/yuque/confluence2lark/releases)

下载对应的平台，并解压。

## 使用方法

解压下载到的安装包，获得：

* confluence2lark 或 confluence2lark.exe
* confluence2lark.yml


打开 `confluence2lark.yml` 并参考你的 Confluence 的 MySQL 数据库配置信息修改，如：

```yml
database:
  # 数据库名称
  db: confluence
  # MySQL 服务器主机名或 IP
  host: localhost
  # MySQL 端口
  port: 3306
  # MySQL 用户名
  username: confluence
  # MySQL 密码
  password:
```

在使用前，请适当看一下 confluence2lark 的帮助信息，打开 “终端” （Windows 叫 CMD 或命令行），并执行：

> NOTE: Windows 是 `confluence2lark.exe`


```bash
$ confluence2lark -h
NAME:
   confluence2lark - 迁移 Confluence 的数据到语雀（通过直连数据库，仅支持 Confluence 5.4）

USAGE:
   confluence2lark [global options] command [command options] [arguments...]

VERSION:
   1.0.0

COMMANDS:
     help, h  Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --token value, -t value        语雀个人账号的 PrivateToken
   --group value                  导出目标语雀组的路径，如果没有组，请先手工到语雀创建组（并确保 Token 对应的账号有这个组的 Owner 权限）\
                                      ，例如 https://yuque.com/foo，这里就填 foo
   --id value                     Confluence 内容 pageId，将基于这个页面将作为语雀知识库，子页面的内容将作为文档 (default: 0)
   --concurrency value, -c value  并发数量，最大支持 20（受 ulimit 限制，如果需要更大请修改 ulimit -n 1000） (default: 10)
   --mode value, -m value         已有数据处理方式 1. 更新 0. 忽略（效率更高） (default: 1)
   --host value                   目标空间域名，不同企业空间需要设定域名，默认: https://yuque.com
   --help, -h                     show help
   --version, -v                  print the version
```

> 🔒 关于 --token 参数，你可以在 [语雀个人设置页面](/settings/token) 找到你的个人账号 Token 信息。
> ⚠️ 注意：企业空间下，请使用该企业空间下的个人账号 Token，两者是不一样的。


## 迁移

先在语雀上创建好一个团队，并确保你有这个团队的 `Owner` 权限，例如我们创建一个路径为 `cf-demo` 的团队。

```markup
$ confluence2lark --token "kskskks" -id 1215086 --group cf-demo
验证云雀 Token 有效性...[ok]
目标组: cf-demo
PageID: 1215086
并发量: 20

查询原始 MySQL 数据...[ok]
准备目标仓库...[ok]
查询原始 MySQL 的子文档列表数据（根据内容量不同可能需要不少时间）[此阶段中断不影响数据]
  正在查询第 0 层... [ok] 9 条 158.339287ms
  正在查询第 1 层... [ok] 6 条 159.70098ms
  正在查询第 2 层... [ok] 0 条
    组织树形结构第 0 层... [ok] 7.722µs

[查询成功] 一共 15 条记录
开始导入文档到语雀................[ok]
更新 Toc...[ok]
将文档有关的 11 人加入到组里面 ..............[ok]

==== Done ===
```

最后可以访问 [https://yuque.com/cf-demo](https://yuque.com/cf-demo) 查看刚才迁移成功的仓库。

## 常见问题
1. 由于两个系统使用了不同的文档内容格式，confluence2lark 是在迁移的时候会试着转换格式，但不保证一定能准确。当出现格式问题的时候，请尝试手工解决。工具主要是解决内容迁移的问题，细节还得自己处理。


## 更新历史
### 1.0.1
* 修正附件转移存储的域名不正确的问题；
* 默认主机名改为 [https://yuque.com；](https://yuque.com;/)

### 1.0.0
* 首次对外发布；


