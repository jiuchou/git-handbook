# 2.1.基本使用

步骤总览：

1. 使用 `gitbook init`初始化书籍目录
2. 使用 `gitbook serve`编译预览书籍



详细步骤：

1.使用 `gitbook init`初始化书籍目录，生成目录结构

```bash
d:\book>gitbook init
warn: no summary file in this book
info: create README.md
info: create SUMMARY.md
info: initialization is finished

d:\book>dir
2018/12/16 周日  18:37    <DIR>          .
2018/12/16 周日  18:37    <DIR>          ..
2018/12/16 周日  18:37                16 README.md
2018/12/16 周日  18:37                40 SUMMARY.md
               2 个文件             56 字节
               2 个目录 82,731,745,280 可用字节
```

文件说明

README.md 和 SUMMARY.md 是两个必须文件。README.md 是对书籍的简单介绍，SUMMARY.md 是书籍的目录结构。

2.定义目录结构，修改SUMMARY.md内容如下

```bash
d:\book>type SUMMARY.md 
# SUMMARY

* [Chapter1](chapter1/README.md)
  * [Section1.1](chapter1/section1.1.md)
  * [Section1.2](chapter1/section1.2.md)
* [Chapter2](chapter2/README.md)
```

使用 `gitbook init`，创建 SUMMARY.md 中的目录结构。

```bash
d:\>cd book

d:\book>gitbook init
info: create chapter1/README.md
info: create chapter1/section1.1.md
info: create chapter1/section1.2.md
info: create chapter2/README.md
info: create SUMMARY.md
info: initialization is finished

d:\book>dir
2018/12/16 周日  18:43    <DIR>          .
2018/12/16 周日  18:43    <DIR>          ..
2018/12/16 周日  18:43    <DIR>          chapter1
2018/12/16 周日  18:43    <DIR>          chapter2
2018/12/16 周日  18:37                16 README.md
2018/12/16 周日  18:43               192 SUMMARY.md
               2 个文件            208 字节
               4 个目录 82,731,651,072 可用字节
```

3.编译预览

执行`gitbook serve`编译和预览书籍

```bash
$ gitbook serve
Press CTRL+C to quit ...

Live reload server started on port: 35729
Starting build ...
Successfully built!

Starting server ...
Serving book on http://localhost:4000
```

说明: `gitbook serve` 命令实际上会首先调用 `gitbook build`编译，完成以后打开一个 web 服务器，默认监听在本地的 4000 端口。

指定端口号

```bash
gitbook serve --port 8888
```

