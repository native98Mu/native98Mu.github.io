---
layout: post
title: 对话框发出的一个请求，模型要回答需要哪些步骤
subtitle: 为什么同一个模型能同时处理多个请求
cover-img: /assets/img/cover-llm-api.png
# cover-img: /assets/img/path.jpg
# thumbnail-img: /assets/img/thumb.png
# share-img: /assets/img/path.jpg
tags: [LLM, API]
author: Muji
---



缘起新人培训时候的一位同学，在培训会上问了一个问题：模型训练好推理时都是固定的，为什么同一个模型在调用时候同时段可以处理不一样的问题，输出不同的答案？同时和朋友吃饭的时候，他也正好在问大模型是怎么根据不同人输入的文字生成不同回答的。

这里正好就先写下用户在对话框中输入文字发送后，对应的模型是如何处理的过程。

大致可以分为 3 个阶段：

1. 输入的预处理：这里一般会有 4 个部分的操作
- 分词（Tokenization）：也就是 tokenization 的部分，输入的文字会被模型对应的分词器切分成单字或者是字词样的token。而每个分词器都有一个预先定义的词汇表，对应token会映射成一个 token id。比如说“你是谁”，使用Qwen分词器后的字词序列就是["你","是"]，对应的token id就是

- 特殊符号拼接：一般会在输入的文字序列前加上system 
prompt，以及前后对应的特殊 tokens，比如开始，结束，角色类型（system，user等）；比较典型的就是 Qwen3 混合推理，是否开启思维链就能够通过特殊 token 模板控制

- 向量化（Embedding）：每个 tokenid 都对应一个高维向量，包含着字词的一些语意信息。比如说这些向量是模型在训练过程中学习到的。

- 位置编码：为了让模型知道每个字词在序列中的前后关系，还需要添加位置编码向量，让模型能够理解“你是谁”，和“谁是你”是不同的意思。



2. 推理生成：这就是常说的模型计算过程，中间部分典型的都是 transformer：

输入的文本会

3. 输出


