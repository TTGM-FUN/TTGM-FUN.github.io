---
title: 我经常犯的错误 IndexError list index out of range
layout: post
tags:
- python
- code
---

LearnEngish Bug 记录:

我经常犯的错误，主要是太粗心。

运行又这样了！超出列表范围!

```bash
Traceback (most recent call last):
  File "startPlay.py", line 46, in <module>
    mainSeeWordList()
  File "startPlay.py", line 24, in mainSeeWordList
    pygame.mixer.music.load('soundFile/' + wordList[wordNumber] + '.wav')
IndexError: list index out of range
```

查看一下代码：

```python
wordNumber = random.randint(0, len(wordList))
```

len(wordList) 长度是20,randown随机数是0, 20。就是这里错了。下标是从0开始计数好吧！真是太粗心了!

修改为:

```
wordNumber = random.randint(0, (len(wordList) -1))
```












