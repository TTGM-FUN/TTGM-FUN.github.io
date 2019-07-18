---
permalink: learn_code
layout: page
title: Learning Code.....
---

# 背单词

学习Python写的一个小程序。

- 可以利用这个小程序背单词。

- 需要安装Python pygame 模块。

- 单词列表是Think Python的第1.8章术语表。如果你需要背别的单词可以自己更换。

[关于LearnEnglish小程序语音库的问题](https://kongpengju.com/blog/2019/07/18/Python-learn-answers_01/)

使用方式:

```python
$ Python3 startPlay.py
```

音频采集的是真人自然发音，根据听到的声音输入单词，如果不知道什么单词会不同人循环发音。如果输入错误会提示错误，并显示正确答案。

![](/images/code_info.png)

```
wordlist.md  # 是单词列表
```

这些代码包含了字符串，列表及循环操作。根据学习情况正在不断完善。

下一步主要是修改bug和完善功能。

- 更换单词列表功能，通过输入文件名自动读取。

- 添加图片提示。

- 错误词反复练习。

- 还没想好。。。。。。。原先写了个自动采集音频的Shell脚本。还可以的，Python应该做这个还容易些。

好吧，就到这里吧，小伙伴们有什么问题或建议可以在IRC频道联系我 [Webchat With Me](https://webchat.freenode.net/#Learn_Together) 或Email。

项目地址: 

[https://github.com/kpjmark/learnenglish.git](https://github.com/kpjmark/learnenglish.git)

git：

```
$ git clone "https://github.com/kpjmark/learnenglish.git"
```
