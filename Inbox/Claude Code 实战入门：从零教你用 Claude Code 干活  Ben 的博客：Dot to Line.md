---
title: "Claude Code 实战入门：从零教你用 Claude Code 干活 | Ben 的博客：Dot to Line"
source: "https://benx.ai/blog/posts/claude-code-practical-guide-2026"
author:
  - "[[Ben]]"
published: 2026-03-31
created: 2026-05-12
description: "Claude Code 不只是聊天，而是能直接帮你动手做事。从搜索资料、爬取网页到写文章，5 个真实场景带你掌握 Claude Code 的实战用法。附 Skills、MCP、斜杠命令等进阶技巧。"
tags:
  - "clippings"
---
> 本文持续更新，最新版本请查看： [飞书原文](https://waytoagi.feishu.cn/wiki/QR3MwiNmPikTiykJ5GIcxsDpnWh)
> 
> 分享人：Ben | AI工具进化论
> 
> 适合人群：想用 AI 提升效率的产品经理、开发者、内容创作者

## 一、Claude Code 是什么？和普通 AI 对话有何不同

### 1.1 一句话定义

Claude Code 是 Anthropic 推出的 AI 编程助手，能直接在你的电脑上帮你干活。你只需要用简单的语言告诉它要做什么，它就能理解你的项目，自动完成操作。

核心区别： **不只是聊天，而是能直接帮你动手做事。**

### 1.2 和 ChatGPT / Claude 网页版的核心区别

| 维度 | 普通 AI 对话（网页版） | Claude Code |
| --- | --- | --- |
| 交互方式 | 复制代码 → 粘贴到对话框 → 复制回答 → 粘贴回编辑器 | 直接在你的项目里操作，不需要来回复制 |
| 上下文 | 你告诉它什么，它才知道什么 | 它能自己读你整个项目的代码，自己搜索文件 |
| 执行力 | 只能给你建议和代码片段 | 能直接创建文件、修改代码、运行命令、跑测试 |
| 记忆 | 每次对话是独立的 | 通过 CLAUDE.md 和 Memory 系统，它能记住项目规则和你的偏好 |
| 工具调用 | 无法调用外部工具 | 通过 MCP 可以连接浏览器、数据库、GitHub 等外部服务 |

### 1.3 一个直观的比喻

- **普通 AI 对话** = 你打电话问一个远程顾问
- **Claude Code** = 你请了一个助手坐在你旁边，他能自己翻你的文件夹，自己动手改

## 二、安装和配置

### 2.1 推荐方式：VS Code + Claude Code 插件

详细安装步骤请参考： [Claude Code 保姆级入门教程（2026.3 月更新）](https://waytoagi.feishu.cn/docx/DKp0dhZ5foPMg2xrDYKcO0rtnxd)

### 2.2 配置好之后的界面

![][attachments/a6933f0b8e712dbf4804c79a22ba6e34_MD5.webp]

![][attachments/21abb7a81cfdef8f5bbff3f0d8a33c63_MD5.webp]

### 2.3 第一次体验：让 Claude Code 帮你整理文件

打开你的「下载」文件夹，输入「帮我整理一下文件」：

![[attachments/db1b99959cb2201fceb43121c2bfdc53_MD5.webp]]

## 三、场景一：搜索资料，让 Claude 自动搜索、整理、总结

Claude Code 可以帮你自动搜索网上的资料，并整理成你需要的格式。

### 三类搜索工具

**1\. 内置 WebSearch** （开箱即用）

不需要任何额外配置，Claude Code 自带的搜索能力。直接说「帮我搜索 XXX」就行。

**2\. 搜索 MCP 插件** （更专业的搜索）

| 插件 | 免费额度 | 特点 |
| --- | --- | --- |
| Brave Search | 2000 次/月 | 免费额度大，日常够用 |
| Tavily | 1000 次/月 | AI 友好的搜索结果 |
| Perplexity | 按量付费 | 搜索质量最高 |

**3\. Context7 MCP** （专查编程文档）

专门用来查编程框架和库的文档，比通用搜索更精准。

### 使用方式

直接告诉 Claude Code：「帮我搜索 2026 年最新的 React Server Components 用法，整理成一份对比表格」

## 四、场景二：爬取网页，抓取网页内容、提取关键信息

需要从网页上抓取信息时，Claude Code 有三种工具可以选择：

| 工具 | 适合场景 | 稳定性 |
| --- | --- | --- |
| Chrome DevTools MCP | 日常首选，最稳定 | ⭐⭐⭐ |
| WebFetch | 快速抓简单页面 | ⭐⭐ |
| agent-browser | 需要隔离环境时 | ⭐⭐ |

### 使用方式

告诉 Claude Code：「帮我打开 XXX 网站，抓取页面上的产品列表，整理成表格」

## 五、场景三：写文章，从调研到成稿的完整流程

这是我用得最多的场景之一。Claude Code 不只能写代码，还能帮你写文章。

### 四步流程

1. **调研** ：让 Claude Code 搜索相关资料，整理关键信息
2. **确定大纲** ：基于调研结果，和 Claude Code 讨论大纲
3. **写初稿** ：Claude Code 按大纲写出初稿
4. **降 AI 味审校** ：加入个人经历和观点，让文章更有人味

### 关键技巧

- 提供你的写作风格参考（可以给 Claude Code 看你之前写过的文章）
- 用 CLAUDE.md 记录你的写作规范
- 用 Skills 封装写作流程，下次直接复用

## 六、进阶技巧：Skills、MCP、斜杠命令的实际应用

### 斜杠命令

![[attachments/869c1c2fc2ebfcc4edd9dff5bd7c9954_MD5.webp]]

常用斜杠命令：

- `/compact` — 压缩对话，节省上下文
- `/clear` — 清空对话，重新开始
- `/rewind` — 回退到上一步
- `/voice` — 语音模式（按住空格说话）

### 工作模式切换

![[attachments/bdbfe46af197f8a110056eb43d8f9b4d_MD5.webp]]

四种模式：

- **Plan mode** ：只规划不执行，适合复杂任务
- **Ask before edit** ：每次修改前问你确认
- **Edit automatically** ：自动修改，但危险操作会确认
- **Bypass permissions** ：全自动模式（个人项目用）

### 历史对话

![[attachments/4fde7b47560369bca1589cc6370ecaf1_MD5.webp]]

所有对话都会保存，可以随时回顾之前的工作。

### @ 引用

![[attachments/6b0e2905c695c4a04460531ee6c90881_MD5.webp]]

用 `@文件名` 可以直接引用项目中的文件，让 Claude Code 读取和理解。

### 添加上下文

![[attachments/55643e8822c5580b6cadeaf6fe4c9a9a_MD5.webp]]

可以添加文件、文件夹、甚至网页链接作为上下文。

### CLAUDE.md

在项目根目录创建 `CLAUDE.md` 文件，写入项目规则和偏好。Claude Code 每次启动都会读取这个文件，相当于给 AI 助手一份「工作手册」。

### Skills

![[attachments/83630017917cd9a86456b708e44712bb_MD5.webp]]

Skills 是可复用的 AI 工作流。你可以：

- 使用别人做好的 Skills（ [https://github.com/anthropics/skills）](https://github.com/anthropics/skills%EF%BC%89)
- 自己创建 Skills，封装重复性工作

### MCP（Model Context Protocol）

MCP 让 Claude Code 可以连接外部服务：

- **Chrome DevTools MCP** ：操作浏览器
- **Brave Search MCP** ：搜索网络
- **Context7 MCP** ：查编程文档
- **飞书 MCP** ：操作飞书文档、日历、消息等

## 七、常见问题和避坑指南

**Q1：Claude Code 怎么付费？**

三种方式：

- Claude Pro/Max 订阅（官方，需外币信用卡）
- 中转 API（推荐国内用户）
- 国产大模型平替（DeepSeek、Kimi K2 等）

**Q2：改错了怎么撤销？**

- 按 ESC 两次取消当前操作
- 输入 `/rewind` 回退
- 直接说「帮我还原刚才的修改」

**Q3：文件会不会被搞乱？**

Claude Code 默认在「Ask before edit」模式下工作，每次修改都会先问你确认。如果不确定，在重要项目上先用 git 做个备份。

**Q4：提示 request body too large**

![[attachments/388a18a8999c77a9a22af37eb9beaa31_MD5.webp]]

原因：发送了太大的文件。解决：新开一个对话，避免直接发送大图。

**Q5：代码质量怎么保证？**

- 让 Claude Code 写完后自己跑测试
- 重要功能手动测试一遍
- 用 git 管理版本，方便回退

**Q6：常见的坑**

- 不要在一个对话里塞太多任务，容易混乱
- 复杂任务先用 Plan mode 规划，再执行
- 定期用 `/compact` 压缩对话，避免上下文溢出

## 八、总结：我用 Claude Code 的真实感受

用了半年多 Claude Code，最大的感受是： **它改变了我的工作方式** 。

以前很多想法，卡在「我不会写代码」这一步。现在，从想法到产品的距离，缩短到了一句话。

但它也不是万能的。复杂的系统架构、精细的性能优化、深度的 debug，还是需要人的判断。Claude Code 最擅长的是： **帮你快速把想法变成可运行的东西，然后你在这个基础上迭代。**

## 九、实战小作业：学完就练

**作业一：创建一个自己的 Skill（入门级）**

把你常用的工作流封装成一个 Skill，比如「每次写完代码自动跑测试」。

**作业二：写一份调研报告（中级）**

选一个你感兴趣的话题，让 Claude Code 帮你搜索资料、整理信息、生成报告。

**作业三：做一个能玩的网页小游戏（进阶级）**

用 Claude Code 做一个贪吃蛇、打砖块或者扫雷游戏，部署上线分享给朋友。

---

**关于作者** ：Ben，WaytoAGI AI 编程区主理人，前飞书多维表格产品经理。用 AI 编程独立完成 40+ 个网站项目。公众号 @AI工具进化论 | Twitter @littlebena