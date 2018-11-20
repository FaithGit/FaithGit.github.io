---
title: 打造完美自用ubuntu(二)给AppImage qq添加快捷方式并添加到显示应用程序列表
date: 2018-10-04 21:50:19
tags: Ubuntu
categories: Ubuntu
type: "Ubuntu"
header_image: http://image.fujs.top/ubuntu18.04-2-index.png
---
![界面图](http://image.fujs.top/ubuntu18.04-2-index.png)
还是老规矩,先来一波新垣结衣(左下角就是我们要达到的效果)
## 5步走
### 在任意位置新建一个文件 重命名为xx.desktop
### `gedit xx.desktop`
### 在空白处添加
```
[Desktop Entry]
Name=QQ
Exec=/home/fu/桌面/DeepinQQ-20180228-x86_64.AppImage
Icon=/home/fu/图片qq.png           
Type=Application
StartupNotify=true
```
>注意复制的时候,存在换行符的,记得删除,如若不行,可重新敲打代码

`Name		快捷方式的名称`
`Exec			就是AppImage qq所在的文件路径`
`icon			就是要为其添加的图标`

### 保存文件后 右键属性,在权限目录下 **允许作为程序执行文件上**打钩
这个时候 文件就会变成
![qq图标](http://image.fujs.top/ubuntu18.04-2-qq.png)
### `sudo nautilus` 启动个无敌权限的文件夹 把刚刚的文件放到这个目录下
 /usr/share/applications
## icon下载
 6. 最后放上qq的icon 地址连接
 链接: https://pan.baidu.com/s/19vTQmSy8vI2BdQI7msiO7g 提取码: errr
 
## 完工
这样我们的qq快捷方式就创建完毕了,如果想要放在dock栏里就可以右键加入啦