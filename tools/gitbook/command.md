# GitBook 命令

这里主要介绍一下 GitBook 的命令行工具 gitbook-cli 的一些命令, 首先说明两点:

* gitbook-cli 和 gitbook 是两个软件
* gitbook-cli 会将下载的 gitbook 的不同版本放到 ~/.gitbook中, 可以通过设置GITBOOK_DIR环境变量来指定另外的文件夹

## 列出 gitbook 所有的命令

> gitbook help

## 输出 gitbook-cli 的帮助信息

> gitbook --help

## 生成静态网页

> gitbook build

## 生成静态网页并运行服务器

> gitbook serve

## 生成时指定gitbook的版本, 本地没有会先下载

> gitbook build --gitbook=2.0.1

## 列出本地所有的gitbook版本

> gitbook ls

## 列出远程可用的gitbook版本

> gitbook ls-remote

## 安装对应的gitbook版本

> gitbook fetch 标签/版本号

## 更新到gitbook的最新版本

> gitbook update

## 卸载对应的gitbook版本

> gitbook uninstall 2.0.1

## 指定log的级别

> gitbook build --log=debug

## 输出错误信息

>　gitbook builid --debug