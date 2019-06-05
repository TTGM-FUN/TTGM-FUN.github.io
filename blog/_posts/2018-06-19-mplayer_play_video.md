---
title: Mplayer 使用技巧
layout: post
tags:
- code
- pyhon
- c language
- java
- rails
- ruby
- linux command
---

使用 Mplayer 播放 youtube 视频

```bash
$ mplayer -fs -cookies -cookies-file /tmp/cookie.txt $(youtube-dl -gf 34 --cookies /tmp/cookie.txt "https://www.youtube.com/watch?v=b_ZWBJhrMOs")
```

使用mplayer录制在线视频

```bash
$ mplayer $(youtube-dl -g "https://www.youtube.com/watch?v=b_ZWBJhrMOs") -dumpstream -dumpfile output.mp4
```

mplayer 指定声卡输出

```bash
$ mplayer test.mp3 -ao alsa:device=hw=1.0
```

mplayer终端下播放视频

```bash
$ mplayer test.mp4 -vo fbdev
```
