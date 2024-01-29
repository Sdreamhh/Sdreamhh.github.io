---
title: 基于 GitHub Pages 和 Jekyll 的博客搭建
tags: [博客]
categories: [博客]
math: true #是否启用数学公式
image: #文章顶部的图片
   path: ../images/avatar.jpg
   alt: 我无比惊讶。
---

## 前言

这是基于**GitHub Pages**和**Jekyll**，以**[Chirpy](https://chirpy.cotes.page/)**为主题的个人博客搭建教程。在开始之前，需要安装以下软件：

- VScode：IDE
- [Git](https://git-scm.com/)：分布式版本控制系统
- [Jekyll](https://www.jekyll.com.cn/)：静态站点生成器

## 用GitHub创建一个新的站点

在GitHub中搜索**[Chirpy Starter](https://github.com/cotes2020/chirpy-starter)**，选择<kbd>Using this template</kbd>><kbd>Create a new repositiory</kbd>，将仓库命名为`username.github.io`。在仓库的文件列表中，选择<kbd>Code</kbd>，复制链接到VScode中，将项目克隆到本地。

在运行本地服务器之前，需要在根目录的终端输入：

```terminal
$ bundle
```

接着输入：

```terminal
$ bundle exec jekyll s
```

此时在浏览器的网址栏中输入[localhost:4000](localhost:4000)，就可以看到本地运行的网页了。

## 激活站点

在激活站点之前，需要更改一个文件。将`_config.yml`{: .filepath}中`url`一项改为本站点的地址，**注意，不管用户名有没有大写，必须全部为小写：**

```yml
url: username.github.io
```

在GitHub中，选择<kbd>Settings</kbd>><kbd>pages</kbd>，<kbd>Bulid and deployment</kbd>><kbd>Sourse</kbd>，选择<kbd>GitHub Actions</kbd>，发送一条日志。你可以在<kbd>Actions</kbd>中查看进度。当`pages-build-deployment`完成后，站点就部署成功了，此时可以通过[username.github.io]()访问你的站点。

## 个性化

### 基本信息

站点的个人基本信息可以在`_config.yml`{: .filepath}中设置，文件内部有详细的介绍。这里简单介绍几项重要的内容：

- `title`：主标题
- `tagline`：副标题
- `img_cdn`：文件路径前缀
- `avatar`：侧边栏头像
- `toc`：是否开启文章目录

### 设置网页图标

原文：[Link](https://chirpy.cotes.page/posts/customize-the-favicon/)

选择一张喜欢的图片作为网页图标，在[**Real Favicon Generator**](https://realfavicongenerator.net/)中选择<kbd>Select your Favicon image</kbd>上传图片，之后选择<kbd>Generate your Favicons and HTML</kbd>来生成图标，最后点击下载。

在`/assets/img`{: .filepath}中只需要将下载得到的文件替换掉整个文件夹就可以实现图标的转换了。如果没有该文件路径，自己创建一个。

## 写一篇文章

原文：[Link](https://chirpy.cotes.page/posts/write-a-new-post/)

首先是文章的标题。在命名`.md`文件时，需要按照`YYYY-MM-DD-文件名`的固定格式。接着在文件头写入：

```md
---
author: sbming
title: 基于 GitHub Pages 和 Jekyll 的博客搭建
date: 2023-06-05 19:48:00 +0800
tags: [博客] #标签
categories: [博客] #目录
math: true #是否启用数学公式
pin: false #是否置顶文章
---
```

之后就可以用MarkDown正常写文章了。 最后将`.md`文件插入到`/_posts`{: .filepath}中，实现文章的上传。

文章的书写格式原文：[Link](https://chirpy.cotes.page/posts/text-and-typography/)



