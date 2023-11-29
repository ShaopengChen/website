+++ 
draft = false
date = 2023-05-30T17:41:58+08:00
title = "Hugo + Github Pages搭建个人网站"
description = ""
slug = ""
authors = []
tags = []
categories = []
externalLink = ""
series = []
+++

# Hugo 搭建

* 环境：Ubuntu 20.04LTS
* 平台：Github Pages

## 安装 Hugo
```bash
$ sudo apt install hugo
```

## 创建网站
```bash
$ hugo new site website
```
执行完成后会生成一个website文件夹

## 添加 Hugo 主题
选择一个你喜欢的Hugo主题，如hugo-coder，克隆到themes目录。
```bash
$ cd website/themes
$ git clone https://github.com/luizdepra/hugo-coder.git
```
## 创建文章
```bash
$ hugo new content/posts/1.md
```

## 启动hugo服务
```bash
$ hugo server
```
浏览器访问localhost:1313，即可查看本地搭建的网站。

# Github Pages 建站

## 本地生成静态网站
```bash
$ cd website
$ hugo
```
生成的网站文件都存放在public文件夹中
## 推送到GitHub仓库
需要先创建个人站点的GitHub仓库（yourname.github.io）,并建立远程分支main。
```bash
$ cd public
$ git init
$ git add .
$ git commit -m "descriptions"
$ git push origin main
```
完成之后，打开网页yourname.github.io即可查看。