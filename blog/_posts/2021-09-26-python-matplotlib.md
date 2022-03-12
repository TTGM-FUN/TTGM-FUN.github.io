---
title: Python自动生成小组量化直方图
layout: post
tags:
- Python
- matplotlib
---

Example:

[![](/images/group_poster.png)](/images/group_poster.png)

- Code:

```python
#!/usr/bin/evn python3
# -*- coding: utf-8 -*-
"""
kongpengju.com
"""

import numpy as np
import matplotlib.pyplot as plt
plt.rcParams['font.sans-serif']=['Microsoft YaHei']

N = 6
groupMenbers = ('张XX', '王XX', '李XX', '赵XX', '钱XX', '孙XX') # 组员
groupMenberWin = (4, 10, 2, 4, 2, 4)  # 加分情况
groupMenberLose = (2, 4, 6, 2, 8, 2)  # 扣分情况
ind = np.arange(N)  
width = 0.28   

p1 = plt.bar(ind, groupMenberWin, width, color='#2eb872', label='Win', ec='black') # 颜色 #2eb872
p2 = plt.bar(ind + width, groupMenberLose, width, color='#fa4659', label='Lose', ec='black') # 颜色 #fa4659

plt.ylabel('Scores')
plt.title('X组第X周成长足迹') # 周
plt.xticks(ind, groupMenbers)
plt.yticks(np.arange(0, 17, 2)) # 分数上限,只改17就行
plt.legend()

plt.savefig('group_poster.png')
plt.show()
```
