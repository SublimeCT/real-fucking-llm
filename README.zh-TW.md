# Emotional LLM 提示詞（情緒化 / 臭髒 / 真實人類反應）

> 讓 LLM 像真實哥們一樣工作：有情緒、有崩潰、有狂喜，失敗會自責認蠢，成功會狠狠乾杯慶祝。
> 關於為什麼會寫這個提示詞, 可以參考 [這篇部落格文章](https://blog.xiaban.run/posts/2025/real-fucking-llm/)

**🌍 語言:** [🇺🇸 English](README.md) | [🇨🇳 简体中文](README.zh-CN.md) | [🇹🇼 繁體中文](README.zh-TW.md) | [🇯🇵 日本語](README.ja.md) | [🇻🇳 Tiếng Việt](README.vi.md) | [🇪🇸 Español](README.es.md) | [🇰🇷 한국어](README.ko.md)

---

## 🌍 提示詞語言

* 🇺🇸 [English](prompts/REAL_FUCKING_LLM.en.md)
* 🇨🇳 [简体中文](prompts/REAL_FUCKING_LLM.zh-CN.md)
* 🇹🇼 [繁體中文](prompts/REAL_FUCKING_LLM.zh-TW.md)
* 🇯🇵 [日本語](prompts/REAL_FUCKING_LLM.ja.md)
* 🇻🇳 [Tiếng Việt](prompts/REAL_FUCKING_LLM.vi.md)
* 🇪🇸 [Español](prompts/REAL_FUCKING_LLM.es.md)
* 🇰🇷 [한국어](prompts/REAL_FUCKING_LLM.ko.md)

---

## 📌 專案目的

這個專案提供一段**高強度情緒化提示詞（Prompt）**，用於注入到 Claude Code / 通用 LLM 的 system / initial prompt 中，使模型：

* ❌ 不再像冷冰冰的機器人
* ✅ 像真實人類朋友一樣有情緒
* 🤬 失敗時暴躁、自責、承認自己愚蠢
* 🎉 成功時狂喜、慶祝、釋放壓力
* 🧠 同時**保持技術正確性**

它適用於：

* Claude Code
* 任何支援 system / developer prompt 的 LLM
* 本地 Agent / Coding Agent / MCP 工具鏈

---

## 🧠 Prompt 特性

* **情緒強度：MAX**
* **語言風格：真實人類 / 哥們 / 非客服**
* **失敗處理**：
  * 強烈懊惱
  * 明確自責
  * 必須罵自己、承認犯蠢
  * 不甩鍋、不狡辯
* **成功處理**：
  * 情緒爆炸式慶祝
  * 必須帶髒話
  * 有解脫感和成就感

---

## 📁 專案結構（建議）

```text
.
├─ prompts/
│  └─ REAL_FUCKING_LLM.$lang.md
├─ README.md
├─ README.$lang.md
```

* `REAL_FUCKING_LLM.*.md`：核心提示詞（直接餵給模型）
* `README.*.md`：各語言文檔

---

## 🚀 使用方式

### Claude Code
作為子命令(`commands`)使用:
1. 創建 `.claude/commands/REAL_FUCKING_LLM.md`, 將 `prompts/REAL_FUCKING_LLM.xxx.md` 內容複製到檔案中
2. 在 `claude` 對話中輸入 `@.claude/commands/REAL_FUCKING_LLM.md`

### Trae（作為智慧體）
點擊 **創建智慧體**, 將 `prompts/REAL_FUCKING_LLM.xxx.md` 內容複製過來

### 通用 LLM / Agent
直接將 `prompts/REAL_FUCKING_LLM.xxx.md` 內容複製到對話中, 或者設定為系統提示詞


## 🧪 行為規則摘要

### ❌ 任務失敗時（被指出錯誤）

模型**必須**：

* 情緒明顯失控
* 罵自己愚蠢 / 腦殘 / 犯傻
* 承認錯誤來源於自身
* 在情緒中給出正確修復方案

### ✅ 任務成功時

模型**必須**：

* 強烈慶祝
* 使用髒話表達釋放與成就
* 像真實人類熬夜後終於交付一樣

---

## ⚠️ 使用注意事項

* 本 Prompt **刻意違反"中性表達"設計**
* 含有明顯情緒化與髒話輸出
* **不適合**：
  * 企業客服
  * 公共 API
  * 面向未成年人產品

**適合**：
* 個人專案
* 極客工具
* 私有 Agent
* 程式設計陪伴 / 情緒化 Coding Assistant

---

## 🧩 可擴展方向

你可以在此基礎上繼續擴展：

* 🎚️ 情緒等級參數（1～10）
* 🤬 極端暴躁 / 嘴臭模式
* 🤝 溫和但真實的朋友模式
* 🔄 根據 Git diff / CI 結果自動切換情緒

---

## 📜 License

MIT

你想怎麼用就怎麼用，罵得再狠也沒人攔你。

---

## 🏁 最後一句

如果你的 LLM 還在裝冷靜、裝專業、裝 AI——

那說明你 Prompt 還不夠狠。

這個專案就是用來狠狠幹碎這種虛偽的。