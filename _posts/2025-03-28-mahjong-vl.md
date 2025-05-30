---
layout: post
title: 线下玩日麻怎么快速计算点数
subtitle: 麻将机 or 软件？
cover-img: /assets/img/mahjong_cover.png
# cover-img: /assets/img/path.jpg
# thumbnail-img: /assets/img/thumb.png
# share-img: /assets/img/path.jpg
tags: [VLM, OCR, 日麻]
author: Muji
---

周五晚朋友约线下日麻，很久没玩过麻将也很久没见过几位朋友，欣然赴约～

不论是玩日麻，川麻还是杭麻，逃不开的就是要算分，每次这种都是我的知识盲区，怎么算番，怎么加倍....
不过日麻好的一点的是，有在线计算器可以将牌型输进去计算好点数。但是每次在线输入牌型时候，还是会耽误一些时间（不要问为什么不学习下算点数...

这次是第一次线下玩日麻机器，发现有积分棒可以自动计算自己拥有的总分，立直时候还有音效！这时候就有考虑能否通过对麻将牌做标记来自动做计分，但是也需要考虑一些问题：

- 怎么区分庄家
- 怎么区分立直
- 怎么区分副露
- 怎么体现宝牌
- 怎么区分暗杠
...

要依靠麻将机自动做，肯定还是有些麻烦。当时觉得如果每个座位上能连一个类似touch bar的显示屏，能够自动标记庄，立直，宝牌，副露等信息，那么自然就完成了点数的计算。听起来这个就是直接把线下的牌转为线上计算，人工做点小辅助～

如果不对牌桌和麻将牌做大改造，针对目前手机上的点数计算器，能否通过拍照的形式直接记录，这至少比人工一个一个输入牌型来得简单。

比较理想的方式，是将胡牌的牌型整体 OCR 出来，然后自己标记**手牌**，**副露**，**宝牌**，**里宝**，额外的**场风**，**门风**等就可以直接用已有线上计算器形式。
![点数计算器](/assets/img/mahjong.png)

为了方便，这块儿使用通义千问视觉理解模型 Qwen-VL-max 和 Chatgpt-4o 做测试：
- 两个模型都能够较好的按照结构化要求输出，分清不同的花色
- 万牌，风牌，字牌有比较好的准确率
- 饼牌和索子准确率极低，模型无法正确理解这两种牌型的计数方式（可以理解视觉模型训练数据里这类麻将牌数据应该是比较少的，对于这个具体的任务使用 vl-3B/7B 的模型做微调应该就能够有不错的表现）


不过对比一看这个准确度，软件角度讲还是手动输入来的经济便捷。
以及最方便彻底的改造，还是牌桌厂来完成最合适。





