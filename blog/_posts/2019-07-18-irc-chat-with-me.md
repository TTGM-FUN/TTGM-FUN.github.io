---
title: 如何使用IRC聊天
layout: post
tags:
- Linux
- irc
---

可能会有小伙伴好奇，会问为什么大家都用QQ和微信，你怎么用IRC聊天呢？我的回答是我妈妈不让我用！但是我也有QQ和微信的帐号只是在她手机上安装着。主要是接收学校老师布置的作业和通知的。

IRC是一个多用户、多频道的纯文本模式互动聊天系统。完全可以体现有事说事没事下线的原则。在这里乱说话的少之又少，因为服务器有历史记录、用户ip地址等。甚至都可以在网上搜到！(更多关于IRC如隐藏ip、安全加密等!我不感兴趣。你可以[在这里了解到更多](https://en.wikipedia.org/wiki/Internet_Relay_Chat),我只是使用它去学习)如果你只是学习或解决问题那么来吧，这里适合你。

- 网页版IRC

[![](/images/web_irc.png)](https://web.libera.chat/#Learn-Together)

只需点击[https://web.libera.chat/#Learn-Together](https://web.libera.chat/#Learn-Together)进入就可以了。可以不用注册只需输入Nick名就可以了，就是随便起一个用户名。没有注册的话就不用勾选I have a password 然后勾选I'm not a robot通过人机验证就可以START登录了。

- Windows 10 版IRC

[Weechat](https://weechat.org/)

[![](/images/pc_irc.png)](https://weechat.org/)

- Linux

```
aptitude install irssi
```

- 常用命令

注册：

```
/msg NickServ REGISTER 密码 电子邮件地址
```

验证密码：

```
/msg NickServ IDENTIFY 昵称 密码
```

验证后，换昵称加为额外的名:

```
/msg NickServ GROUP
```

改昵称：

```
/nick 新的昵称
```

查看某人资料：

```
/whois 昵称
```

查看所有频道里面的人的名单:

```
/who
```

加入频道:

```
/join #Learn_Together
```

在当前频道说话：

```
/say 要说的话
```

给某人发送悄悄话：

```
/msg 他的昵称 信息内容
```

查看留言列表：

```
/msg memoserv list
```

查看留言：

```
/msg memoserv read 留言号码
```

发送留言：

```
/msg memoserv send 对方妮称 留言内容
```

留言帮助：

```
/msg memoserv help
```

退出关闭聊天:

```
/quit
```

更多可以参考IRC帮助:

```
/help
```

小伙伴们还有什么问题吗？我也想不起有什么了，下次再说吧。


