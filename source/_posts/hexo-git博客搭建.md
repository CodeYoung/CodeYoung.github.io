---
title: hexo-git博客搭建步骤
top: 1
tags:
	-博客
	-学习
---
工作了快6年了，几次都想写写博客总结一下，今天终于走出第一步了，第一篇就来总结一下利用hexo,git搭建个人博客主要步骤。因为之前已经在github上Fork了一个仓库用于博客，所以，本文就不再写关于Fork博客仓库的内容。


## 软件环境准备

### 安装node.js,git

我用的win10，直接去官网下载[node.js](http://nodejs.cn/download/)和[git](https://git-scm.com/download/win)安装即可。


### 搭建环境

  新建blog文件夹（因为是用的MAC双系统，我直接新建该文件在WIN10系统的C盘），在blog文件夹下新建blog_data文件夹。进入blog_data文件夹并打开git bash使用命令：
hexo init初始化hexo。初始化成功后打开_config.yml配置hexo(如下两张图片):
	{% asset_img 图片一.png 替换作者名称 %}
	{% asset_img 图片二.png 配置github信息 %}
进入自己的github，选择用于博客的仓库，新建一个分支Hexo(可取其他名称)并复制Master分支的内容，并把Hexo设置为默认分支。然后把该分支(Hexo)克隆到新建的blog文件夹，进入克隆的xxx.github.io文件夹,利用命令git branch可看到当前分支为Hexo。把blog_data的里面的文件全复制到xxx.github.io里面。

### 写博客

打开文件夹xxx.github.io/source/_posts,新建一个xxx.md进行新的博客撰写。并打开git bash使用命令:
hexo g生产静态文件；
hexo d提交静态文件到master分支；
打开博客主页可发现已经更新到最新的博客


### 更新源文件

上面一个步骤已经更新了github上面博客的静态页面，但是我们需要把源文件也更新到github的Hexo分支。所以打开git bash，进入xxx.github.io文件夹，利用命令：
	git add .
	git commit '说明'
	git push origin Hexo
同步博客的源文件，以便于在其他地方也能下载最新的博客源文件进行更新


