# 2 GitBook安装及常用命令

使用npm安装GitBook的命令行工具：

```
npm install gitbook-cli -g -d
```

安装完成后查看GitBook的版本：

```
gitbook --version
```

更新GitBook的命令：

```
npm update gitbook-cli -g
```

卸载GitBook的命令：

```
npm uninstall gitbook-cli -g
```

本例中使用的是全局安装 GitBook 命令，还有一种安装方式是本地安装，两种方式有什么不同呢？

- 本地安装：安装包会被下载到当前所在目录，因此只能在当前目录下使用。
- 全局安装：安装包会被下载到到特定的系统目录下，安装包能够在所有目录
下使用。


**需要注意的是：**用户首先需要安装 nodejs，以便能够使用 npm 来安装 gitbook。