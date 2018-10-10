---
title: 新建一个hexo+git
date: 2018-03-07 12:51:43
tags: hexo
categories: hexo
type: "hexo"
---

欢迎来到我的个人博客
===================

这是我第一次使用hexo+git的方式去创建一个个人的博客，之前从未深入git和markdown这些软件和写文章的方法，这篇文章主要讲述从零到逐步完善我的hexo+next主题的博客之旅，日后再建能够有所帮助。
因为是第一篇文章就多说点，首先最开心的就是域名了！
**f5cc.cc**，在[GoDaddy](https://sg.godaddy.com) 💰32 ，域名本身并没有什么含义只是短和好记罢了

----------
# 搭建
只要百度一下hexo+git关键词，就基本上都有了，还有那种什么大量优化的集合，我觉得也没必要弄得那么精致，毕竟只是个记录的工具。
但是值得注意的一些不一样的，可能是版本不对下面我举个例子

## next主题配置文件，menu菜单区别
``` 
menu:
  home: / || home #首页
  #about: /about/ || user
  tags: /tags/ || tags #标签
  categories: /categories || th #分类
  archives: /archives/ || archive #归档

```
上面是一个我这个版本的一个开启nav的配置代码，百度上的就不会有||之后的代码了，||之后的代码主要用来显示图标的，如果你删除了就缺失图标了。

##  🤯表情包
表情包我真是花费了好多时间，hexo官网说支持
> **Markdown Support:** **All** features of GitHub Flavored Markdown are **supported**. You can even use most Octopress plugins in Hexo.

试了很久都不行，然后去问qq群里面的大神们，给我了一些插件去安装，表情是可以的，但是都是图片格式还能放大。。
附上QQ群号 **287306637**  
 潜水酱油很多牛人也多的非常热闹的群


最后附上我的**解决方案**
😂就是这个 **[emojipedia](https://emojipedia.org/ "emjoy")**
直接用来复制粘贴，轻松便捷，无需任何插件。