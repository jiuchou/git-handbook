# 4.1.gitbook init报错

## 问题1(Error: Shasum check failed)
1.报错信息

```bash
d:\book>gitbook init
Installing GitBook 3.2.3

Error: Shasum check failed for XXX\register.npm.taobao.org\glob-parent\download\glob-parent-2.0.0.tgz
Expected: xxxxxx
Actual:   xxxxxx
From:     xxxxxx
```

2.原因分析

公司网络隔离，使用代理无法正常获取GitBook安装包。
在具有类似软件环境(nodejs和npm相同版本)，具有良好网络的机器上，使用本教程安装GitBook，`gitbook init`可直接执行成功。

3.解决方案

Steps:

1.  `gitbook fetch`

2.  `gitbook init`

## 扩展

根据网络来源内容，除问题1外，gitbook init报错可能存在以下原因:

* [Error: Cannot find module 'gitbook-html'](https://github.com/GitbookIO/gitbook/issues/1792#issuecomment-299550649)
* [记坑爹的服务器端gitbook安装过程-太坑了](http://www.yanjuntech.cn/archives/2396)

