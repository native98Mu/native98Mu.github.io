---
layout: post
title: 大模型 API 调用时的参数都是什么意思
subtitle: 他们都是如何影响模型回复结果的
cover-img: /assets/img/cover-llm-api.png
# cover-img: /assets/img/path.jpg
# thumbnail-img: /assets/img/thumb.png
# share-img: /assets/img/path.jpg
tags: [LLM, API]
author: Muji
---


许多B端客户在使用模型时，基本不会认真看 API 各个参数功能，仅按基准的demo就开始接入。使用过程对于模型 API 的参数含义也不是很了解，经常就会有各种问题。正好自己日常用得也比较多，就对一些常见参数做说明，方便后续理解～


（这块儿 DeepSeek API DOCS 就做得比较好，他们的 Curl 调用示例直接展示了所有可用的参数，非常适合做参数功能验证。）

```
curl -L -X POST 'https://api.deepseek.com/chat/completions' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
--data-raw '{
  "messages": [
    {
      "content": "You are a helpful assistant",
      "role": "system"
    },
    {
      "content": "Hi",
      "role": "user"
    }
  ],
  "model": "deepseek-chat",
  "frequency_penalty": 0,
  "max_tokens": 2048,
  "presence_penalty": 0,
  "response_format": {
    "type": "text"
  },
  "stop": null,
  "stream": false,
  "stream_options": null,
  "temperature": 1,
  "top_p": 1,
  "tools": null,
  "tool_choice": "none",
  "logprobs": false,
  "top_logprobs": null
}'
```

