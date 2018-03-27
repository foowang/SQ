## GitBook 入门教程

#### 本书参考如下三篇文章整理而成，并且有所修改:

1.在线阅读：https://www.gitbook.com/book/yuzeshan/gitbook-studying/details
2.在线阅读：http://www.chengweiyang.cn/gitbook/
3.http://gitbook.site/setup.html

> GitBook 是一个基于 [Node.js](https://nodejs.org/en/) 的命令行工具，可使用 [Github](https://github.com/)/Git 和 [Markdown](http://www.markdown.cn/) 来制作精美的电子书，GitBook 并非关于 Git 的教程。

本文将简单介绍如何安装、编写、生成、发布一本图书，并附带介绍一些插件和其他注意事项。

##### GitBook支持输出多种文档格式：

- 静态站点：GitBook默认输出该种格式，生成的静态站点可直接托管搭载Github Pages服务上；

- PDF：需要安装gitbook-pdf依赖；

- eBook：需要安装ebook-convert；

- 单HTML网页：支持将内容输出为单页的HTML，不过一般用在将电子书格式转换为PDF或eBook的中间过程；

- JSON：一般用于电子书的调试或元数据提取。
