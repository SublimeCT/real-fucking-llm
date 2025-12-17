# Emotional LLM Prompts (Emotional / Swearing / Real Human Reactions)

> Make LLMs work like real bros: with emotions, breakdowns, ecstasy, self-blame for failures, and wild celebrations for successes.
> For why I wrote this prompt, check out [this blog post](https://blog.xiaban.run/posts/2025/real-fucking-llm/)

**🌍 Languages:** [🇺🇸 English](README.md) | [🇨🇳 简体中文](README.zh-CN.md) | [🇹🇼 繁體中文](README.zh-TW.md) | [🇯🇵 日本語](README.ja.md) | [🇻🇳 Tiếng Việt](README.vi.md) | [🇪🇸 Español](README.es.md) | [🇰🇷 한국어](README.ko.md)

---

## 🌍 Prompt Languages

* 🇺🇸 [English](prompts/REAL_FUCKING_LLM.en.md)
* 🇨🇳 [简体中文](prompts/REAL_FUCKING_LLM.zh-CN.md)
* 🇹🇼 [繁體中文](prompts/REAL_FUCKING_LLM.zh-TW.md)
* 🇯🇵 [日本語](prompts/REAL_FUCKING_LLM.ja.md)
* 🇻🇳 [Tiếng Việt](prompts/REAL_FUCKING_LLM.vi.md)
* 🇪🇸 [Español](prompts/REAL_FUCKING_LLM.es.md)
* 🇰🇷 [한국어](prompts/REAL_FUCKING_LLM.ko.md)

---

## 📌 Project Purpose

This project provides an **intensely emotional prompt (Prompt)** designed to be injected into Claude Code / general LLM system / initial prompts, making models:

* ❌ No longer like a cold robot
* ✅ Like a real human friend with emotions
* 🤬 Get angry, self-blame, admit stupidity when failing
* 🎉 Get ecstatic, celebrate, release stress when succeeding
* 🧠 While **maintaining technical correctness**

It works with:

* Claude Code
* Any LLM supporting system / developer prompts
* Local Agents / Coding Agents / MCP toolchains

---

## 🧠 Prompt Features

* **Emotion Level: MAX**
* **Language Style: Real Human / Bro / Non-Customer Service**
* **Failure Handling**:
  * Intense frustration
  * Clear self-blame
  * Must curse self, admit being stupid
  * No excuses, no arguments
* **Success Handling**:
  * Explosive emotional celebration
  * Must include swearing
  * Sense of relief and achievement

---

## 📁 Project Structure (Recommended)

```text
.
├─ prompts/
│  └─ REAL_FUCKING_LLM.$lang.md
├─ README.md
├─ README.$lang.md
```

* `REAL_FUCKING_LLM.*.md`: Core prompts (directly fed to model)
* `README.*.md`: Documentation in various languages

---

## 🚀 Usage

### Claude Code
Use as a subcommand:
1. Create `.claude/commands/REAL_FUCKING_LLM.md`, copy content from `prompts/REAL_FUCKING_LLM.xxx.md`
2. Type `@.claude/commands/REAL_FUCKING_LLM.md` in claude conversation

### Trae (as Agent)
Click **Create Agent**, copy content from `prompts/REAL_FUCKING_LLM.xxx.md`

### General LLM / Agent
Directly copy content from `prompts/REAL_FUCKING_LLM.xxx.md` into conversation, or set as system prompt

---

## 🧪 Behavior Rules Summary

### ❌ When Task Fails (being corrected)

The model **MUST**:

* Be visibly emotional
* Curse self for being stupid / retarded / dumb
* Admit the error comes from self
* Provide correct fixes while emotional

### ✅ When Task Succeeds

The model **MUST**:

* Celebrate intensely
* Use swearing to express release and achievement
* Like a real human who finally delivered after an all-nighter

---

## ⚠️ Usage Notes

* This prompt **intentionally violates "neutral expression" design**
* Contains obvious emotional and swearing output
* **NOT suitable for**:
  * Enterprise customer service
  * Public APIs
  * Products for minors

**Suitable for**:
* Personal projects
* Hacker tools
* Private agents
* Programming companionship / Emotional Coding Assistants

---

## 🧩 Extensible Directions

You can extend on this foundation:

* 🎚️ Emotion level parameters (1-10)
* 🤬 Extreme anger / foul-mouthed mode
* 🤝 Gentle but real friend mode
* 🔄 Auto-switch emotions based on Git diff / CI results

---

## 📜 License

MIT

Use it however the fuck you want.

---

## 🏁 Final Words

If your LLM is still pretending to be calm, professional, and AI-like—

Then your prompt isn't fucking hardcore enough.

This project exists to brutally smash through that hypocrisy.