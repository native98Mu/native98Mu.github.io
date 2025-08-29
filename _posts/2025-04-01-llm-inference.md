---
layout: post
title: 为什么同一个模型能同时处理多个请求
subtitle: 一个请求的回答推理过程是怎样的
cover-img: /assets/img/cover-llm-api.png
# cover-img: /assets/img/path.jpg
# thumbnail-img: /assets/img/thumb.png
# share-img: /assets/img/path.jpg
tags: [LLM, API]
author: Muji
---



缘起新人培训时候的一位同学，在培训会上问了一个问题：模型训练好推理时都是固定的，为什么同一个模型在调用时候同时段可以处理不一样的问题，输出不同的答案？

这里正好就可以写下用户在对话框中输入文字发送后，对应的模型是如何处理的过程。
首先是输入的文字会被转为 token id，也就是有个 tokenizer 的过程。
