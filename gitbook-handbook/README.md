# 前言

GitBook 是一个基于 Node.js 的命令行工具，支持 Markdown 和 AsciiDoc 两种语法格式，可以输出 HTML、PDF、eBook 等格式的电子书。

GitBook 不是 Markdown 编辑工具，也不是 Git 版本管理工具。但 GitBook 又与 Markdown 和 Git 息息相关，因为只有将它们结合起来使用，才能将它们的威力发挥到极致。

因此，通常我们会选择合适的 Markdown 编辑工具以获得飞一般的写作体验；使用 GitBook 管理文档，预览、制作电子书；同时通过 Git 管理书籍内容的变更，并将其托管到云端（比如 GitHub、GitLab、码云，或者是自己搭建的 Git 服务器），实现多人协作。

GitBook的优势：

- 语法简单
- 兼容性强
- 导出方便
- 专注内容
- 团队协作

GitBook的劣势：

- 复杂排版，使用Word等工具更为方便。

## 支持格式

GitBook支持输出多种文档格式，如：

* 静态站点：GitBook默认输出该种格式，生成的静态站点可直接托管搭载Github Pages服务上；
* PDF：需要安装[ebook-concert](http://calibre-ebook.com/download)依赖；
* eBook：需要安装[ebook-concert](http://calibre-ebook.com/download)；
* 单HTML网页：支持将内容输出为单页的HTML，不过一般用在将电子书格式转换为PDF或eBook的中间过程；
* JSON：一般用于电子书的调试或元数据提取。

## Gitbook项目地址

* GitBook项目官网：[http://www.gitbook.io](http://www.gitbook.io/)
* GitBook Github地址：<https://github.com/GitbookIO/gitbook>
* toolchain <https://toolchain.gitbook.com/>

## 本项目地址

* 仓库：<https://github.com/jiuchou/gitbook-handbook>
* 在线阅读：
  * <https://hongfan.gitbook.io/gitbook-handbook/>
  * https://jiuchou.github.io/gitbook-handbook/

### 项目说明

大部分项目内容整理自网络，部分内容为原创。内容引用原地址包含但不限于：

* [GitBook plugin 文档](https://github.com/GitbookIO/plugin)
* [GitBook 文档](https://github.com/GitbookIO/gitbook)
* [GitBook 从懵逼到入门](https://blog.csdn.net/lu_embedded/article/details/81100704)
* [GitBook 简明教程](http://www.chengweiyang.cn/gitbook)
* [GitBook 使用教程](https://einverne.github.io/gitbook-tutorial/)

