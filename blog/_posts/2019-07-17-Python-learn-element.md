---
title: Python 查找列表元素的各种方法
layout: post
tags:
- Python
- Linux
- code
---

查找列表中出现最多的元素

- for 循环加计数器暴力查询

```python
def findToMore(seeItList): 
    boosNum = 0
    littleNum = seeItList[0] 
      
    for i in seeItList: 
        freeFind = seeItList.count(i) 
        if(freeFind > boosNum): 
            boosNum = freeFind 
            littleNum = i 
  
    return littleNum
  
seeItList = [2, 2, 1, 2, 3, 1] 
print(findToMore(seeItList)) 
```

- 列表法

```python
def findToMore(seeItList): 
    return max(set(seeItList), key = seeItList.count) 

seeItList = [2, 2, 1, 2, 3, 1]
print(findToMore(seeItList))
```
