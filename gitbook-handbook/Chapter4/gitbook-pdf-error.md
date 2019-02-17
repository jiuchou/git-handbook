# 4.2.gitbook pdf报错

1.报错信息

```bash
d:\book>gitbook pdf .
info: 7 plugins are installed
info: 6 explicitly listed
info: loading plugin "highlight"... OK
info: loading plugin "search"... OK
info: loading plugin "lunr"... OK
info: loading plugin "sharing"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 10 pages
info: found 11 asset files

EbookError: Error during ebook generation: 'ebook-convert' is not recognized as an internal or external command,
operable program or batch file.
```

2.原因分析

GitBook在生成PDF的过程中使用到calibre的转换功能，没有安装calibre或安装了calibre没有配置环境变量都会导致转换PDF失败

3.解决方案

参考[制作电子书](../Chapter2/make-ebook.md),安装calibre后，转换成功。

注意：安装calibre后需要重新启动命令行窗口

