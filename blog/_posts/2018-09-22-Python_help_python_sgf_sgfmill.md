---
title: Python sgf 库sgfmill 使转换gib 、ugi 等文件更方便了
layout: post
tags:
- code
- shell command
- linux
---

shell 脚本的批量转换和python各有利弊。但python更方便些。

例子:

*文件读取*

```python
from sgfmill import sgf
with open("foo.sgf", "rb") as f:
    game = sgf.Sgf_game.from_bytes(f.read())
winner = game.get_winner()
board_size = game.get_size()
root_node = game.get_root()
b_player = root_node.get("PB")
w_player = root_node.get("PW")
for node in game.get_main_sequence():
    print(node.get_move())
```

*详细请到*

[https://github.com/mattheww/sgfmill](https://github.com/mattheww/sgfmill)

[https://mjw.woodcraft.me.uk/sgfmill/doc/1.1.1/examples.html](https://mjw.woodcraft.me.uk/sgfmill/doc/1.1.1/examples.html)
