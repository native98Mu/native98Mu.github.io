---
layout: post
title: 为什么模型结构都在转MOE
subtitle: 和 Dense 相比 MOE 到底变了什么？
cover-img: /assets/img/cover-llm-api.png
# cover-img: /assets/img/path.jpg
# thumbnail-img: /assets/img/thumb.png
# share-img: /assets/img/path.jpg
tags: [LLM, MOE]
author: Muji
---

## MOE 原理


- 为什么会选择 MOE 模型？
    - 对于dense模型更大的参数量，在达到相同期望损失时cost更低，但是推理阶段消耗更多；但如果是moe，训练cost更低，推理时也少 （虽然显存加载更多，但激活参数少）
- MOE 特点：
    - 相同计算代价下，网络参数规模更大，性能更好
    - 基本可以达到相同参数规模的dense模型性能
    - 相比同参数dense模型，计算cost变小，显存不变
    - 可能有专家负载不均衡问题，训练难度高
- MOE结构做了怎样的改变？


MOE 主要对前向网络做改变，DENSE是FCNN先升维，再降维的映射（两个线性层）；MOE是中间分为多个子FCNN家模块，前置增加一个路由模块，选择该token会走向的专家模块权重：如图，假设路由模块概率top2选择了专家1和3，那么就会经过这两个子专家模块，之后专家权重加权求和得到输出层向量

需要注意的是专家选择是**对每个 token 做选择的**



专家网络链路：前向传播时对输入形状做修改，从batchsize*sequence_length*hidden_size变为 token数量*hidden_size，之后经过路由线性模块和softmax，转化成每个专家的选择权重；之后选择topk个专家的index和权重，并重新归一化

MOE层链路：放置n个专家网络和一个路由层，一个batch的sequence进来，做前向传播，得到对应专家和权重，之后相加求和得到moe层对应的输出

