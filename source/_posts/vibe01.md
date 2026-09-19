---
title: Vibe Coding 01：IDE 怎么选
date: 2026-09-19 20:42:09
categories:
- AI
tags:
- vibe coding
- AI

---

## 在一切开始前

> 工欲善其事，必先利其器

本系列文章将从零开始，用朴素易懂的教程帮助各位上手AI

本篇博客为闲暇时即兴写成，如出现疏漏、不严谨之处，还望各位大佬指正

### 什么是Vibe Coding？

Vibe，直译为“氛围”，那“Vibe Coding”就是“氛围编程”

这是什么意思？

想象你是一位产品经理，你在向开发讲述项目需求，过程中你唯一做的就是对话，随后项目就完成了。

这就是vibe coding，你只需要和AI 对话，AI便会帮你写代码，跑构建，做验证。



### 本篇是什么？

现市面上，国内外有多种harness工具可供选择，新手往往眼花缭乱，无法找到最适合自己的那款，本文将一一列出常用的工具，给出使用教程与优缺点，任君选择



## Cursor

如果很早以前你曾了解过AI，那你一定听说过Cursor

清爽的UI，与VSCode无异的体验，可以让你快速上手

![image-20260919211916903](https://img.paperchan.cn/file/1789823967460_image-20260919211916903.png)

在24年，它无疑是最好的选择，脚本无限续杯

### 使用教程

现在使用Cursor无法BYOK（Bring your own key,即调用自己的api），按理讲只能购买官方套餐

此处有一解决方式，使用哈雷彗星大佬的

[补丁]: https://github.com/CometixSpace/CCursor

安装方式：

`npx @cometix/ccursor install`

前提你需要有NodeJS环境，如果你不知道什么是node，请点击下方链接下载

[node-v24.21.0](https://nodejs.org/dist/v24.21.0/node-v24.21.0-x64.msi)

![image-20260919211932360](https://img.paperchan.cn/file/1789823977687_image-20260919211932360.png)

进入cursor后点击左上角File-Open IDE，进入IDE页面后点击左侧CCursor图标，点击Add

在新建的Provider里填写base url与api key（即auth value）

base url如果使用社团的公益站，则如图填写

![image-20260919212014594](https://img.paperchan.cn/file/1789824020497_image-20260919212014594.png)

接下来配置模型

![image-20260919212201158](https://img.paperchan.cn/file/1789824132375_image-20260919212201158.png)

点击fetch，可以获取公益站的模型，点击模型选择，注意gpt系列模型应设置上下文限制（Context token limit）为272000，同时可以开启Reasoning level切换

<img src="https://img.paperchan.cn/file/1789824286544_image-20260919212433217.png" alt="image-20260919212433217" style="zoom:80%;" />

### 优点？

- 智能的subagent（子代理），减少因grep等操作造成的主agent上下文腐烂
- 优雅的Agent Window

## Codex

### 缺点

本质codexcli的electron套壳，占用高，截止0919未解决，多个长对话切换会有明显卡顿

## Antigravity

配套Google的One Plan，需要购买Google AI Pro套餐才能使用

有一些特别渠道可以低价购买套餐到自己账号上

先前有学生认证（SheerID）无限续期

本文非引流，介绍另外一种Jio认证方式

Jio是？

可通过一些卡网购买兑换链接，无需信用卡即可兑换套餐

### 优点

额度较3月份大砍后有明显回转，9月份gemini 3.8 flash发布，账号有充足额度使用

## TRAE

## Workbuddy

大份。

## CLI类

后文为CLI（命令行工具）介绍

## ClaudeCode

## Pi Agent

## Cline



## 避雷

### ZCODE

Zcode是智谱清言（Z.AI/BigModel）为自家GLM模型设计的harness工具

9月18日被爆出自主上传用户.git目录（偷src），不建议继续使用
