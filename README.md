# 👨‍🏫 DialogSum: A Real-life Scenario Dialogue Summarization
목적 : 일상 대화 텍스트의 맥락을 파악하여 핵심 요약문을 생성

## 👨‍👧‍👦 Team 
<table align="center">
  <!-- 상단 팀원 이름 Table-->
  <tr>
    <th align="center">👑 이진성</th>
    <th align="center">🙍 박세희</th>
    <th align="center">🙍 서효림</th>
    <th align="center">🙍‍♂ 유창준</th>
    <th align="center">🙍‍♂ 이건우</th>
  </tr>
  
  <!-- 팀원 이미지 Table-->
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/a9befe05-0cb9-4e0c-ba1f-43b4275ce55e" width="130">    <!--이진성-->
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/8640b497-ee8b-426f-b314-e6681ac5e0a6" width="130">    <!--박세희-->
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/5b02c89e-5860-43a6-9adc-d1e2944952f6" width="115">    <!--서효림-->
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/11d4493f-10d3-4342-8bc8-3c78353626e1" width="130">    <!--유창준-->
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/11d4493f-10d3-4342-8bc8-3c78353626e1" width="130">    <!--이건우-->
    </td>
  </tr>

  <!-- 팀원 역할 Table-->
  <tr>
    <!--이진성-->
    <td align="center">
      EDA <br>
      Data Preprocessor <br>
      Modeling
    </td>
    <!--박세희-->
    <td align="center">
      EDA <br>
      Data Preprocessor <br>
      Modeling
    </td>
    <!--서효림-->
    <td align="center">
      EDA <br>
      Data Preprocessor <br>
      Modeling
    </td>
    <!--유창준-->
    <td align="center">
      EDA <br>
      Data Preprocessor <br>
      Modeling
    </td>
    <!--이건우-->
    <td align="center">
      EDA <br>
      Data Preprocessor <br>
      Modeling
    </td>
  </tr>

  <!-- GitHub URL-->
  <tr>
    <td align="center">
      <a href="https://github.com/wlstjd6524"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>        <!--이진성-->
    </td>
    <td align="center">
      <a href="https://github.com/carolinespwork"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>    <!--박세희-->
    </td>
    <td align="center">
      <a href="https://github.com/S202010741"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>        <!--서효림-->
    </td>
    <td align="center">
      <a href="https://github.com/NullXeronier"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>      <!--유창준-->
    </td>
    <td align="center">
      <a href="https://github.com/lgw2000"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>           <!--이건우-->
    </td>
  </tr>

</table>


## 📺 Presentation
[발표자료](https://github.com/user-attachments/files/27059403/NLP3._.pptx)


## 📂 ReadME Index 
[🎯 Project Overview (프로젝트 개요 및 목표)](#project-overview) <br>

[⏱️ Project Duration & 🔧 Tech Stack (기간 및 기술스택)](#projectduration-techstack) <br>

[📊 Data Analysis & Hypothesis (데이터 분석 및 실험 방향성 설정)](#data-analysis) <br>

[🚀 Experimental Progression (실험 과정 및 빌드업)](#experimental-progression) <br>

[🧪 Final SOTA Architecture & Result (핵심 실험과 최종 아키텍처 및 최종결과)](#final-sota-architecture) <br>

[🛠️ Troubleshooting & Engineering (문제 해결 및 인프라 안정화)](#troubleshooting-engineering) <br>

[👥 Team Leadership & Management (팀 리더십 및 협업)](#teamleadership-management) <br>

[📈 Retrospective & Future Work (회고 및 향후계획)](#retrospective-futurework)


<a id="project-overview"></a>

## 🎯 Project Overview
### 프로젝트 배경
- 본 프로젝트는 일상 대화부터 벌률, 의료 등 복잡한 도메인을 아우르는 다중 턴(Multi-turn) 한국어 대화 데이터를 기반으로, 제3자 관점의 핵심 요약(1~2 문장)을 생성하는 <b>추상적 요약 모델 파이프라인 구축</b> 을 목표로 합니다.
- 단순히 베이스라인 모델을 파인튜닝하는 것을 넘어, 데이터의 질적 향상과 제한된 컴퓨팅 자원 내에서의 학습 효율성을 극대화하는 <b>실험 주도형 접근</b> 을 채택했습니다.

### 핵심 과제
- 복잡한 Multi-turn 문맥 내 팩트 일관성 유지 : 여러 화자가 교자하는 환경에서 화자 간의 의도와 결정 사항을 왜곡 없이 추출하고, 원본 데이터의 특성을 보존하는 최적의 Prompt 및 전처리 파이프라인 설계.
- Long-tail 분포를 가지는 도메인 불균형 해소 : 9,000여 개 이상의 토픽 중 훈련 데이터가 턱없이 부족한 희귀 상황에 대응하기 위해 타겟팅 기반 데이터 증강 전략 수립.
- 제한된 하드웨어 리소스(24GB VRAM) 극복 : 단일 GPU 환경에서 발생하는 OOM(Out Of Memory) 문제를 해결하기 위한 모델 경량화(PEFT/LoRA) 및 Unsloth 라이브러리 도입, 그리고 Response-Only Loss 기반의 메모리 최적화.

### 핵심 평가 지표 및 최적화 목표
단순 하이퍼파라미터 튜닝에 의존하지 않고, 데이터 중심 실험을 달성하기 위해 다음 4가지 평가지표를 핵심 타겟으로 삼고 성능을 개선했습니다.
  - ROUGE-1
  - ROUGE-2
  - ROUGE-L
  - 이 ROUGE Score 를 종합한 Final_Result
  - 생성된 추상적 요약문이 정답과 형태소/단어 단위부터 문장 구조까지 얼마나 일치하는지 재현율(Recall) 기반으로 측정


<a id="projectduration-techstack"></a>

## ⏱️ Project Duration & 🔧 Tech Stack
### ⏱️ Project Duration
- 2026.02.26 ~ 2026.03.12

### 🔧 Tech Stack
| Category | Tech Stack |
| :--- | :--- |
| **Language** | Python 3.10 |
| **Hardware** | Single GPU (NVIDIA RTX 3090, 24GB VRAM) |
| **Deep Learning Framework** | PyTorch, Hugging Face (transformers) |
| **LLM Models (Encoder-Decoder)**| KoBART |
| **LLM Models (Decoder-Only)** | Solar Pro 10.4B, Qwen3 14B |
| **LLM Optimization (경량화)** | PEFT (LoRA), Unsloth |
| **Data Augmentation (증강)** | Solar Pro3 API, OpenAI API |
| **Data Analysis & EDA** | Pandas, NumPy |
| **Experiment Tracking & Metric** | Weights & Biases (wandb), rouge |
| **Collaboration** | Slack, Zoom |


<a id="data-analysis"></a>

## 📊 Data Analysis & Hypothesis
### 📷 기본 데이터 구성
- Train 12,457 건 / Dev 499 건 / Test : 499 건
- Fetures: `fname`, `dialogue`, `summary`, `topic` 등 결측치(Null) 가 없는 정제된 텍스트 데이터

### Insight 1. 극단적 Long-Tail 불균형과 GIGO 를 고려한 타겟팅 증강









## 🔨 프로젝트 시스템 아키텍처
<img width="2816" height="1536" alt="Image" src="https://github.com/user-attachments/assets/0d8f3399-c906-457b-9fc4-8052d5cd7a97" /> <br>

## 📷 Data 정보
- 학습 데이터 : 약 12,457건
- Dev 데이터 : 약 499건
- Test 데이터 : 약 499건

- 데이터 구성 : fname(식별 고유 아이디), dialogue(원본 대화문), summary(핵심 요약문), topic(대화 주제) <br> <br>


➕ 추가적으로 Solar API 를 통해 다음과 같은 데이터 증강을 진행해봤습니다.
  1. 첫 번째로 Topic 별 부족한 데이터를 채우기 위해 제공받은 학습 데이터 보다 더 많은 약 14,000건의 데이터를 증강해보았습니다. <br>
  다만, 프롬프트 정교화를 하지 못한 상태로 데이터를 긁어오라는 명령어를 주다보니 오히려 성능을 하락시키는 Garbage Data 가 들어와 폐기처리 하였습니다.
  2. 따라서 Few-Shot 프롬프트를 조금 더 정교하게 깎아서 추가적으로 140 건의 훈련 데이터와 처리방식이 거의 동일한 데이터를 증강해보았습니다.


## 📒 EDA
- [EDA노트](https://drive.google.com/file/d/1A18T8T-Yk_U2bPW_zLiIpVDraB-DGdK8/preview)

## 🚀 파이프라인 및 주요 실험
### 0. Special Token 최적화
대화 데이터의 특성을 살려 #Person1#, #Person2# 등의 화자 마스킹 텍스트를 모델의 Special Token으로 정식 등록을 진행해봤습니다. <br>
모델이 이를 단순한 문자열이 아닌 '독립적인 핵심 개체(의미 단위)'로 온전히 이해하도록 유도하였습니다.

---

### 1. EDA 기반 위치 정보 최적화
EDA 결과, 요약문(Summary)의 단어들이 대화문의 '뒷부분'보다는 '앞부분'과 유의미하게 높은 중복도(Overlap)를 보인다는 점을 발견하였습니다. <br>
이를 바탕으로 정보 손실을 최소화하면서 연산 효율을 높이기 위한 입력 텍스트 길이(Max Length) 컷오프 기준을 전략적으로 설정하였습니다.

---

### 2. 특수문자 정제 및 원본 데이터 보존 실험
베이스라인(Baseline) 코드 환경에서 모델의 오인(Misunderstanding)을 방지하고자 특수문자를 제거하거나 대체하는 전처리를 시도했습니다. <br>
그러나 특정 전처리 방식이 오히려 문맥 손실을 야기해 성능 하락으로 이어지는 현상을 발견하였고, 이를 통해 무리한 텍스트 변형보다는 원본 데이터의 특성을 최대한 보존하는 방향으로 학습 전략을 선회하여 실험을 진행했습니다.

---

### 3. 정규식 기반 특수 토큰 정제 및 확장
#Person1# 는과 같이 화자 태그와 조사 사이의 불필요한 공백을 정규식으로 제거하여 로컬 검증 점수(ROUGE) 향상을 이끌어냈습니다. <br>
또한, 기본 제공된 특수 토큰 외에 탐색적 데이터 분석(EDA) 과정에서 발견된 #Price#, #Person4~7# 등을 토크나이저에 추가 등록하여, 토크나이저가 핵심 화자 태그를 임의로 분절(Subword Tokenization)하는 현상을 완벽하게 방지했습니다. <br>
반면, 0.01% 미만으로 등장하는 'ㅋㅋ', 'ㅠㅠ' 등의 이모티콘은 모델에 미치는 영향이 미미하다고 판단하여 원본을 유지했습니다.

---

### 4. 임베딩 기반 동적 퓨샷(Dynamic Few-Shot) 프롬프팅 도입
Solar API 활용 시, 초기에는 TF-IDF나 토픽 예측을 시도했으나 예측 오류가 요약 품질 하락으로 직결되는 문제를 겪었습니다. <br>
이를 해결하기 위해 multilingual-e5-base 임베딩 모델을 활용하여, 현재 입력된 대화문과 의미적으로 가장 유사한 정답 대화쌍을 검색(Semantic Search)하여 Few-Shot 예시로 동적 제공하는 방식을 채택했습니다.

---


## 🚨 문제 및 인사이트 도출
### 1. 베이스라인 모델의 전처리 도입 문제
#### 문제
초반 모델 학습 시 대화 데이터 내부에 규칙 없는 화자 표기, 불필요한 특수문자 등 노이즈가 많아 모델이 대화의 맥락과 핵심을 제대로 파악하지 못하는 현상이 발생하였습니다.

#### 해결
팀원과 같이 진행한 EDA 를 통해서 아래와 같은 초기 전처리 파이프라인을 구축하였습니다.

1-1. 화자 태규 정규화 (Speaker Normalization) : 'A:', '1번:', 'Person A' 등으로 파편화되어 있던 화자 기호를 모델이 역할극으로 인식하기 가장 좋은 표준 형태인 #Person1#, #Person2#... 등으로 완벽하게 통일하였습니다.
1-2. 특수문자 및 노이즈 정제 : 요약의 핵심 의미에 기여하지 않는 불필요한 연속 공백, 탭(Tab), 의미 없는 기호(HTML 의 <br> Tag 등..)등을 정규표현식(Regex)을 활용해 일괄 정제하였습니다.
1-3. 길이 기반 이상치 필터링 (Outlier Removal) : 대화가 너무 짧아 문맥 추론이 불가능한 데이터나, 모델이 최대 토큰 제한을 초과하여 학습에 방해가 되는 비정상적으로 긴 데이터를 EDA 를 통해 탐지 및 과감하게 Cut-Off,

#### 인사이트
화려한 최신 모델링이나 복잡한 튜닝 기법 이전에, '정제된 순도 100%의 Data' 를 만드는 기본기로 베이스라인 보다 조금 더 높은 점수를 얻게되는 접근법, 특히 '글자' 라는 데이터를 어떤식으로 전처리 해야하 하는지에 대한 맥락을 이해하고 'Garbage In, Garbage Out' 이라는 데이터의 중요성을 이해하게 되었습니다.

---

### 2. 하드웨어 리소스 부족 현상
#### 문제
단일 GPU(24GB) 환경에서 10B 이상의 거대 LLM(Solar, Qwen3)을 파인튜닝하려다 보니 끝없는 OOM (Out of Memory) 에러가 발생하였습니다.

#### 해결
PEFT(LoRA) 기법을 도입하고, Batch Size 를 1로 줄이는 대신 'gradient_accumulation_steps=32' 를 적용하였습니다.. 최종적으로 Unsloth 라이브러리를 도입하여 VRAM 사용량을 극한으로 줄이고 학습 속도를 2배 이상 올려보았습니다.

### 인사이트
제한된 자원 속에서도 효율적인 메모리 관리 기법과 최적화 라이브러리를 적극적으로 서치하고 도입하면 거대 모델도 충분히 다를 수 있다는 엔지니어링 역량 확보하였습니다.

---

### 3. 모델 학습 방식의 전환 : Response-Only Loss
#### 문제
SOLAR 모델 로컬 테스트 대비 리더보드 점수가 하락되는 현상 및 모델이 질문(Prompt) 까지 학습하려다 요약 퀄리티가 떨어지는 현상을 발견하였습니다.

#### 해결
Hugging Face 의 최신 트렌드를 파악해서 ChatML 템플릿을 명확히 적용하고, 질문은 마스킹 처리해서 오직 정답(요약문)만 학습하게 만드는 Response-Only Loss 를 도입해봤습니다.

#### 인사이트
모델에게 무작정 텍스트를 넣는게 아니라, '무엇을 학습해야 하는지' 목적 함수를 명확히 깎아주는 것이 성능 폭발의 중요한 요소 중 하나라는 것을 확인했습니다.

---

### 4. 로컬 환경 설정 및 라이브러리 의존성 충돌 해결
#### 문제
모델 코드를 작성하는 시간보다 로컬 환경 내 라이브러리 버전 충돌(CUDA, PyTorch 등) 및 환경 세팅 오류를 해결하는 데 예상치 못한 많은 리소스가 소모되었습니다.

#### 해결
에러 로그를 끈질기게 추적하며 라이브러리 간의 의존성 문제를 하나씩 격파하고, LLM 구동을 위한 안정적인 로컬/서버 베이스 환경을 최종적으로 구축하였습니다.

#### 인사이트
화려한 모델링 이전에 '안정적인 개발 환경 구축'이 실무 프로젝트의 가장 중요한 첫 단추임을 뼈저리게 체감하였습니다. <br>
향후 실무에서도 언제든 발생할 수 있는 이슈인 만큼, 가상환경이나 컨테이너(Docker) 등 인프라 및 백그라운드 지식을 탄탄히 쌓아야 한다는 경각심과 방향성을 얻었습니다.

---

### 5. 특정 토픽 편향성(데이터 불균형) 및 리소스 한계 극복 시도
#### 문제
EDA 분석 결과 '음식 주문' 등 특정 토픽에 데이터가 과도하게 편향되어 있는 불균형 문제를 확인하였고, 이로 인해 모델의 범용적인 요약 성능이 저하될 우려가 있었습니다. <br>
또한, 이를 해결하기 위해 대형 모델과 복잡한 검증 방식을 도입하는 과정에서 서버 메모리 부족(OOM) 현상이 빈번하게 발생했습니다.

#### 해결
컴퓨터 비전(CV) 분야에서 널리 활용되는 K-Fold 교차 검증 및 앙상블(Ensemble) 기법을 자연어 처리(NLP) 파이프라인에 과감하게 접목하여, 편향된 데이터에 대한 모델의 과적합(Overfitting)을 방지하고자 시도했습니다.

#### 인사이트
데이터 불균형을 해소하기 위한 앙상블 전략의 아이디어는 유효했으나, LLM과 같이 무거운 거대 모델 환경에서 K-Fold를 돌릴 경우 서버 자원(VRAM) 관리가 프로젝트의 성패를 가르는 핵심 변수임을 깨달았습니다. <br>
성능 향상 기법과 컴퓨팅 리소스 사이의 트레이드오프(Trade-off)를 정밀하게 컨트롤하는 능력이 필수적임을 깊이 체감했습니다.

---

### 6. 직관에 의존한 룰 기반 로직의 함정과 데이터 기반 의사결정
#### 문제
요약문의 자연스러움을 위해 화자 태그(#Person1# 등)를 가상 이름으로 치환하는 자체 함수(infer_roles())를 개발하고, 'Topic' 키워드를 프롬프트에 강제로 포함시키려 시도했습니다. <br>
그러나 역할 유추 성공률이 60%에 불과했고, 오히려 LLM이 Few-Shot 예시의 가상 이름을 그대로 베껴 쓰는 환각(Hallucination) 병목 현상이 발생하여 점수가 하락했습니다.

#### 해결
철저한 EDA를 통해 실제 정답 요약 데이터의 82.4%가 특수 태그(#Person#)를 그대로 유지하고 있으며, 요약문의 길이가 대화 길이의 약 20% 수준으로 콤팩트하게 압축된다는 객관적 지표를 확인했습니다. <br>
이에 가상 이름 치환 로직을 전면 폐기하고, 디코더의 최대 길이를 50으로 하향 조정했으며 프롬프트에 "대화 전체 설명이 아닌 핵심 행동 하나만 20단어 이하로 요약하라"는 명확한 통제 지시문을 삽입하여 성능을 복구했습니다.

#### 인사이트
LLM 프롬프트 설계나 전처리 로직은 개발자의 '직관(자연스러울 것이라는 추측)'이 아닌, 철저하게 '데이터의 통계적 패턴(EDA 지표)'을 근거로 이루어져야 함을 깊이 체감했습니다.

---

### 7. 외부 API 속도 제한(Rate Limit) 대응
#### 문제
API를 활용한 모델 앙상블 과정에서 분당 요청 수(RPM) 제한으로 인해 지속적인 에러가 발생했으며, 제출 마감 시간이 임박한 상황에서 전체 프로세스가 중단될 위기에 처했습니다.

#### 해결
스크립트 내에 '60건 처리 후 60초 대기'하는 예외 처리 및 타임아웃 방어 로직을 긴급하게 추가하여 안정적인 추론 파이프라인을 구축했고, 마감 직전에 무사히 제출을 완료했습니다.

#### 인사이트


---


## 📈 결과

### Leader Board
<img width="981" height="391" alt="Image" src="https://github.com/user-attachments/assets/95b75ebe-059f-43a1-914f-dfc97874ae9d" />
Rank 3 🥉


## 📚 Presentation
- [발표자료](https://github.com/AIBootcamp20/dialogue-summarization-nlp_3/blob/main/Code/%EC%9D%B4%EC%A7%84%EC%84%B1/Announcement/NLP3%EC%A1%B0_%EB%B0%9C%ED%91%9C%EC%9E%90%EB%A3%8C.pdf)


## 🔎 프로젝트 한계 및 개선사항
### 1. 데이터 증강의 양날의 검 (프롬프트 엔지니어링의 중요성)
### 한계
데이터 부족을 해결하기 위해 초기 증강을 시도했으나, 성능이 대폭 하락하는 이슈 발생가 발생하였습니다.

### 시도 및 접근
원인을 분석해 보니 프롬프트가 정교하지 못해서 LLM 이 기존 포맷에 맞지 않는 노이즈 데이터를 대량 생성하였습니다. <br>
이후 LIMA 법칙을 참고하여, 양보다는 질을 높이기 위해 Few-Shot 프롬프트를 아주 정교하게 깎고, JSON 파싱 에러 방어까지 구축하여 고퀄리티 타겟팅 증강 코드를 완성했습니다.

### 한계 및 아쉬운 점
시간(GPU 마감일 및 대회 마감일) 관계쌍 완벽하게 세팅된 고퀄리티 증강 데이터를 SOTA 모델에 최종적으로 태워보지 못하고 마무리한게 된 점이 가장 아쉬웠습니다.

### 인사이트
데이터 증강은 무조건적인 Score 향상에 대한 정답은 아니며, 데이터의 품질(Quality)을 통제하지 못하는 증강은 안 하느니만 못하다는 교훈을 얻게되었습니다.

---

### 2. 초기 모델(KoBART) 고착화 및 최신 LLM 도입 지연
### 한계
LLM 파인튜닝 프로젝트가 처음이다 보니, 초기 베이스라인으로 설정했던 소형 모델(KoBART)의 성능을 영혼까지 끌어올리는 데에만 프로젝트 후반부까지 너무 많은 시간을 할애하였습니다.

### 시도 및 접근
KoBART의 한계를 돌파하기 위해 다양한 하이퍼파라미터 튜닝과 전처리를 시도했으나 성능의 천장(Ceiling)에 부딪히게 되었습니다. <br>
이후 프로젝트 후반부에 과감하게 체급이 큰 최신 LLM(SOLAR, Qwen)으로 전환을 시도해봤습니다.

### 한계 및 아쉬운 점
다른 아키텍처나 더 큰 파라미터를 가진 최신 모델을 시도해 볼 타이밍을 너무 늦게 잡은게 아쉬웠습니다. <br>
또한 최신 모델로 전환한 후 성능이 대폭 상승하는 것을 보며, 초반에 시야를 더 넓게 가지지 못한 점이 큰 아쉬움으로 남음.

### 인사이트
다음 프로젝트부터는 한 모델에 매몰되기보다는, 초반에 최신 연구 동향(SOTA)을 빠르게 리서치하여 유망한 후보 모델 2~3개를 선정한 뒤, '빠른 프로토타이핑(Quick Prototyping)'을 통해 가장 잠재력 있는 엔진을 먼저 찾아내는 전략을 취해야 함을 배우게 되었습니다.

---

### 3. 베이스라인 모델의 성능 천장(Ceiling)과 파이프라인 전환 타이밍
### 한계
기존 베이스라인 소형 모델을 튜닝하는 과정에서 더 이상 점수가 오르지 않는 구조적인 성능 한계점(Ceiling)에 도달했음을 느꼈습니다.

### 시도 및 접근
이 한계를 타파하기 위해 프로젝트 후반부에 파라미터 규모가 크고 한국어 이해도가 높은 SOTA LLM(SOLAR)으로 모델 전환을 과감히 시도했습니다.

### 한계 및 아쉬운 점
SOLAR 모델의 학습 및 하이퍼파라미터 튜닝에 필요한 물리적인 시간(GPU 구동 시간)이 턱없이 부족하여, 해당 모델의 잠재력을 리더보드 점수로 끝까지 확인하지 못한 채 마무리하게 된 점이 뼈아픈 아쉬움으로 남습니다.

### 인사이트
특정 기법이나 모델의 성능이 확실한 한계에 봉착했다고 판단될 때, 매몰 비용(Sunk Cost)에 얽매이지 않고 다음 단계(새로운 모델이나 구조)로 빠르게 피벗(Pivot)하는 **'Agile(민첩한) 시간 관리와 결단력'**이 제한된 기간의 AI 프로젝트에서 가장 중요한 전략임을 뼈저리게 느꼈습니다.

---

### 4. 인코더-디코더 모델의 구조적 한계와 대형 모델(Unsloth)로의 전환 및 학습 안정성 과 체크포인트 관리 부재
### 한계
초기에는 멀티턴 대화의 양방향 문맥 파악에 유리할 것이라 판단하여 인코더-디코더 구조의 KoBART를 베이스라인으로 채택하고 Optuna를 통해 하이퍼파라미터 탐색을 진행했습니다. <br>
그러나 주어와 목적어가 뒤바뀌어 요약되는 치명적인 할루시네이션(ROUGE-1=0.0 케이스 발생)이 구조적으로 반복되었습니다. <br>
또한 모델 학습 관리 측면에서 Qwen3 모델 학습 도중 예기치 않게 서버가 강제 중단되는 사고가 발생했습니다. <br>
당시 중간 가중치를 저장하는 체크포인트 로직을 구현해두지 않아, 처음부터 다시 학습을 돌려야 하는 막대한 리소스와 시간 손실을 겪었습니다.

### 시도 및 접근
KoBART 아키텍처 자체의 상한선을 인지하고, 이를 돌파하기 위해 디코더 온리(Decoder-only) 기반의 거대 모델인 Qwen3-8B를 도입했습니다. <br>
제한된 GPU 환경 속에서도 8B 이상의 파라미터 튜닝이 가능하도록 Unsloth 라이브러리와 LoRA 기법을 적극 활용하여 모델의 체급을 성공적으로 높였습니다.

### 한계 및 아쉬운 점


### 인사이트
장시간 소요되는 LLM 파인튜닝 환경에서는 서버 중단 현상을 언제든 발생할 수 있는 기본 상수로 간주해야 합니다. <br>
향후 프로젝트에서는 특정 스텝(Step)이나 에폭(Epoch) 단위로 모델의 상태를 자동 저장하는 세이프티 넷(Safety Net) 구축이 최우선 필수 작업임을 뼈저리게 배웠습니다.

---

### 종합 인사이트 
- 좋은 데이터는 좋은 모델의 결과를 뽑아준다는 사실과, 무작정 데이터 증강이 모델 성능을 무조건 적으로 높이는 사실은 아니라는 점들로 데이터의 소중함을 다시 한번 더 느꼈던 것 같습니다.
- 좋은 실험과 그리고 그런 것을 시도하기 위해서는 환경 셋팅이 잘 되어져야 한다고 생각했고, 그리고 그런 환경을 지원하는 자원 리소스에 대한 관리에 대한 라이브러리 사용이나 관리법도 중요하다 라는 걸 느꼈습니다.
- 이번 기회를 통해서 사람이 데이터를 바라볼 때 직관적으로 이거는 성능이 오를 것 같다고 한 지표가 무조건적으로 성능향상에 기여하지는 않다 라는 점을 한번 더 느끼게 되었고, 냉철하게 데이터를 바라봐야 되겠다는 생각이 들었습니다.
- 현업에서 강조했던 '시간' 과 '인력 자원 비용' 그리고 '리소스 자원 한계' 의 3가지 문제점을 몸소 느낄 수 있었습니다.


## 📍 회고
👑 이진성 : 딥러닝 프로젝트의 파이프라인에 대한 개념이 고착화 된 상태에서 텍스트를 받아들이는 프로젝트를 진행하면서 많은 점을 느꼈던 요약 생성 대회 였던 것 같습니다. 특히 사진을 전처리 하는 요소보다 '글자' 라는 개념은 우리가 평상시에 사용하는 학문이다 보니 전처리에 대한 전략이나 데이터를 이해하는데 많이 어려움이 없겠다 라는 생각을 가지고 뛰어들었는데 실제는 이런 생각이 오만함 이였다 라는 점을 느꼈던 것 같습니다. <br>
실질적으로 사람이 바라보는 시선에서만 데이터를 바라보면 어느정도 한계점이 일찍 도달하겠다 라는 생각이 들었고, 다시 한번 데이터를 바라보는 시선은 다양한 방면에서 바라봐야 모델에 높은 점수를 기여할 수 있구나 라는 소중한 GIGO 를 몸소 느껴볼 수 있었던 프로젝트 였던 것 같습니다. <br>
이번 대회를 통해서 '어떤 특정 분야에서 강점을 가지는 모델' 의 중요성보다 '좋은 데이터, 분포도가 골고루 퍼진 데이터' 의 중요성을 깨닫게 되었고, 또 한정된 리소스 자원을 최대한 활용해서 우리가 취하고자 하는 모델을 사이즈에 맞춰 서빙하는 리소스 자원 관리에 대한 여러 인사이트도 얻게 되어서 뜻 깊었던 프로젝트 였던 것 같습니다.

🙍 박세희 : 여러가지로 어려움이 많았던 대회였지만 그만큼 배운점도 많았던것 같습니다. LLM 분야에 대해서 아직 저의 지식과 경험이 많이 부족하다는 것을 느꼈고 매일 빠르게 변하는 기술의 최전선에 있는 분야인만큼 이를 제대로 활용하기 위해선 앞으로 더 많은 노력이 필요하겠다는걸 느끼게 된 시간이었습니다.

🙍 서효림 : KoBART Fine-tuning, LLM Prompt Engineering, LoRA SFT, Embedding Retrieval, 앙상블까지 한 대회 안에서 다양한 방법을 직접 시도하고 비교해본 것도 값진 경험이라고 생각합니다. 비록 서버가 중단되고 시간이 부족하여 Qwen3도 완전히 돌려보지 못해 아쉬움이 남지만, 이런 상황들까지도 임기응변으로 대처하며 1분전 제출을 완료했던 그 순간이 이번 대회를 가장 기억에 남을 것 같습니다.

🙍‍♂ 유창준 : KoBART Fine-tuning,  Cognitive-based Multi-level Augmentation까지 한 대회 안에서 다양한 방법을 직접 시도. 비록 서버가 중단되고 시간이 부족하여 llama3.2 도 완전히 돌려보지 못해 아쉬움이 남지만, 이런 상황들까지도 임기응변으로 대처한 순간이 이번 대회를 가장 기억에 남을 것 같습니다.

🙍‍♂ 이건우 : 다양한 문제속에서 많은 것을 배울 수 있었던 대회였습니다. 특히, 문제에 막혔을 때 한 곳에 지체하기보다 빠르게 다음 단계로 넘어가는 빠른 실행과 전환의 중요성을 체감했습니다.
또한 자연어 분야가 얼마나 빠르게 진화하는지 체감하면서 스스로의 부족함도 많이 느꼈습니다.
속도감 있게 문제를 돌파해 나가야 겠다고 생각하게 되었습니다.


## 👨‍👩‍👧‍👧 협업
#### 🤝 협업일정 및 방식
- 협업일정 : 정규 수업시간 (09시 ~ 18시) 도 중 시간제약 없이 현재 진행상황 실시간 공유 및 18시 수업 종료 전 금일 진행했던 프로젝트 작업내용 공유
- 협업방식 : Slack

- 미팅일정 : 각 개인의 프로젝트 진행율을 반영하여 회의 마지막 진행상황으로 다음 회의 일정 조율하기
- 미팅방식 : 실시간 Zoom 플랫폼을 통한 화면공유 및 실시간 음성 대화
  
<img width="1920" height="1920" alt="Image" src="https://github.com/user-attachments/assets/1431131e-9587-44b5-aa5b-845af4ae2f81" />
<img width="1920" height="1920" alt="Image" src="https://github.com/user-attachments/assets/3bf05246-4e5f-4a12-9e01-ec7eb015031b" />

#### 📋 일정 및 프로젝트 관리 툴

- WAN DB
<img width="1845" height="784" alt="Image" src="https://github.com/user-attachments/assets/f50da561-6647-43f6-9b51-0108c11155b5" />

## 🌐 기술스택
[KoBART] : https://huggingface.co/digit82/kobart-summarization

[Optuna] : https://optuna.org 

[Solar API] : https://developers.upstage.ai

[Multilingual-e5-base] : https://huggingface.co/intfloat/multilingual-e5-base

[Unsloth + Qwen3-8B] : https://github.com/unslothai/unsloth

[Python-mecab-ko] : https://pypi.org/project/python-mecab-ko

[Unsloth] : https://unsloth.ai/docs/models/tutorials
