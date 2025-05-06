---
layout: post
title: 大模型 API 调用时的参数都是什么意思
subtitle: 为什么同一个模型能输出不同的结果？
cover-img: /assets/img/cover-llm-api.png
# cover-img: /assets/img/path.jpg
# thumbnail-img: /assets/img/thumb.png
# share-img: /assets/img/path.jpg
tags: [LLM, API]
author: Muji
---

### 训练

训练时候模型会 random 一个初始态，一个句子正常是 predict next token，如果 predict 下一个 token 的tokenizer id 和真实的 word 不对应，模型会调整参数，让选择真实 word 的可能性提升，其他 words 的可能性降低


### 模型性能指标


1. latency （时延）
2. throughtput (吞吐量)
3. cost （成本）

### 推理过程
1. Transformer-based Decoder token 生成过程 （initial phase and autoregressive phase）

**假设 batchsize 为1**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/5a244f81-b50b-4d9c-869a-2215a9c30922/09dca31d-fa01-4754-a0b5-653eb25bac29/Untitled.png)

1. Loading the model weights to GPU
2. Tokenizing the prompt on CPU and transferring the token tensor to GPU （ sentence 会先经过 tokenizer 转变为 vector）

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/5a244f81-b50b-4d9c-869a-2215a9c30922/b87cd757-2a97-480f-8d7f-9dc5ba14088a/Untitled.png)

1. Generating the first token of the completion by running the tokenized prompt through the network （initiation phase/***pre-fill phase***）
2. Appending the generated token to the sequence of input tokens and using it as a new input to generate the second token of the completion. Then, repeat this process until either a stop sequence has been generated (e.g. a single end-of-sequence (EOS) token) or the configured maximum sequence length has been reached （***generation phase***, the ***decoding phase***, the *auto-regressive phase* or even the *incremental phase*.）

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/5a244f81-b50b-4d9c-869a-2215a9c30922/56d36a3a-b885-4401-944b-09e56a5547d9/Untitled.png)

1. Fetching the the completion’s tokens to CPU and detokenize them to get your generated text

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/5a244f81-b50b-4d9c-869a-2215a9c30922/2e1e5f7e-058e-4064-b216-8ea570d348ab/Untitled.png)

Decoder 自身不输出token，而是输出 logits；输出logits的最后一层通常被称为 LM head。最后需要从logits中推导token，通常会选择greedy decoding或者sampling decoding

take a sequence of tokens as input and return a corresponding output token are usually called an *execution engine* or an ***inference engine*.**