---
title: 对于git的理解与总结
author: FTH
tags: git
categories: git
type: "git"
date: 2018-04-23 18:30:00
---
已经自学了一年多关于前端这块，发现触及的方方面面实在是太多，有太多需要学习。
一直有知道github这个东东但是不知道怎么用，所以废话不多说了 跟着大表哥**（[B站up表严肃](https://www.bilibili.com/video/av17603446)）**一起学习git的知识吧！

----------
# 安装git
这个直接度娘git直接下载就可以了，使用的话window直接右键就有bash，就是个dos小黑框

# 敲命令吧
虽然有图形化的，但是还是多敲敲代码为好,其中的利害不再赘述。
## 首先我们要设置好邮箱和昵称
``` 
$ git config --global user.name "FaithGit"                
$ git config --global user.email "你的邮箱地址"
```
## 初始化
``` 
$ git init xxx  //新建一个xxx文件夹的初始文件夹
```
里面有个隐藏文件夹，我们所有的版本控制都在那个目录里
## 怎么吃上“💊后悔药”
如何建立节点。（因为是看了表严肃的教程视频所有对他的理解已经根深蒂固了，而且也很形象，很符合自己。）
在进行了一波自己的骚操作，我想你已经准备好建立一个节点控制了吧
``` 
$ git add . ||针对某个文件 单独加入暂存区
$ git commit -m "对自己的描述"
```
## **可以去吃💊后悔药了**
   ### 历史记录
假设有了很多后悔药可以去吃了，如何去查看自己有的药呢
``` 
$ git log --all --oneline --graph  //图像化显示一行历史
```
这个无非就是自己了解下后缀有什么效果
![Alt text](http://p7mx7a48u.bkt.clouddn.com/git.png)

> 我们从上向下解读一下框框起来的含义
 > - **粉色框** :指针指向master
 > - **蓝色框** :branch 分支名
 > - **黄色框** :💊后悔药的描述
 > - **粉色框** :💊后悔药的唯一id
----------
   ### 切换节点
你知道哪里有问题了就要吃药了，那么我们可以用
``` 
$ git checkout ****** 后悔药的唯一ID
```
不知道怎么吃后悔药也没有关系
``` 
$ git checkout -  退回一个节点
```
## 给你的💊药加上特殊的标记
在某些比较有重大意义的时刻，我们可以给💊药丸加上tag标注
``` 
$ git tag -a 标签名 -m"描述" 身份id
$ git tag  //罗列所有tag
$ git show tag名称  //显示tag名称的信息
```
# 创建分支吧！
嘿嘿有事要早点回去了，以后再补吧！
``` 
$ git branch 分支名
$ git checkout -b 分支名 //一句话创建并指向分支
$ git merge 分支名 合并分支
```
# 上传github库
``` 
$ git remote add 远程名字 远程地址
$ git remote -v 
$ git push 远程名字 分支 //上传github库
```
# 克隆远程库
``` 
$ git clone 地址
```
# 更新
``` 
$ git pull //获取远程更新
```