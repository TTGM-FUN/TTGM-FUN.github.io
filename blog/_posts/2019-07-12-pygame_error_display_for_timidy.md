---
title: 自己动手解决的pygame error
layout: post
tags:
- Python
- Linux
---

今天在家修改前几天自己写的一个Python小游戏，想起再添加一个背景音乐就好了。

```bash
gameOverSound = pygame.mixer.Sound('endGameover.wav')
pygame.mixer.music.load('srartBackground.mid')
```
问题来了，运行后却显示以下错误：

```bash
pygame.error: /etc/timidity.cfg: No such fileor directory
```

我学Python写的一些小程序出现错误的时候，基本都是妈妈在旁边一步一步引导我查找错误修正错误的，这次她不在我能自己完成修改这个错误吗？

其实我也算是资深Linux用户了，时间和我的年龄一般大。但我没怎么学Linux只是会点基本的命令。因为我们家的Linux桌面始终是黑黑的一大片(terminal)，不会命令什么也做不了！

那看到这个错误提示，我首先想到的是etc目录一般都是放的程序配置文件，后缀名为cfg的肯定是配置文件了！那timidity就不是pygame里的模块什么的。我就使用命令搜索了一下果然timidity是一个midi播放器。果断安装

```bash
$ aptitude install timidity
```

问题解决了，可以顺利播放背景音乐了。好开心！

Python 的错误提示真是很好，错误的行数和错误类型很清晰明了，我喜欢！


