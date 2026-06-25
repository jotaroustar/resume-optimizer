# 📝 📄 简历优化器 (Resume Optimizer)

<!-- Copyright © 2026 jotarou.com. All rights reserved.
     未经授权的复制或商业用途均被禁止。 -->

[![Live Demo](https://img.shields.io/badge/Production-jotarou.com-d4622a.svg)](https://jotarou.com/tools/)
[![GitHub Pages](https://img.shields.io/badge/Backup-GitHub%20Pages-2d7a4f.svg)](https://jotaroustar.github.io/resume-optimizer/)
[![Pure JS](https://img.shields.io/badge/Vanilla%20JS-100%25-yellow.svg)]()

一款**纯前端、轻量级、零服务器依赖**的智能简历优化工具。集成传统的简历规则硬编码诊断（免费模式）与现代 LLM（大语言模型）的深度改写、匹配、面试预测等高级功能。

A lightweight, pure front-end, zero-server-dependency AI resume optimization tool. It integrates traditional hard-coded rule diagnostics with modern LLM deep re-writing, JD matching, and interview simulation features.

---

## 🚀 🚀 在线使用 / Live Demo

本项目已双线部署，您可以选择以下任意地址直接免安装在线使用：

* **🌐 官方生产环境（主站）**: [https://jotarou.com/tools/](https://jotarou.com/tools/)
* **⚡ GitHub Pages 镜像（备用）**: [https://jotaroustar.github.io/resume-optimizer/](https://jotaroustar.github.io/resume-optimizer/)

---

## ✨ 核心特性 / Features

* **⚡ 纯前端架构 (Serverless & Private)**：项目仅由单个 HTML 文件构成，所有逻辑均在浏览器本地运行。API Key 仅保存在用户的 `localStorage` 中，绝不上传至第三方服务器，最大程度保障隐私安全。
* **🔍 免费规则检查 (Rule-Based Diagnostic)**：
    * 自动检索简历中的**弱动词**（如：负责、参与、协助）。
    * 检测**中英文标点混用**以及异常空白行。
    * 智能识别**量化数据缺失**（未发现数字），并给出修改范例。
* **🤖 多语种 AI 深度优化 (LLM Powered)**：
    * **简历润色**：原文 vs 优化后对比高亮展示，强化动词、自动补全量化表达逻辑。
    * **JD 匹配分析**：输入目标岗位描述，自动输出匹配评分 (0-100)、已覆盖技能、缺失关键项及针对性修改建议。
    * **自我介绍生成**：支持 30秒、1分钟、2分钟三种不同时长的正式面试开场白定制。
    * **面试问题预测**：根据简历项目深挖潜在的面试硬核问题，并附带 STAR 法则回答思路引导。
* **🌐 智能语言自适应 (Language Agnostic)**：无缝支持**中文、英文、日文**简历，AI 将自动识别输入源语言并使用相同语言进行对等高质量输出。
* **📋 完美富文本复制 (Rich-Text Copying)**：内置异步 Clipboard 级一键复制，保留 Markdown 渲染后的高亮框、粗体和列表排版，可直接完美粘贴至 Word 或飞书/钉钉文档。

---

## 🛠️ 技术栈 / Tech Stack

项目坚持“极简即正义”的理念，无 Webpack/Vite 繁琐构建，通过内联高性能生产库实现开箱即用：
* **HTML5 & CSS3**：原生 CSS 变量实现高级复古米色调（Woodland/Warm Neutral）响应式 UI。
* **JavaScript (ES6+)**：原生异步 Fetch 流式可中断控制（`AbortController`）。
* **[marked.js (v18.0.5)](https://github.com/markedjs/marked)**：嵌入式高性能 Markdown 解析器。
* **[DOMPurify (v3.4.10)](https://github.com/cure53/DOMPurify)**：严苛的客户端 XSS 过滤器，确保 AI 生成的 HTML 安全。

---

## 💻 本地运行 / Local Development

如果您希望在本地独立运行：
1. 克隆或下载本仓库源码。
2. 双击运行 `index.html` 即可在本地浏览器中直接使用全部功能。

---

## ⚙️ 接入 API 平台说明 / API Configuration

本工具默认支持标准的 OpenAI API 格式兼容接口：
* **默认模型**：`gpt-4o-mini`（快速且兼顾性价比）、`deepseek-chat`（极低价格）。
* **自定义端点**：默认请求 `https://jotarou.com/v1/chat/completions`。若要在 GitHub 个人魔改版中使用官方或其他转发接口，可直接修改代码中 `callAPI` 函数内的 `baseUrl` 变量。

---

## 📄 开源协议 / License

Copyright © 2026 [jotarou.com](https://jotarou.com). All rights reserved.  
未经授权的复制或商业用途均被禁止。  

部分前端开源依赖库（Marked, DOMPurify）遵循其各自的 MIT / Apache 2.0 / MPL 2.0 开源协议。
