## Node.js简介及安装

**安装gitbook前必须先安装node。**

什么是nodejs?

> Node.js 是一个基于 Chrome V8 引擎的 JavaScript 运行环境。 
Node.js 使用了一个事件驱动、非阻塞式 I/O 的模型，使其轻量又高效。 
Node.js 的包管理器 npm，是全球最大的开源库生态系统。

脚本语言需要一个解析器才能运行，JavaScript是脚本语言，在不同的位置有不一样的解析器，如写入html的js语言，浏览器是它的解析器角色。而对于需要独立运行的JS，nodejs就是一个解析器。

每一种解析器都是一个运行环境，不但允许js定义各种数据结构，进行各种计算，还允许js使用允许环境提供的内置对象和方法做一些事情。如运行在浏览器中的js的用途是操作DOM，浏览器就提供了document之类的内置对象。而运行在nodejs中的js的用途是操作磁盘文件或搭建http服务器，nodejs就相应提供了fs,http等内置对象。

### 安装步骤

1. 下载对应你系统的Node.js版本：https://nodejs.org/en/
2. 选安装目录进行安装
3. 环境配置
4. 测试
5. 注意事项

#### 安装

1、2两步在官网下载之后直接下一步安装即可，建议勾上
![默认Add to PATH](images/GitBook1.1.0.png)

当安装完成后，打开CMD窗口进行简单测试是否安装成功
![nodejs版本，npm版本](images/GitBook1.1.1.png)

当现实上面窗口即表明nodejs安装成功，因为安装的是新版nodejs，npm也会一起安装。

#### 环境配置

说明：这里的环境配置主要配置的是npm安装的全局模块所在的路径，以及缓存cache的路径，之所以要配置，是因为以后在执行类似：npm install express [-g] （后面的可选参数-g，g代表global全局安装的意思）的安装语句时，会将安装的模块安装到【C:\Users\用户名\AppData\Roaming\npm】路径中，占C盘空间。

例如：我希望将全模块所在路径和缓存路径放在我node.js安装的文件夹中，则在我安装的文件夹【D:\SQ\node\nodejs】下创建两个文件夹【node_global】及【node_cache】

创建完两个空文件夹之后，打开cmd命令窗口，输入

```
npm config set prefix "D:\SQ\node\nodejs\node_global"
npm config set cache "D:\SQ\node\nodejs\node_cache"
```

当不想使用上述设置，只需删除.npmrc文件即可(默认在用户根目录下)

进入环境变量对话框，在**【系统变量】**下新建【NODE_PATH】，输入【D:\SQ\node\nodejs\node_global\node_modules】，将**【用户变量】**下的【Path】修改为【D:\SQ\node\nodejs\node_global】

#### 测试

配置完后，安装个module测试下，我们就安装最常用的express模块，打开cmd窗口，
输入如下命令进行模块的全局安装：

```
npm install express -g     # -g是全局安装的意思
```

#### 注意事项

##### 更改注册表源

国内用户在npm上经常安装不上包，大部分原因是被wall了，导致根本没法使用。而淘宝团队给出了[npm镜像](https://npm.taobao.org/)，我们可以将npm的注册表源改为此镜像解决npm中包无法install的问题。
 
1.临时使用：安装某个包时使用如下命令

```
$ npm --registry https://registry.npm.taobao.org install [packagename]
```
将[packagename]改为想要安装的包的名字即可。 

2.永久使用

```
npm config set registry https://registry.npm.taobao.org

// 配置后可通过下面方式来验证是否成功 

npm config get registry 
```

安装的包的依赖是否有无法下载的。这种不太好判断，可以在npm install命令后加一个-d或--verbose来显示详细信息，这样就可以看到是安装的哪一步除了问题。 
```
$ npm install webpack -g -d或$ npm install webpack -g --verbose
```
