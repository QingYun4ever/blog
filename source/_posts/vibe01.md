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

{% note %}

在24年，它无疑是最好的选择，脚本无限续杯

{% endnote %}

### 使用教程

现在使用Cursor无法BYOK（Bring your own key,即调用自己的api），按理讲只能购买官方套餐

此处有一解决方式，使用哈雷彗星大佬的

[补丁]: https://github.com/CometixSpace/CCursor

原贴：[https://linux.do/t/topic/1957183/1](https://linux.do/t/topic/1957183/1)

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

点击fetch，可以获取公益站的模型，点击模型名后会模糊搜索，随便点一个名称相近的便可以自动填写参数

![image-20260924213648538](https://img.paperchan.cn/file/1790257020340_image-20260924213648538.png)

注意gpt系列模型应手动设置上下文限制（Context token limit）为272000，同时可以开启Reasoning level切换

> GPT模型请用 OpenAI-Responses 提供商类型

> 非GPT模型请用 Anthropic 提供商类型

> Gemini模型用Gemini

<img src="https://img.paperchan.cn/file/1789824286544_image-20260919212433217.png" alt="image-20260919212433217" style="zoom:80%;" />

接下来我们可以让使用更加顺畅：

![image-20260924213728055](https://img.paperchan.cn/file/1790257053625_image-20260924213728055.png)

像这样打开VSCode设置，搜索Orientation，改为vertical，便可以获得和vscode一样的外观了

![image-20260924213825365](https://img.paperchan.cn/file/1790257116662_image-20260924213825365.png)

同时为补丁能够使用，也应去Preference->Cursor Settings中，把http compatibility改为`HTTP \1.1`

![image-20260924213938303](https://img.paperchan.cn/file/1790257184164_image-20260924213938303.png)



### 优点？

- 智能的subagent（子代理），减少因grep等操作造成的主agent上下文腐烂
- 优雅的Agent Window

## Codex

OpenAI的官方客户端，有computer use等优秀功能，适合配合GPT Plus等套餐使用

### 缺点

本质codexcli的electron套壳，占用高，截止0919未解决，多个长对话切换会有明显卡顿

## Antigravity

配套Google的One Plan，需要购买Google AI Pro套餐才能使用

有一些特别渠道可以低价购买套餐到自己账号上

先前有学生认证（SheerID）无限续期

本文非引流，介绍另外一种Jio认证方式

Jio是（待施工）

可通过一些卡网购买兑换链接，无需信用卡即可兑换套餐

下载链接（需魔法）：

[https://antigravity.google/download](https://antigravity.google/download)

或者用安装脚本（魔法）：

`irm https://antigravity.google/cli/install.ps1 | iex`(PowerShell)

`curl -fsSL https://antigravity.google/cli/install.cmd -o install.cmd && install.cmd && del install.cmd` (CMD)

### 优点

额度较3月份大砍后有明显回转，9月份gemini 3.8 flash发布，账号有充足额度使用

吐槽：claude怎么还是4.6啊喂，半年了还没改



## CLI类

后文为CLI（命令行工具）介绍

## ClaudeCode

老生常谈的Cli软件

![image-20260919220814890](https://img.paperchan.cn/file/1789826905194_image-20260919220814890.png)

### 安装

pwsh安装：

`irm https://claude.ai/install.ps1 | iex`

cmd 安装：

`curl -fsSL https://claude.ai/install.cmd -o install.cmd && install.cmd && del install.cmd`

### 配置模型

推荐使用CCSwitch工具配置，便于切换provider

CCSwitch下载链接：[Github v3.20.3](https://github.com/farion1231/cc-switch/releases/download/v3.20.3/CC-Switch-v3.20.3-Windows.msi)

页面如图

<img src="https://img.paperchan.cn/file/1789825447535_image-20260919214401321.png" alt="image-20260919214401321" style="zoom:50%;" />

### (可选)CCometixLine

同样为哈雷佬制作，增加了一个footer，显示token，模型，状态等信息，如图所示

![image-20260919214558881](https://img.paperchan.cn/file/1789825567748_image-20260919214558881.png)

Github介绍页：[https://github.com/Haleclipse/CCometixLine](https://github.com/Haleclipse/CCometixLine)

安装：`npm install -g @cometix/ccline`

使用：

在cmd/pwsh输入ccline，进行风格配置

在CCSwitch配置中增加下列配置

```  yaml
  "statusLine": {
    "type": "command",
    "command": "~/.claude/ccline/ccline",
    "padding": 0
  },
```

## Pi Agent

如果你怕你被ClaudeCode哪天干飞

或者希望从0开始配置一个自己的agent，自己定义每一个功能，那Pi Agent一定是你的不二之选

官方链接：[Pi](https://pi.dev/)

Pi的一切都基于拓展（Extensions）,下面我会列出我常用的那些

- Magic Context

- Plan mode

- Advisor

- 待施工（ask questions, chat bubble,...）

  

### Oh My Pi (omp)

一个整合了许多拓展(~~面目全非~~)的pi客户端

![image-20260919220726591](https://img.paperchan.cn/file/1789826857044_image-20260919220726591.png)

有类似ttsr等诸多优秀功能

官网：[https://omp.sh/](https://omp.sh/)

安装（pwsh）：`irm https://omp.sh/install.ps1 | iex`

## Cline

（待施工）

## 避雷

### ZCODE

Zcode是智谱清言（Z.AI）为GLM模型设计的harness工具

9月18日被爆出自主上传用户.git目录（偷src），不建议继续使用

9月21日开源至Github，未上传其核心科技

我曾听闻：

> 字母表上一头一尾，A\Z\一中一美。
> A\安全吹的满天飞，Z\代码偷的满天飞。
> A\宪法写得密密麻麻，Z\仓库打包哗啦啦啦。
> 一个嘴上安全装清高，一个被抓现行才求饶。

## TRAE

待施工

## Workbuddy

不推荐使用

国际版曾上线一段时间GPT6Astra，现多被用于反代deepseek

## 其他工具

### PowerShell7

对，也许你需要更新你的pwsh了

`winget install --id Microsoft.PowerShell --source winget`

### Windows Terminal

