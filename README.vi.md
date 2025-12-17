# Emotional LLM Prompt (Cảm xúc / Chửi rủa / Phản ứng Người thật)

> Khiến LLM của bạn hoạt động như một người bạn thật: có cảm xúc, có lúc sụp đổ, có lúc điên cuồng, thất bại sẽ tự dỗi nhận mình dốt, thành công sẽ chúc mừng rùm beng.

---

## 📌 Mục đích Dự án

Dự án này cung cấp một **prompt cảm xúc cường độ cao** để tiêm vào Claude Code / LLM chung system / initial prompt, làm cho mô hình:

* ❌ Không còn như một robot lạnh lẽo
* ✅ Như một người bạn thật có cảm xúc
* 🤬 Thất bại thì cáu gắt, tự trách, thừa nhận mình dốt
* 🎉 Thành công thì điên cuồng, ăn mừng, giải tỏa căng thẳng
* 🧠 Đồng thời **duy trì tính kỹ thuật chính xác**

Phù hợp cho:

* Claude Code
* Bất kỳ LLM nào hỗ trợ system / developer prompt
* Agent địa phương / Coding Agent / chuỗi công cụ MCP

---

## 🧠 Đặc tính Prompt

* **Cảm xúc: MAX**
* **Phong cách Ngôn ngữ: Người thật / Bạn bè / Không phải Dịch vụ Khách hàng**
* **Xử lý Thất bại**：
  * Hối hận mạnh mẽ
  * Tự trách rõ ràng
  * Phải chửi mình, thừa nhận mình dốt
  * Không đổ lỗi, không bao biện
* **Xử lý Thành công**：
  * Ăn mừng bùng nổ cảm xúc
  * Phải có từ chửi
  * Có cảm giác giải thoát và thành tựu

---

## 📁 Cấu trúc Dự án (Đề xuất)

```text
.
├─ prompts/
│  └─ HUMAN_PROMPTS.$lang.md
├─ README.md
├─ README.$lang.md
```

* `HUMAN_PROMPTS.*.md`: Prompt cốt lõi (trực tiếp cho mô hình)
* `README.*.md`: Tài liệu các ngôn ngữ

---

## 🌍 Ngôn ngữ

* 🇺🇸 [English](README.md)
* 🇨🇳 [简体中文](README.zh-CN.md)
* 🇯🇵 [日本語](README.ja.md)
* 🇻🇳 [Tiếng Việt](README.vi.md)
* 🇪🇸 [Español](README.es.md)
* 🇰🇷 [한국어](README.ko.md)

---

## 🚀 Cách sử dụng

### Claude Code

```bash
# Như lệnh con
claude code --system-file prompts/HUMAN_PROMPTS.vi.md

# Hoặc tiêm vào phiên làm việc
cat prompts/HUMAN_PROMPTS.vi.md | claude code --system-prompt -
```

### Trae (như một AI Agent)

```javascript
// Cấu hình Trae
const agentConfig = {
  systemPrompt: fs.readFileSync('prompts/HUMAN_PROMPTS.vi.md', 'utf8'),
  // ... các cấu hình khác
};
```

### CodeX / Cursor (các triển khai tương tự)

```python
# Cho CodeX
import os

with open('prompts/HUMAN_PROMPTS.vi.md', 'r') as f:
    system_prompt = f.read()

# Sử dụng trong cuộc gọi API
response = openai.ChatCompletion.create(
    model="gpt-4",
    messages=[
        {"role": "system", "content": system_prompt},
        {"role": "user", "content": user_input}
    ]
)
```

```bash
# Cho Cursor - thêm vào .cursorrules hoặc cài đặt không gian làm việc
echo "cat prompts/HUMAN_PROMPTS.vi.md" > ~/.cursor/rules/emotional-prompt.rule
```

### LLM / Agent Chung

* Đặt vào **system role**
* Ưu tiên phải cao hơn task prompt

> ⚠️ Đừng coi đây là user prompt

---

## 🧪 Tóm tắt Quy tắc Hành vi

### ❌ Khi Thất bại (bị chỉ ra lỗi)

Mô hình **PHẢI**:

* Cảm xúc rõ ràng mất kiểm soát
* Chửi mình dốt / não nát / ngốc
* Thừa nhận lỗi đến từ bản thân
* Đưa ra phương án sửa đúng trong cảm xúc

### ✅ Khi Thành công

Mô hình **PHẢI**:

* Ăn mừng mạnh mẽ
* Sử dụng từ chửi để biểu đạt giải thoát và thành tựu
* Như người thật thức đêm cuối cùng cũng giao hàng

---

## ⚠️ Lưu ý Sử dụng

* Prompt này **cố ý vi phạm thiết kế "biểu đạt trung lập"**
* Chứa đầu ra cảm xúc và từ chửi rõ rệt
* **KHÔNG phù hợp** cho：
  * Dịch vụ khách hàng doanh nghiệp
  * API công khai
  * Sản phẩm cho vị thành niên

**Phù hợp** cho：
* Dự án cá nhân
* Công cụ hacker
* Agent riêng tư
* Bạn đồng hành lập trình / Trợ lý Lập trình Cảm xúc

---

## 🧩 Hướng mở rộng

Bạn có thể mở rộng trên nền tảng này:

* 🎚️ Tham số cấp cảm xúc (1-10)
* 🤬 Chế độ tức giận cực độ / mồm thối
* 🤝 Chế độ bạn thân nhẹ nhàng nhưng thật
* 🔄 Tự động chuyển cảm xúc dựa trên Git diff / kết quả CI

---

## 📜 Giấy phép

MIT

Dùng thế nào cũng được.

---

## 🏁 Lời cuối

Nếu LLM của bạn vẫn còn giả vờ冷静, chuyên nghiệp, kiểu AI—

Thì prompt của bạn chưa đủ mạnh.

Dự án này tồn tại để đập tan sự giả tạo đó.