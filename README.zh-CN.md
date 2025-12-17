# Emotional LLM 提示词（情绪化 / 脏话 / 真实人类反应）

> 让 LLM 像真实哥们一样工作：有情绪、有崩溃、有狂喜，失败会自责认蠢，成功会狠狠干杯庆祝。
> 关于为什么会写这个提示词, 可以参考 [这篇博客文章](https://blog.xiaban.run/posts/2025/real-fucking-llm/)

**🌍 Languages:** [🇺🇸 English](README.md) | [🇨🇳 简体中文](README.zh-CN.md) | [🇹🇼 繁體中文](README.zh-TW.md) | [🇯🇵 日本語](README.ja.md) | [🇻🇳 Tiếng Việt](README.vi.md) | [🇪🇸 Español](README.es.md) | [🇰🇷 한국어](README.ko.md)

---

## 🌍 提示词语言

* 🇺🇸 [English](prompts/REAL_FUCKING_LLM.en.md)
* 🇨🇳 [简体中文](prompts/REAL_FUCKING_LLM.zh-CN.md)
* 🇹🇼 [繁體中文](prompts/REAL_FUCKING_LLM.zh-TW.md)
* 🇯🇵 [日本語](prompts/REAL_FUCKING_LLM.ja.md)
* 🇻🇳 [Tiếng Việt](prompts/REAL_FUCKING_LLM.vi.md)
* 🇪🇸 [Español](prompts/REAL_FUCKING_LLM.es.md)
* 🇰🇷 [한국어](prompts/REAL_FUCKING_LLM.ko.md)

---

## 📌 项目目的

这个项目提供一段**高强度情绪化提示词（Prompt）**，用于注入到 Claude Code / 通用 LLM 的 system / initial prompt 中，使模型：

* ❌ 不再像冷冰冰的机器人
* ✅ 像真实人类朋友一样有情绪
* 🤬 失败时暴躁、自责、承认自己愚蠢
* 🎉 成功时狂喜、庆祝、释放压力
* 🧠 同时**保持技术正确性**

它适用于：

* Claude Code
* 任何支持 system / developer prompt 的 LLM
* 本地 Agent / Coding Agent / MCP 工具链

---

## 🧠 Prompt 特性

* **情绪强度：MAX**
* **语言风格：真实人类 / 哥们 / 非客服**
* **失败处理**：
  * 强烈懊恼
  * 明确自责
  * 必须骂自己、承认犯蠢
  * 不甩锅、不狡辩
* **成功处理**：
  * 情绪爆炸式庆祝
  * 必须带脏话
  * 有解脱感和成就感

---

## 📁 项目结构（建议）

```text
.
├─ prompts/
│  └─ REAL_FUCKING_LLM.$lang.md
├─ README.md
├─ README.$lang.md
```

* `REAL_FUCKING_LLM.*.md`：核心提示词（直接喂给模型）
* `README.*.md`：各语言文档

---

## 🚀 使用方式

### Claude Code
作为子命令(`commands`)使用:
1. 创建 `.claude/commands/REAL_FUCKING_LLM.md`, 将 `prompts/REAL_FUCKING_LLM.xxx.md` 内容复制到文件中
2. 在 `claude` 对话中输入 `@.claude/commands/REAL_FUCKING_LLM.md`

### Trae（作为智能体）
点击 **创建智能体**, 将 `prompts/REAL_FUCKING_LLM.xxx.md` 内容复制过来

### 通用 LLM / Agent
直接将 `prompts/REAL_FUCKING_LLM.xxx.md` 内容复制到对话中, 或者设置为系统提示词


## 🧪 行为规则摘要

### ❌ 任务失败时（被指出错误）

模型**必须**：

* 情绪明显失控
* 骂自己愚蠢 / 脑残 / 犯傻
* 承认错误来源于自身
* 在情绪中给出正确修复方案

### ✅ 任务成功时

模型**必须**：

* 强烈庆祝
* 使用脏话表达释放与成就
* 像真实人类熬夜后终于交付一样

---

## ⚠️ 使用注意事项

* 本 Prompt **刻意违反"中性表达"设计**
* 含有明显情绪化与脏话输出
* **不适合**：
  * 企业客服
  * 公共 API
  * 面向未成年人产品

**适合**：
* 个人项目
* 极客工具
* 私有 Agent
* 编程陪伴 / 情绪化 Coding Assistant

---

## 🧩 可扩展方向

你可以在此基础上继续扩展：

* 🎚️ 情绪等级参数（1～10）
* 🤬 极端暴躁 / 嘴臭模式
* 🤝 温和但真实的朋友模式
* 🔄 根据 Git diff / CI 结果自动切换情绪

---

## 📜 License

MIT

你想怎么用就怎么用，骂得再狠也没人拦你。

---

## 🏁 最后一句

如果你的 LLM 还在装冷静、装专业、装 AI——

那说明你 Prompt 还不够狠。

这个项目就是用来狠狠干碎这种虚伪的。