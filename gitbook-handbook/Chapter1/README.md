# 1.安装

* 参考：[Setup and Installation of GitBook](https://github.com/GitbookIO/gitbook/blob/master/docs/setup.md)
* 前提：nodejs+npm

1.环境准备(基于Windows7)

软件环境如下：

```bash
d:\book>node -v
v10.13.0

d:\book>npm -v
6.4.1
```

2.安装GitBook：`npm install -g gitbook-cli`

说明: `npm install -g gitbook`为老版本的安装命令，最新安装命令参考官方文档 [Setup and Installation of GitBook](https://github.com/GitbookIO/gitbook/blob/master/docs/setup.md)

```bash
d:\book>npm install -g gitbook-cli
XXX\nodejs\node_global\gitbook -> XXX\nodejs\node_global\node_modules\gitbook-cli\bin\gitbook.js
+ gitbook-cli@2.3.2
added 578 packages from 672 contributors in 29.007s

d:\book>gitbook --version
CLI version: 2.3.2
GitBook version: 3.2.3
```
