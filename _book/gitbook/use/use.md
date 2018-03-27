## GitBook基本使用

gitbook 的基本用法非常简单，基本上就只有两步：

1. 使用 gitbook init 初始化书籍目录
2. 使用 gitbook serve 编译书籍

### 初始化 GitBook
    
创建 mygitbook 文件夹，并切换到这个文件夹下面

```
gitbook init
```
然后会初始化GitBook目录，自动创建两个md格式的文件README.md和SUMMARY.md

- README.md - 项目的介绍都写在这个文件里，最上层(和SUMMARY.md同级)的是本书的Introduction。
- SUMMARY.md - GitBook 的目录结构在这里配置。

#### 定义目录结构

**两种方法**

在SUMMARY.md文件中定义目录结构有两种方法。

1. 先定义好目录结构，通过gitbook init自动生成目录结构对应的文件夹和Markdown文件。

2. 先创建好文件夹和Markdown文件再来编辑目录结构。

SUMMARY.md 的目录结构长什么样？ 看下面：

```
# Summary

* [Introduction](README.md)
* [GitBook入门教程](gitbook/README.md)
    - [1. 安装](gitbook/install/README.md)
        * [1.1 Nodejs简介及安装](gitbook/install/NodejsInstall.md)
        * [1.2 GitBook安装](gitbook/install/GitBookInstall.md)
    - [2. 使用](gitbook/use/use.md)
```

这个目录建好以后在根目录下执行命令：
```
gitbook init
```
那些没有的目录和文件都会被创建


### 启动服务

书籍目录结构创建完成以后，就可以使用 gitbook serve 来编译和预览书籍了：

```
gitbook serve
```
gitbook serve 命令实际上会首先调用 gitbook build 编译书籍，完成以后会打开一个 web 服务器，监听在本地的 4000 端口。如果编译有问题，会抛出错误信息。

用浏览器打开 http://localhost:4000/ 或 http://127.0.0.1:4000/ 查看显示书籍的效果。