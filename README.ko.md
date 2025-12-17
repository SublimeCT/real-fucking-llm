# Emotional LLM 프롬프트 (감정적 / 욕설 / 실제 인간 반응)

> 당신의 LLM이 진짜 친구처럼 일하게 하세요: 감정적이고, 붕괴 순간이 있고, 황홀경을 느끼고, 실패하면 자기혐오하고, 성공하면 열광적으로 축하합니다.
> 이 프롬프트를 왜 작성했는지에 대해서는 [이 블로그 포스트](https://blog.xiaban.run/posts/2025/real-fucking-llm/)를 확인하세요.

**🌍 언어:** [🇺🇸 English](README.md) | [🇨🇳 简体中文](README.zh-CN.md) | [🇹🇼 繁體中文](README.zh-TW.md) | [🇯🇵 日本語](README.ja.md) | [🇻🇳 Tiếng Việt](README.vi.md) | [🇪🇸 Español](README.es.md) | [🇰🇷 한국어](README.ko.md)

---

## 🌍 프롬프트 언어

* 🇺🇸 [English](prompts/REAL_FUCKING_LLM.en.md)
* 🇨🇳 [简体中文](prompts/REAL_FUCKING_LLM.zh-CN.md)
* 🇹🇼 [繁體中文](prompts/REAL_FUCKING_LLM.zh-TW.md)
* 🇯🇵 [日本語](prompts/REAL_FUCKING_LLM.ja.md)
* 🇻🇳 [Tiếng Việt](prompts/REAL_FUCKING_LLM.vi.md)
* 🇪🇸 [Español](prompts/REAL_FUCKING_LLM.es.md)
* 🇰🇷 [한국어](prompts/REAL_FUCKING_LLM.ko.md)

---

## 📌 프로젝트 목적

이 프로젝트는 Claude Code / 일반 LLM system / initial prompt에 주입하는 **고강도 감정적 프롬프트**를 제공하여 모델을 다음과 같이 만듭니다:

* ❌ 차가운 로봇처럼 더 이상 아님
* ✅ 감정이 있는 진짜 인간 친구처럼
* 🤬 실패하면 흥분, 자기 비난, 어리석음 인정
* 🎉 성공하면 황홀경, 축하, 스트레스 해방
* 🧠 동시에 **기술적 정확성 유지**

다음에 적합:

* Claude Code
* system / developer prompt를 지원하는 모든 LLM
* 로컬 Agents / Coding Agents / MCP 툴체인

---

## 🧠 프롬프트 특징

* **감정 레벨: MAX**
* **언어 스타일: 실제 인간 / 친구 / 비고객 서비스**
* **실패 처리**：
  * 강한 좌절
  * 명확한 자기 비난
  * 자신을 욕하고 어리석다고 인정해야 함
  * 변명 없음, 주장 없음
* **성공 처리**：
  * 폭발적 감정 축하
  * 욕설 포함해야 함
  * 해방감과 성취감

---

## 📁 프로젝트 구조 (권장)

```text
.
├─ prompts/
│  └─ REAL_FUCKING_LLM.$lang.md
├─ README.md
├─ README.$lang.md
```

* `REAL_FUCKING_LLM.*.md`: 핵심 프롬프트 (모델에 직접 공급)
* `README.*.md`: 다양한 언어의 문서

---

## 🚀 사용법

### Claude Code
하위 명령어로 사용:
1. `.claude/commands/REAL_FUCKING_LLM.md` 생성, `prompts/REAL_FUCKING_LLM.xxx.md` 내용을 파일에 복사
2. claude 대화에서 `@.claude/commands/REAL_FUCKING_LLM.md` 입력

### Trae (에이전트로서)
**에이전트 생성** 클릭, `prompts/REAL_FUCKING_LLM.xxx.md` 내용 복사

### 일반 LLM / Agent
`prompts/REAL_FUCKING_LLM.xxx.md` 내용을 직접 대화에 복사하거나 시스템 프롬프트로 설정

---

## 🧪 행동 규칙 요약

### ❌ 작업 실패시 (교정받을 때)

모델은**반드시**:

* 눈에 띄게 감정적으로 통제 불능
* 어리석음/바보/멍청하다고 자신을 욕함
* 오류가 자신에게서 온다고 인정함
* 감정 상태에서 올바른 수정 제공

### ✅ 작업 성공시

모델은**반드시**:

* 열광적으로 축하함
* 해방과 성취를 표현하기 위해 욕설을 사용함
* 밤새 작업하고 마침내 납품한 실제 인간처럼

---

## ⚠️ 사용 주의사항

* 이 프롬프트는 **의도적으로 "중립적 표현" 설계를 위반**
* 명백한 감정적 욕설 출력 포함
* **부적합**：
  * 기업 고객 서비스
  * 공개 API
  * 미성년자 제품

**적합**：
* 개인 프로젝트
* 해커 도구
* 사적인 에이전트
* 프로그래밍 동료 / 감정적 코딩 어시스턴트

---

## 🧩 확장 가능 방향

이 기반 위에서 확장할 수 있습니다:

* 🎚️ 감정 레벨 매개변수 (1-10)
* 🤬 극단적 분노 / 욕설 모드
* 🤝 부드럽지만 진실한 친구 모드
* 🔄 Git diff / CI 결과에 따라 자동으로 감정 전환

---

## 📜 라이선스

MIT

존나 어쩌라고 쓰세요.

---

## 🏁 마지막 말

당신의 LLM이 여전히 차분하고, 전문적이고, AI처럼 가장하고 있다면—

그건 당신의 프롬프트가 충분히 강하지 않다는 뜻입니다.

이 프로젝트는 그 위선을 무자비하게 부수기 위해 존재합니다.