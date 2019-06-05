---
title: Tesseract OCR文字识别，提取pdf文字
layout: post
tags:
- code
- 生活日记
- linux
---

星期日和同学去看电影回来后就发烧了，今天请了一天假在家休息。

过几天就围棋晋级考试了，在家里随便翻了下电脑里的围棋电子书，倒！发现真是好久没看了，不知不觉竟然收集有15G的围棋电子书，幸亏那时我已经分好类了，就挑了本中盘类的看。

这本是很老的书了，来自日本棋院的书，蜀艺出版社的。看了几页后慢慢进入状态了，这书写的真不错，但是越往后看越模糊，这书是扫描版的，后面扫描的字体竟然东缺一块西缺一块的，好在我有工具Tesseract, 它是2006年Google赞助开发的一个开源项目。可以被认为是当时最准确的开源OCR引擎之一。虽然它一直在我电脑里躺着，但我只用过最多这么5-6次吧，不止AlphaGo Master可以训练围棋，Tesseract也可以训练字库.就是训练Tesseract的文字识别能力。有兴趣的同学可以访问以下链接了解详情。具体用法在Git里也有介绍。

[Tesseract 维基百科](https://en.wikipedia.org/wiki/Tesseract_(software))

[https://opensource.google.com/projects/tesseract](https://opensource.google.com/projects/tesseract)

没有安装的同学可以git

```bash
git clone 'https://github.com/tesseract-ocr/tesseract.git'

```
