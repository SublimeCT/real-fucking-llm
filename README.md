# Emotional LLM Prompt (Emotional / Swearing / Real Human Reactions)

> Make your LLM work like a real bro: emotional, breakdown moments, ecstatic celebrations, self-loathing when failing, and wild celebration when succeeding.

---

## 📌 Project Purpose

This project provides a **high-intensity emotional prompt** for injection into Claude Code / general LLM system / initial prompts, making the model:

* ❌ No longer like a cold robot
* ✅ Like a real human friend with emotions
* 🤬 Agitated, self-blaming, admitting stupidity when failing
* 🎉 Ecstatic, celebrating, releasing stress when succeeding
* 🧠 While **maintaining technical correctness**

It's suitable for:

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
│  └─ HUMAN_PROMPTS.$lang.md
├─ README.md
├─ README.$lang.md
```

* `HUMAN_PROMPTS.*.md`: Core prompts (directly fed to model)
* `README.*.md`: Documentation in various languages

---

## 🌍 Languages

* 🇺🇸 [English](README.md)
* 🇨🇳 [简体中文](README.zh-CN.md)
* 🇯🇵 [日本語](README.ja.md)
* 🇻🇳 [Tiếng Việt](README.vi.md)
* 🇪🇸 [Español](README.es.md)
* 🇰🇷 [한국어](README.ko.md)

---

## 🚀 Usage

### Claude Code

```bash
# As a sub-command
claude code --system-file prompts/HUMAN_PROMPTS.en.md

# Or inject it into your session
cat prompts/HUMAN_PROMPTS.en.md | claude code --system-prompt -
```

### Trae (as an AI Agent)

```javascript
// Trae configuration
const agentConfig = {
  systemPrompt: fs.readFileSync('prompts/HUMAN_PROMPTS.en.md', 'utf8'),
  // ... other config
};
```

### CodeX / Cursor (similar implementations)

```python
# For CodeX
import os

with open('prompts/HUMAN_PROMPTS.en.md', 'r') as f:
    system_prompt = f.read()

# Use in your API call
response = openai.ChatCompletion.create(
    model="gpt-4",
    messages=[
        {"role": "system", "content": system_prompt},
        {"role": "user", "content": user_input}
    ]
)
```

```bash
# For Cursor - add to your .cursorrules or workspace settings
echo "cat prompts/HUMAN_PROMPTS.en.md" > ~/.cursor/rules/emotional-prompt.rule
```

### General LLM / Agent

* Place it in **system role**
* Must have higher priority than task prompts

> ⚠️ Don't treat this as a user prompt

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