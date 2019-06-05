---
title: SONY VAIO VGN-UX17 触摸屏校准 for linux
layout: post
tags:
- testing
---

SONY VAIO 已经很老的机型了，平时在家里都是做无线路由的。只是最小化安装的Gentoo，并没有安装桌面。老妈买了Google Wifi 所以 VAIO 被淘汰了。

那我就拿来折腾了，（老妈说我这是折腾）。格式化，分区，重新安装全功能 Gentoo 哈哈！可是安装好后进入桌面后麻烦来了，触摸屏可以使用就是触摸笔定位不正确，差一点半点也就算了，差将近1厘米啊。。 好了，我们就开始使用xinput 校准吧:)

步骤1:  运行 xinput list 查找触摸屏ID 

```bash
$ xinput list
```

是这个: GUNZE USB Touch Panel  ID 11

步骤2:  运行xinput list 11 查看X,Y坐标 0:1023之间


```bash
$ xinput list 11
```

步骤3:  运行 xinput test 11 用触摸笔测试X,Y。从左上角开始 如显示35:44, 逐个测试4个角，记住坐标 ctrl+c 退出.

```bash
$ xinput test 11

```

步骤4:  把记住的4个点用命令微调，直到对齐

```bash
$ xinput set-prop 11 "Evdev Axis Calibration" 35 986 44 986
```

步骤6：复制并创建配置文件

```bash
$ cp -R /usr/share/X11/xorg.conf.d/ /etc/X11/
$ vim /etc/X11/xorg.conf.d/99-calibration.conf

```

添加以下

```bash
Section "InputClass"
Identifier "calibration"
MatchProduct "GUNZE USB Touch Panel"
Option "Calibration" "35 986 44 986"
EndSection
```

OK! 

```bash
# reboot
```
