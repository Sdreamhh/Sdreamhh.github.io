---
title: 基于GitHub Pages和Jekyll的博客搭建
date: 2023-06-05 19:48:00 +0800
tags: [博客]
categories: [博客]
math: true #是否启用数学公式
pin: false #是否置顶文章
image: #
   path: /avatar.jpg
   alt: 我无比惊讶。
---

## 前言

这是基于**GitHub Pages**和**Jekyll**，以**[Chirpy](https://chirpy.cotes.page/)**为主题的个人博客搭建教程。在开始之前,你需要安装以下几样东西:

- VScode: 好用的IDE
- [Git](https://git-scm.com/): 本地文件和GitHub仓库的实时更新
- [Jekyll](https://www.jekyll.com.cn/): 静态站点生成器

## 用GitHub创建一个新的站点

在GitHub中搜索**[Chirpy Starter](https://github.com/cotes2020/chirpy-starter)**,选择<kbd>Using this template</kbd>><kbd>Create a new repositiory</kbd>，将仓库命名为`username.github.io`。在仓库的文件列表中，选择<kbd>Code</kbd>，复制链接到VScode中，将项目克隆到本地。

在运行本地服务器之前，在根目录的终端中输入:

```terminal
$ bundle
```

然后再输入:

```terminal
$ bundle exec jekyll s
```

此时在浏览器中输入[localhost:4000](localhost:400),就可以看到在本地运行的网页了。

## 激活站点

在激活站点之前，需要更改一个文件。在`_config.yml`{: .filepath}中`url`一项改为自己站点的地址:

```yml
url: username.github.io
```

在GitHub中，选择<kbd>Settings</kbd>><kbd>pages</kbd>，<kbd>Bulid and deployment</kbd>><kbd>Sourse</kbd>，选择<kbd>GitHub Actions</kbd>，发送一条日志。你可以在<kbd>Actions</kbd>中查看进度。当`pages-build-deployment`完成后，站点就部署成功了，你可以通过[username.github.io]()访问你的站点。

