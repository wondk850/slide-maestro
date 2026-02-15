# 🎬 Slide Maestro — YouTube → NotebookLM Slide Prompt Generator

> **YouTube 영상 URL만 넣으면, AI가 분석해서 디자인 + 콘텐츠 구조까지 통제하는 완성형 슬라이드 프롬프트를 자동 생성합니다.**

![Gemini](https://img.shields.io/badge/Google%20Gemini-Gem-blue?logo=google&logoColor=white)
![NotebookLM](https://img.shields.io/badge/NotebookLM-Slides-purple)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 🤔 이게 뭔가요?

NotebookLM에서 슬라이드를 만들 때, **디자인 스타일도 모르겠고, 몇 장으로 어떤 흐름으로 만들지도 모르겠다면?**

**Slide Maestro**는 Gemini Gem으로, YouTube 영상을 분석해서:

1. 🔍 **콘텐츠 유형, 톤, 키워드를 자동 파악**
2. 🎯 **10개 맞춤 템플릿 중 최적 TOP 3 추천**
3. ✨ **슬라이드 번호별 콘텐츠 목차 + 디자인 스타일을 결합한 완성형 프롬프트 생성**
4. 🌐 **한국어+영어 동시 출력**

### 💡 핵심: 단순 디자인 템플릿이 아닙니다

기존 도구들은 "색상, 폰트, 스타일"만 알려줍니다. **Slide Maestro는 Slide 1부터 Slide N까지 각각 어떤 내용이 들어가야 하는지 콘텐츠 구조까지 통제합니다.**

```
❌ 기존: "테크 다크 스타일로 만들어줘" → NotebookLM이 알아서 → 엉뚱한 결과
✅ 마에스트로: "테크 다크 + Slide 1~15 각각 이 내용" → NotebookLM 완벽 통제
```

---

## 🚀 사용 방법

### 방법 1: Gemini Gem으로 사용 (추천)

1. [Google Gemini](https://gemini.google.com/) 접속
2. **Gem 만들기** 클릭
3. `slide_maestro_system_prompt.md` 내용 전체를 **시스템 프롬프트**에 붙여넣기
4. YouTube URL 입력 → 끝! 🎉

### 방법 2: NotebookLM 소스로 업로드

1. [NotebookLM](https://notebooklm.google.com/) 접속
2. `slide_maestro_system_prompt.md` 파일을 **소스로 업로드**
3. "이 디자인 시스템을 기반으로 YouTube 영상을 분석해줘"라고 요청

---

## 📋 10개 맞춤 템플릿

| # | 템플릿 | 적합한 콘텐츠 | 참조 스타일 |
|---|--------|-------------|------------|
| 1 | 🖥️ **테크 다크** | AI, AGI, 딥러닝, 코딩 | Apple Keynote × DeepMind |
| 2 | 🏗️ **어반 블루프린트** | GTX, 재건축, 도시계획, 철도 | 건축 도면 × 공학 노트북 |
| 3 | 📰 **에디토리얼 모던** | 지정학, 역사, 국제정치 | The Economist × Foreign Affairs |
| 4 | 💰 **파이낸셜 프로** | 경제, 투자, 금리, 환율 | Goldman Sachs × Bloomberg |
| 5 | 📚 **교육 클린** | 영어, 수능, 문법, 언어학 | Khan Academy × Notion |
| 6 | 👤 **인물 프로필** | CEO, 리더, 인터뷰, 전기 | TIME 매거진 × TED |
| 7 | 📖 **미니멀 북** | 독서, 자기계발, 철학 | 무인양품 × Apple 여백 |
| 8 | 🔬 **사이언스 그리드** | 뇌과학, 물리, 바이오 | MIT Media Lab × Nature |
| 9 | 🏛️ **공식 리포트** | 정책, 행정, 예산, 법률 | 정부 보고서 × 국회 브리핑 |
| 10 | 💥 **임팩트 원샷** | 핵심 한 줄 요약, 소셜 공유 | Y Combinator × Nike |

---

## 💡 작동 원리

```
YouTube URL 입력
    ↓
Gemini가 영상 자동 분석
(콘텐츠 유형 / 톤 / 데이터 밀도 / 키워드)
    ↓
10개 템플릿 중 TOP 3 추천 + 적정 슬라이드 장수 제안
    ↓
선택한 템플릿으로 [디자인 + 콘텐츠 구조] 완성형 프롬프트 생성
(Slide 1~N 각각의 제목과 핵심 메시지 매핑)
    ↓
NotebookLM에 붙여넣기 → 슬라이드 생성!
    ↓
마이크로 에디팅: "N번 슬라이드 수정해줘" → 해당 슬라이드만 재작성
```

---

## 🛠️ 워크플로우

| 단계 | 누가 | 무엇을 |
|------|------|--------|
| **STEP 1** | 유저 | YouTube URL + 장수/타깃/톤 지정 |
| **STEP 2** | 마에스트로 | 영상 분석 → 템플릿 추천 → 슬라이드별 콘텐츠 매핑 프롬프트 생성 |
| **STEP 3** | 유저 | 프롬프트를 NotebookLM에 복붙 → 슬라이드 생성 |
| **STEP 4** | 유저+마에스트로 | 특정 슬라이드만 수정 요청 → 해당 부분만 재작성 |

---

## 📁 파일 구조

```
slide-maestro/
├── README.md                          # 이 파일
├── LICENSE                            # MIT License
└── slide_maestro_system_prompt.md     # Gemini Gem 시스템 프롬프트 (핵심)
```

---

## 🙏 크레딧

- 슬라이드 디자인 프롬프트 참조: [awesome-notebookLM-prompts](https://github.com/serenakeyitan/awesome-notebookLM-prompts)
- 개발 도구: [Antigravity AI](https://github.com/google-deepmind)

---

## 📄 License

MIT License - 자유롭게 사용하세요!
