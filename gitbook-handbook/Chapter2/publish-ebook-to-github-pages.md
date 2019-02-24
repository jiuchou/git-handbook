# 2.5.发布到Github Pages（转载）

* 原文：
  * [使用github、travis、github pages自动构建发布gitbook页面（国内访问速度会比gitbook快很多）](https://www.jianshu.com/p/41478a0ea104)
  * [发布到Github Pages](https://einverne.github.io/gitbook-tutorial/publish/gitpages.html)

## 前言

[gitbook](https://gitbook.com)使用markdown语法进行写作，自动生成简单漂亮的文档页面，还有海量插件可以使用，并且公开文档都免费提供服务，
 使用起来很方便，有配套的软件，就算不懂代码的人用起来也非常简单。

但是有个缺点就是国内访问很慢，慢得连github的pages页面的速度都不如，而且不支持同步github组织的仓库，所以可以考虑将gitbook编译成静态页面发布到pages，
 而且希望整个发布过程都是自动的，我们自己后面该文档时要做的就只是写文档（直接文本编辑器或者gitbook编辑器都行），写完后提交推送到github，后面的构建、发布全都不用我们自己操作，都自动完成，于是可以用travis，travis对github十分友好，对于公开的仓库，travis也是免费的

## 将静态网站直接发布到Github Pages

可以将编写好的.md文件通过Gitbook处理成静态网站，然后发布到[Github Pages](https://pages.github.com/)上。

将md文件与Github Pages静态文件存放在一个仓库中。md文件为master分支，而html文件为 `gh-pages`分支。

下面将介绍使用一个仓库托管源码，而使用 Travis 自动将静态网站发布到 `gh-pages` 分支中。这样就可以避免提交源码的同时，还需要同步一遍 `gh-pages` 分支。

[domenic](https://gist.github.com/domenic/ec8b0fc8ab45f39403dd) 制作了一个脚本，当 master 分支更新时，自动使用 CI Travis 拉取更新，然后和 `gh-pages` 分支做比较，如果有差异了，自动将 master 分支的修改提交到 `gh-pages` 分支。

## 使用项目的Pages服务

除了上面的直接发布静态文件到Github Pages的方法以外，还可以使用一个单独的项目的Github Pages功能。

### 创建仓库与分支

1. 登陆到Github，创建一个新的仓库，名称我们就命名为`gitbook-tutorial`，这样我就得到一个`gitbook-tutorial`仓库
2. 克隆仓库到本地： `git clone git@github.com:/USER_NAME/gitbook-tutorial.git`
3. 创建一个新分支： `git checkout -b gh-pages`，注意，分支名必须为`gh-pages`
4. 使用 `gitbook build` 生成静态网页
   ```
   gitbook build
   ls | grep -v _book | xargs -i rm -rf {}
   mv _book/* .
   rm -rf _book
   ```
5. 将分支push到仓库： `git push -f origin gh-pages`
6. 切换到主分支：`git checkout master`

经过这一步处理，我们已经创建了`gh-pages`分支了，有了这个分支，Github会自动为你分配一个网址。

> [http://USERNAME.github.io/gitbook-tutorial](http://username.github.io/gitbook-tutorial)

你可以在项目页面右下角`setting`中看到：

![Github Pages](https://einverne.github.io/gitbook-tutorial/imgs/gh-pages-setting.png)

