---
title: 用Python做一个基本的奥数题
layout: post
tags:
- math
- python
- code
---

有一个奇数，它是7的倍数，个位和十位上的数差是1，小于80。你知道它是哪个数吗？


```
普通的算法是： 这个数是21。

小于80的7的倍数一共有11个：7,14,21,28,35,42,49,56,63,70和77

其中奇数是：7,21,35,49,63和77。

接下来，我们只要找出哪个答案数位上的数值之差为1就行了。

7只有1位数，所以不对。

21可以是1-2 = -1。它也可能是2-1 = 1。它就是我们要找的正确答案了。

如果有兴趣，还可以算算其它的数：
3-5 = -2和5-3 = 2
4-9 = -5和9-4 = 5
6-3 = 3和3-6 = -3
7-7 = 0

再也没有数位值差是1的数了，所以只有21是正确答案。

让我们再检查一下，看看对不对：
21是7的倍数（3 * 7 = 21）
21是奇数
21的十位和个位上的数的差是1（2-1 = 1）
因此，21是正确的数字。
```

使用Python计算方法:

```python
numList = []
for i in range(80):
    if i % 7 == 0 and i % 2 == 1:
        numList.append(i)

for numListLen in range(len(numList)):
        numStrList = str(numList[numListLen])
        if len(numStrList) > 1:
            if int(numStrList[0]) - int(numStrList[1]) == 1:
                print(numStrList)
```
