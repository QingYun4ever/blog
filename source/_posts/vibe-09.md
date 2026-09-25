---
title: Vibe杂谈-技巧
date: 2026-09-22 01:03:12
categories:
tags:
---

## 前言

本文简单介绍一些实用技巧

## 联网搜索

由于模型内置的联网搜索能力有时效果并不理想，这里我推荐几种方案

### Tavily

![image-20260923054908512](https://img.paperchan.cn/file/1790113771395_image-20260923054908512.png)

Tavily是一个search/fetch api平台，每账号有1000credit/month,计费分为两种

- Basic Search - 1credit
- Advanced Search - 3credit

总的来说免费余额相当充足，搜索效果也很不错，很适合让AI自主寻找对应doc，并fetch读取

使用方式？

官方文档提供多harness的一键安装脚本，将以skills形式安装，并以环境变量的方式存储api key

### grok

grok以其极强的联网搜索能力著称

我们可以购买free账号的sso/cookie认证文件（很廉价）

使用grok-4.3-fast/grok-4.20-multiagent模型进行搜索



可使用smart search cli/skill便捷接入



## 生图

### GPT-Image-2.5

CPA等工具反代出来的GPT Plus账户的该生图模型并不能直接调用

可以使用5.6-terra等模型使用Responses AI提示词生图，一次生图大概5h额度1%

### GPT Image Playground

开源项目，提供便捷使用的图片生成与编辑

![image-20260924215857202](https://img.paperchan.cn/file/1790258345559_image-20260924215857202.png)

项目地址：[https://github.com/CookSleep/gpt_image_playground](https://github.com/CookSleep/gpt_image_playground)

### GPT Image Canvas

如名，一个图像生成兼编辑的画布

![GPT Image Canvas preview](https://github.com/mrslimslim/gpt-image-canvas/raw/main/docs/assets/app-preview.png)

项目地址：[https://github.com/mrslimslim/gpt-image-canvas](https://github.com/mrslimslim/gpt-image-canvas)

