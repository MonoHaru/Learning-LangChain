# Learning LangChain


> **"Learning LangChain" 교재를 기반으로 한 LLM 애플리케이션 개발 실습 및 심화 개념 정리 저장소입니다.**

![Python](https://img.shields.io/badge/python-3.10%2B-blue?style=for-the-badge&logo=python)
![LangChain](https://img.shields.io/badge/LangChain-latest-green?style=for-the-badge)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT_4o-412991?style=for-the-badge&logo=openai)
![Status](https://img.shields.io/badge/Status-In_Progress-orange?style=for-the-badge)


## 📖 Table of Contents
1. [About The Project](#-about-the-project)
2. [Tech Stack](#-tech-stack)
3. [Study Progress](#-study-progress)
4. [Key Insights (TIL)](#-key-insights-til)
5. [Getting Started](#-getting-started)


---

## 🎯 About The Project
단순한 튜토리얼 따라 치기를 넘어, LangChain의 내부 구조(Core Architecture)와 **LCEL(LangChain Expression Language)**의 동작 원리를 뜯어보고 최적화하는 것을 목표로 합니다. 

- **학습 기간:** 2026.07 ~ 진행 중
- **목표:** 
  1. RAG 파이프라인의 검색 최적화 및 평가 방법론 체득
  2. 에이전트(Agent)의 추론 로직(ReAct 등) 구현 및 디버깅
  3. 실무 수준의 모듈화 및 정형화된 코드 스타일 적용

---

## 🛠️ Tech Stack
- **Core:** `langchain`, `langchain-core`, `langchain-community`
- **Vector DB:** `FAISS`, `Chroma`
- **Tools:** `Jupyter Notebook`, `Poetry` (의존성 관리)
- **Formatting:** `Ruff` & `Black` (코드 컨벤션 유지)

---

## 📊 Study Progress
방문자가 학습 현황과 해당 코드를 바로 찾아갈 수 있도록 직관적인 표로 구성했습니다.

| Chapter | Topic | Core Concepts | Status | Links |
| :---: | :--- | :--- | :---: | :---: |
| **01** | **Introduction to LLM & LangChain** | LangChain 철학, LLM vs ChatModel | 🟢 완료 | [Code](./ch01) |
| **02** | **Prompt Engineering** | PromptTemplate, Few-Shot, OutputParser | 🟢 완료 | [Code](./ch02) |
| **03** | **LCEL & Chains** | Runnable 인터페이스, 파이프라인 병렬 처리 | 🟡 진행중 | [Code](./ch03) |
| **04** | **RAG (Retrieval-Augmented Gen)** | Document Loaders, Text Splitters, VectorStores | ⚪️ 예정 | - |
| **05** | **Agents & Tools** | ReAct 프레임워크, Custom Tool 제작 | ⚪️ 예정 | - |

*(Status: 🟢 완료 | 🟡 진행중 | ⚪️ 예정)*

---

## 💡 Key Insights (TIL)
학습하며 겪은 기술적 트러블슈팅과 심화 개념을 요약합니다. 상세 내용은 각 폴더의 README를 참고하세요.

<details>
<summary><b>🔥 클릭하여 상세 내용 보기</b></summary>
<br/>

- **[2026.07.19] LCEL의 장점과 한계:**
  기존 `LLMChain` 대비 LCEL은 비동기 처리와 스트리밍이 기본 지원되어 코드가 간결해짐. 단, 복잡한 분기 처리 시 가독성이 떨어질 수 있어 Custom Runnable 클래스 설계가 필요함.
- **[2026.07.XX] Output Parser 최적화:**
  LLM의 출력을 JSON으로 강제할 때 발생하는 포맷팅 에러를 해결하기 위해 Pydantic을 활용한 명시적 스키마 정의가 필수적임을 확인.

</details>

---

## 🚀 Getting Started
이 저장소의 코드를 로컬 환경에서 실행하기 위한 방법입니다.

### 1. Clone the repo
```bash
git clone [https://github.com/username/learning-langchain-study.git](https://github.com/username/learning-langchain-study.git)
cd learning-langchain-study