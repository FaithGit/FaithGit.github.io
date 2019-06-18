---
title: 打造完美自用Ubuntu 18.04 开发环境，解决qq微信网易云
date: 2018-08-04 12:36:57
tags: Ubuntu
categories: Ubuntu
type: "Ubuntu"
header_image:
---
![我老婆不能挡住](http://image.fujs.top/ubuntu18.04-1-index.png)

唠叨几句：壁纸是新恒结衣，为canon代言，自己修改的字体用的也是canon字体；dock没动，纯粹仿造不如去买mac，省时省力；自用电脑是vn7一代的，坑爹的键盘加上没有指示灯，所以特意找到了大小写指示器，步骤下都会讲到；本来是记录在docx上，想想还是得经常用markdown来总结，用平台来分享自己的过程，方便自己今后寻着轨道快速到站。
<!-- more -->
## 下载Ubuntu
- **Ubuntu 18.04 desktop：http://releases.ubuntu.com/18.04/ubuntu-18.04.1-desktop-amd64.iso**
- **随便找个U盘，注意备份数据，用UltraISO打开镜像，再可入硬盘映像，一个启动盘就做好了**
- **因为ssd只是256G，所以未分区，C盘要共存win10与Ubuntu，建议用分区助手，把c盘无损划过来80个G**

## 快速安装Ubuntu
- **重启，选择刚做好的U盘的快速启动项，进入安装选项**
- **断网！选择第一项进入后，选择中文，最小安装，分区不用设，直接共存，虽然会有问题出现，但是不用管，这样最简单，出现的问题后续会提到**

## 进入系统设置

- **更新源咯，在软件和更新中，选择好最优服务器，顺便附加驱动里安装好N卡驱动，这个不再此篇幅介绍，**
![更新软件源](http://image.fujs.top/ubuntu18.04-1-soft.png)
- 然后一套combo: &ensp;`sudo apt-get update` 
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&nbsp;`sudo apt-get upgrade`

## 安装qq
教程源自http://tieba.baidu.com/p/5575480272?pid=118474764350&cid=0#118474764350

- 软件地址：https://pan.baidu.com/s/1pM6TgmB 密码: qwqr 
- 怎样打开64位 Ubuntu 的32位支持功能：https://blog.csdn.net/zjclugger/article/details/51395828 
- 双击或者拖到终端都打不开，那是缺库：`sudo apt install libgl1-mesa-glx:i386 libfreetype6:i386 `
- 就算打开，现在还是很丑的，没关系等我们安装完软件再美化 
![后台](http://image.fujs.top/ubuntu18.04-1-houtai.png)
[内容更新:2018年10月4日]
给qq添加快捷方式,详情请看下面的文章
https://blog.csdn.net/AKillWum/article/details/82940772
## 安装微信
这里我用了软件商店里的wechat 结果死活安装不上，还是找了网上的解决方案
>`sudo snap install electronic-wechat`

## 安装网易云
跟qq和微信一样，网上乱七八糟的骚操作太多了，我们就用最简单别人弄好的1.0.0的版本就行
>https://pan.baidu.com/s/1b8ZxfacW_cAsKLVelsKPmw
## 输入法
[内容更新:2018年10月4日]
搜索搜狗输入法下载linux版本,之后等待安装,然后回到所有应用程序找到输入法
![fix](http://image.fujs.top/ubuntu18.04-1-fix01.png)
使用fix输入法
![fix](http://image.fujs.top/ubuntu18.04-1-fix02.png)
我们每次按shift都会切换, 我只想要按ctrl+shift 才进入搜过输入法的话就禁用两侧shift
![fix](http://image.fujs.top/ubuntu18.04-1-fix03.png)
但是fix 有个配置不保存的问题,所以就需要一行代码搞定
>`sudo chown root:root ~/.config/fcitx/config`
## 解决后台
安装gnome-shell插件 TopIcons
1.在你学习如何使用 GNOME Shell 扩展之前，你应该安装 GNOME Tweak Tool。
>`sudo apt install gnome-tweak-tool`

2.如果你不想费神，你只需获得这个包，你就可以安装 8-10 个 GNOME 扩展。
>`sudo apt install gnome-shell-extensions`

此时你就多了个应用
![优化工具](http://image.fujs.top/ubuntu18.04-1-youhua.png)
如果你这两步都完成了，打开将会看到
![extensions有的包](http://image.fujs.top/ubuntu18.04-1-app.png)
3.我已经都安装好了，所以你如果是第一次安装的话，把上图3个打开
4.现在我们去逛逛装插件的市场
>https://extensions.gnome.org/

但是为了安装 Web 浏览器扩展，你需要两件东西：浏览器附加组件和本地主机连接器。
5.浏览器附加组件（反正我被墙了，所以我用Firefox）

- **[chrome插件](https://chrome.google.com/webstore/detail/gnome-shell-integration/gphhapmejobijbbhgpjhcjognlahblep)**
- **[Firefox插件](https://addons.mozilla.org/en-US/firefox/addon/gnome-shell-integration/)**

6.本地主机连接器
>`sudo apt install chrome-gnome-shell`

![本地主机连接器](http://image.fujs.top/ubuntu18.04-09png)
这样只要打开开关就能安装插件了
本人自用：
- **[TopIcons](https://extensions.gnome.org/extension/495/topicons/) (显示后台)**
-**[Openweather](https://extensions.gnome.org/extension/750/openweather/)(天气预报)**
-**[Lock-keys](https://extensions.gnome.org/extension/36/lock-keys/)(大小写提示)**
-**[Netspeed](https://extensions.gnome.org/extension/104/netspeed/)(网速显示)**

##自用样式
本篇幅不介绍如何美化，详情转载[点我点我](https://blog.csdn.net/zyqblog/article/details/80152016)
![我的样式](http://image.fujs.top/ubuntu18.04-1-style.png)

~~## 截图~~

~~我在用qq的时候 发现自带的截图挺好用的，但是一旦鼠标失焦，就不会出发截图，可见这样的“局部”截图是很影响使用的。~~
~~所以我们要装上[deepin-scrot](https://www.sohu.com/a/141591389_812245)~~
~~注意了 如果是双屏的小伙伴 第二个屏幕是不能截图截进去的!~~

## 截图 
[内容更新:2018年10月3号]

由于deepin-scrot 截图双屏只能截图一个,而且截图起来,一直有蓝边的情况,所以只能另找其他出路,爬文了一会便找到了替代方法,用自带的截图gnome-screenshot,截图好剪切板直接可以用,想要保存到本地那就有很多方法了不说明了.
- 打开系统设置->键盘
- 点击最下面的+号
![命令为gnome-screenshot -ac](http://image.fujs.top/ubuntu18.04-1-screenshot.png)
设置完毕,值得一提的是每次使用还会有快门声~
## 磁盘只读
这就是Ubuntu与win10共存出现的问题，虽然没有好好去研究各种分区，或者还有其他复杂的操作，但是出现这个问题是因为
>在window关闭时应该用重启进入ubuntu，而不是通过关机后进入ubuntu。重启进入的话，grub引导模式才会将系统权限交给ubuntu。如果是关闭后进入ubuntu的话，在ubuntu系统下没有操作系统的权限，只有只读系统权限。

所以这个问题，我们只要预防好就行，实在不行进windows重启进Ubuntu就行了

## 后记
Ubuntu 字体舒服排版好看，虽然一定存在着各种问题，但是能一一解决的话还是很有满足感的，贴进Linux开发，对上线一些小网站还有有所帮助的

---------
*自己使用整理收集，如有侵权 请联系删除!*