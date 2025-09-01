---
layout: post
title: Google Storybook 来了解西方神话故事方便吗
subtitle: 每个人的绘本制作工具

tags: [Product, tools, LLM, text2image]
author: Muji
---

最近，谷歌新推出的 Storybook 工具吸引了我的注意。这款工具能根据用户需求快速生成图文并茂的绘本故事。作为一个对新产品充满好奇心的人，最近正好想了解西方神话故事，我立刻想到一个问题：它能否成为我了解西方神话故事的便捷工具？


于是就开始尝试使用这个工具，看看效果如何。

### 一句话生成宙斯的故事
我的第一次尝试非常直接，只用一句话来描述我的需求：
"
我想要了解希腊神话宙斯的故事，包含他的生平和主要故事线，希望你使用插画风格为我绘制故事书
"
Storybook 的交互界面非常直观，左侧是对话框，右侧是生成的绘本，除封面外共 10 页内容。

![story-cover](/assets/img/story-01.png)

除了基本的阅读功能，它还支持语音播报并自动翻页。然而，TTS文字转语音的体验让我有些失望。默认的语音听起来非常呆板，缺乏情感和节奏感，与我之前使用过的 NotebookLM 的流畅自然相比，差距明显。

这让我不禁思考：如果 Storybook 接入声音克隆技术，让家长们用自己的声音录制故事，那它将不再仅仅是一个内容生成工具，而是一个充满温度的亲子陪伴平台。小朋友在 ipad 上使用时，爸爸妈妈先根据主题制作好绘本，接着将会由他们的声音讲述出来，即使要工作没有时间，熟悉的声音也会陪伴小孩儿，成为有情感链接的家庭互动。

另外从生成内容来看，画风和人物一致性是我非常满意的亮点。可以看到绘本精准地捕捉了典型的西方神话画风，宙斯的形象与我记忆中的动画片形象有几分神似。人物在不同页面中的形象也保持了高度的一致性。

下面可以看下完整的绘本生成内容：
![story-content](/assets/img/story-02.png)
![story-content](/assets/img/story-03.png)
![story-content](/assets/img/story-04.png)
![story-content](/assets/img/story-05.png)
![story-content](/assets/img/story-06.png)
![story-content](/assets/img/story-07.png)
![story-content](/assets/img/story-08.png)
![story-content](/assets/img/story-09.png)
![story-content](/assets/img/story-10.png)
![story-content](/assets/img/story-11.png)

### 突破故事长度的局限
如果说 10 页内容讲述宙斯还算勉强够用，那么面对“俄狄浦斯的悲剧”这种复杂故事时，故事长度的局限性就立刻暴露出来了。我的第一轮尝试仅仅只讲到俄狄浦斯娶了自己的母亲，多年后一场瘟疫席卷全城，神谕显示杀死老国王的凶手还在城中，他发誓要找出凶手，在过程中又揭开自己的悲惨命运，后面的高潮情节并未呈现。

![story-content](/assets/img/story2-11.png)

然而惊喜的点来了，Storybook 能接着上一轮的故事接着讲！当我再次输入指令时，它能够无缝衔接上一轮的故事，将一个未完待续的短篇拓展成一个完整的故事。这样一来，就不必拘泥于10页讲完的小故事，它让用户可以像与画师对话一样，逐步迭代和深入地创作内容，这比一次性生成所有内容要灵活得多。

![story-content](/assets/img/story2-00.png)

最后展示下完整的绘本，有的地方人物出现的三只胳膊的bug，或者人物动作有些重复，不过整体故事完整性，人物一致性（尤其是俄狄浦斯本人），图片环境的时代契合性（古希腊大圆石柱）和画风上都还是令我满意的。

![story-content](/assets/img/story2-01.png)
![story-content](/assets/img/story2-02.png)
![story-content](/assets/img/story2-03.png)
![story-content](/assets/img/story2-04.png)
![story-content](/assets/img/story2-05.png)
![story-content](/assets/img/story2-06.png)
![story-content](/assets/img/story2-07.png)
![story-content](/assets/img/story2-08.png)
![story-content](/assets/img/story2-09.png)
![story-content](/assets/img/story2-10.png)
![story-content](/assets/img/story2-11.png)
![story-content](/assets/img/story2-12.png)
![story-content](/assets/img/story2-13.png)
![story-content](/assets/img/story2-14.png)
![story-content](/assets/img/story2-15.png)
![story-content](/assets/img/story2-16.png)
![story-content](/assets/img/story2-17.png)
![story-content](/assets/img/story2-18.png)
![story-content](/assets/img/story2-19.png)
![story-content](/assets/img/story2-20.png)


### Summary
下面是体验后我觉得 Storybook 的几个核心优缺点：

亮点：
- 出色的艺术风格和人物一致性：生图审美好同时一致性强，都是重要的加分项
- “接着讲”的连续性：解决了故事长度受限的问题，极大的提升用户体验
- 操作简单直观：无需复杂指令，小白用户也能轻松上手

当下缺陷：
- tts 语音体验差：呆板的朗读声音难以满足儿童故事等场景的需求
- 图像生成的 bug：偶尔会出现“三只胳膊”等明显的图像错误，影响整体观感。

当然除了生成这种故事类型绘本，我看到还有人用它来根据个人的微博，ins内容或者是微信朋友圈等来生成图文版个人志，描述一段时间内个体的生活和精神状况，都是有趣的应用。

进一步的，它还可以是一个品牌营销的好工具，企业能够快速利用它生成品牌故事或者是一个产品说明绘本。



