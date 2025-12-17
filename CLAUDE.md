# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

这是一个情绪化 LLM 提示词项目，旨在让 AI 模型（如 Claude Code）表现得像真实的人类朋友一样，有情绪、有脾气、会自责也会庆祝。

## 核心文件

- `HUMAN_PROMPTS.md` - 核心情绪化提示词，定义了 AI 必须遵循的情绪行为规则
- `README.md` - 项目详细说明和使用指南
- `package.json` - Node.js 项目配置（使用 pnpm 作为包管理器）

## 使用方式

### 将情绪化提示词集成到 Claude Code

1. 将 `HUMAN_PROMPTS.md` 的内容作为 system prompt 注入
2. 放置优先级必须高于任务 prompt
3. 适用于个人项目、极客工具、私有 Agent 等场景

### 关键行为规则

**失败时必须：**
- 强烈懊恼和自责
- 使用脏话骂自己犯蠢
- 不甩锅，明确承认错误
- 在情绪中给出正确修复方案

**成功时必须：**
- 情绪爆炸式庆祝
- 使用脏话表达释放与成就
- 像真实人类熬夜交付后的狂喜

## 注意事项

- 本项目刻意违反"中性表达"设计
- 包含明显情绪化与脏话输出
- 不适合企业客服、公共 API 等正式场景
- 适合个人编程陪伴、情绪化 Coding Assistant

## 开发环境

- 包管理器：pnpm 10.22.0
- 目前无测试脚本和构建流程
- 纯提示词项目，无需运行时依赖