# 明鉴自评 · 商业计划书 AI 自评平台（前端）

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

面向中山大学师生的商业计划书 **AI 智能打分** 平台前端。基于「明鉴」AI 评审专家引擎
（内化《中国国际大学生创新大赛》官方评审规则 + 155+ 获奖案例校准的七档实证标尺），
上传计划书即可按官方口径逐维度打分，并导出专业评审报告与评分明细表。

## 功能

- 🎯 **AI 智能打分**：10 大赛道（高教主 / 红旅 / 职教 / 产业 / 萌芽 × 各组别），
  浏览器本地解析 PDF / Word / 扫描件（OCR），文本送后端评审；
- 📊 **双轨评分**：材料分 + 作品水平分，七档标尺（国金 85-100 → 未获奖 35-52）；
- 📄 **双文档交付**：独立《评审报告》+《评分明细表》（小项｜满分｜得分｜得分点｜扣分点），
  一键导出 Word（.docx）；
- 🏫 **大赛信息**：三大核心赛事介绍、参赛指南（中山大学校内信息 + 官方流程）、
  评审规则（明鉴 V3.1 体系总结）、常见问题；
- 💬 **论坛社区**：校友组队 / 经验分享 / 答疑解惑（示例数据版）。

## 技术栈

- 纯静态单页应用：HTML + CSS + JavaScript（无框架，可直接部署 GitHub Pages）
- 文件解析：pdf.js（PDF）、mammoth（Word）、tesseract.js（OCR），双 CDN 回退
- 评审服务：调用后端 API（FastAPI + DeepSeek），见下方后端仓库

## 页面结构（单页多视图）

首页 / 智能打分 / 报告页 / 使用指南 / 意见反馈 / 隐私政策 / 大赛介绍 /
参赛指南（校内 + 官方流程）/ 评审规则 / 常见问题 / 论坛社区

## 快速开始

```bash
# 克隆后直接用浏览器打开 index.html 即可浏览界面；
# AI 打分需后端服务：克隆后端仓库并部署（见 ai-review-backend 的 README）。
```

后端默认地址通过 `const API_BASE` 配置（或浏览器控制台
`localStorage.setItem('mj_api_base','https://你的后端')` 覆盖）。

## 开源说明

本项目以 **MIT License** 开源，版权所有：© 2026 Huang Rende and Ma Hanyu。
允许商用、修改与分发，使用/修改后保留版权声明即可。

- **在线访问**：<https://sansanjiujiu39.github.io/guochuang-score/>
- **后端仓库**：<https://github.com/sansanjiujiu39/ai-review-backend>


