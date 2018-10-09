---
layout: post
title: "用Jekyll在Github搭建属于自己的静态博客"
author: "骆小喵"
categories: learning
tags: [learning]
feature-img: "assets/img/article/jekyll.jpeg"
thumbnail: "assets/img/article/jekyll.jpeg"
---

#### 一、搭建本地Jekyll环境
```
使用gem安装Jekyll
$ gem install jekyll

使用Jekyll创建博客仓库
$ jekyll new blog

进入blog目录 开启Jekyll服务
$ cd blog
$ jekyll serve
```
Jekyll服务默认端口是4000，打开浏览器，输入：[http://localhost:4000](http://localhost:4000)就能看到一个简单的博客页面。

#### 二、Jekyll的一些常用命令
```
当前文件夹中的内容将会生成到 ./_site 文件夹中。
$ jekyll build

当前文件夹中的内容将会生成到目标文件夹<destination>中。
$ jekyll build --destination <destination>

指定源文件夹<source>中的内容将会生成到目标文件夹<destination>中。
$ jekyll build --source <source> --destination <destination>

当前文件夹中的内容将会生成到 ./_site 文件夹中，查看改变，并且自动再生成。
$ jekyll build --watch

一个开发服务器将会运行在 http://localhost:4000/
$ jekyll serve

功能和`jekyll serve`命令相同，但是会脱离终端在后台运行。
如果你想关闭服务器，可以使用`kill -9 1234`命令，"1234" 是进程号（PID）。
如果你找不到进程号，那么就用`ps aux | grep jekyll`命令来查看，然后关闭服务器。
$ jekyll serve --detach

```
#### 三、Jeykll的目录结构
```
├── _config.yml  			(配置文件)
├── _drafts  				(drafts（草稿）是未发布的文章)
|   ├── begin-with-the-crazy-ideas.textile
|   └── on-simplicity-in-technology.markdown
├── _includes 			(加载这些包含部分到你的布局)
|   ├── footer.html
|   └── header.html
├── _layouts 			    (包裹在文章外部的模板)
|   ├── default.html
|   └── post.html
├── _posts 				  (这里都是存放文章)
|   ├── 2007-10-29-why-every-programmer-should-play-nethack.textile
|   └── 2009-04-26-barcamp-boston-4-roundup.textile
├── _site 				(生成的页面都会生成在这个目录下)
├── .jekyll-metadata	  (该文件帮助 Jekyll 跟踪哪些文件从上次建立站点开始到现在没有被修改，哪些文件需要在下一次站点建立时重新生成。该文件不会被包含在生成的站点中。)
└── index.html 		   (网站的index)
```
#### 四、最后一些链接
###### 1. 主题网站，喜欢哪个下载下来改改CSS就可以用了
[Jekyll主题网站](http://jekyllthemes.org/)
###### 2. 冰霜之地大神的博客
[如何快速给自己构建一个温馨的"家"——用 Jekyll 搭建静态博客](https://halfrost.com/jekyll/)
