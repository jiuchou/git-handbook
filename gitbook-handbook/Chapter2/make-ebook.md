# 2.3.制作电子书

## 1.环境准备

* Windows下载：[Download calibre ](https://calibre-ebook.com/dist/win32)

1.下载安装calibre

2.安装`ebook-convert`

```bas
npm install -g ebook-convert
```

## 2.操作说明

执行`gitbook build`命令构建书籍，默认将生成的静态网站输出到 _book 目录。

指定build目录：`gitbook build [书籍路径] [输出路径]`

生成 PDF 格式的电子书

```bash
gitbook pdf ./ ./mybook.pdf
```

生成 epub 格式的电子书

```bash
gitbook epub ./ ./mybook.epub
```

生成 mobi 格式的电子书

```bash
gitbook mobi ./ ./mybook.mobi
```

