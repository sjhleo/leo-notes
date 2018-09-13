# 创建一本书

## 初始化

GitBook可以设置一个样板书：

>$ gitbook init

如果您希望将书籍创建到一个新目录中，可以通过运行 gitbook init ./directory 这样做。

## 构建

使用下面的命令，会在项目的目录下生成一个 _book 目录，里面的内容为静态站点的资源文件：

> $ gitbook build

## Debugging

您可以使用选项 --log=debug 和 --debug 来获取更好的错误消息（使用堆栈跟踪）。例如：

> $ gitbook build ./ --log=debug --debug

## 启动服务

使用下列命令会运行一个 web 服务, 通过 http://localhost:4000/ 可以预览书籍

> $ gitbook serve