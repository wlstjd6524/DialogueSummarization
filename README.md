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

---

### Insight 1. 극단적 Long-Tail 불균형과 GIGO 를 고려한 타겟팅 증강
<img width="833" height="471" alt="Image" src="https://github.com/user-attachments/assets/d62434aa-23b4-4ede-bb14-9bfd4c914409" /> <br>

- 분석 : 총 12,457건의 훈련 데이터 내에 무려 9,235개의 고유 토픽이 존재하며, 대다수의 토픽이 단 1~2 건의 데이터만 보유하는 극단적인 Long-Tail 분포를 띄는 걸 확인했습니다. 이는 희귀 상황에 대한 모델의 요약 일반화 성능을 크게 저하시킬 수 있는 치명적 요인이라 판단했습니다.
- 실험방향 : 소수 토픽에 대한 데이터를 보강하기 위해 Solar API 를 활용한 데이터 증강 파이프라인을 구축하려고 했습니다.
    - 시행착오 : 초기에는 Zero-Shot 프롬프트로 약 14,000 건의 대량 증강을 시도했으나, 프롬프트 엔지니어링의 정교함 부족으로 원본 데이터의 형식을 해치는 'Garbage Data' 가 생성됨을 확인하고 전량 폐기했습니다.
    - 해결 및 가설 : 데이터의 양보다 <b>순도</b> 가 중요함을 인지하고, 타겟 토픽에 대해 정답 포맷을 강제하는 Few-Shot 프롬프트 엔지니어링을 적용했습니다. 이를 통해 원본 분포와 완벽히 일치하는 140건의 고품질 데이터를 선별 증강하여, 희귀 토픽에 대한 성능 방어 가설을 수립했습니다.

---

### Insight 2. 요약문의 구조적 패턴 및 압축률 제약
<img width="637" height="563" alt="Image" src="https://github.com/user-attachments/assets/1c5b5974-4d9d-405c-8b35-d7675c297e0c" /> <br>

<img width="865" height="472" alt="Image" src="https://github.com/user-attachments/assets/f568f8a3-0a08-4a40-a6eb-341b2456fdb3" /> <br>

- 분석 : 원본 대화 대비 요약문의 길이 압축률은 평균 23% 수준으로 내용이 매우 밀도 있게 요약됩니다. 특히 요약문의 87%가 단 1~2 문장으로 구성되며, 종결 어미는 압도적으로 "~다" 식으로 끝나는 정형화된 패턴을 볼 수 있었습니다. 대화문 내부에는 `#Person1#` 과 `#Person2` 태그가 100% 등장하여 화자를 구분하는 걸 볼 수 있었습니다.
- 실험방향 : 모델이 단순히 내용을 줄이는 것을 넘어, `1~2 문장 제한`, `~다 식의 종결어미`, `#Person# 화자 태그 유지` 라는 엄격한 포맷팅 룰을 학습하도록 유도해야 한다고 생각했습니다. 추후 프롬프트 설계나 Loss 계산 시 이러한 구조적 제약 조건을 어길 경우 패널티를 부여하는 방향의 최적화가 필요하다는 가설을 세웠습니다.

---

### Insigt 3. 텍스트 노이즈의 통계적 유의성 및 순정 데이터 보존
- 분석 : 모델 성능을 높이기 위해 데이터 전처리를 수립하는 과정에서, 대화문에 포함된 'ㅋㅋ', 'ㅎㅎ' 와 같은 감탄사나 은어의 통계적 분포를 확인했습니다. 그 결과, 전체 데이터셋에서 해당 패턴이 거의 존재하지 않는 무의미한 수치임을 확인했습니다.
- 실험방향 : 텍스트 전처리 과정에서 불필요한 정규식 연산이나 공격적인 HTML 태그 제거 로직은 과감하게 버리기로 결정했습니다. 오히려 과도한 전처리가 Multi-Turn 대화의 문맥적 흐름을 단절시켜 성능 하락을 유발할 수 있겠다는 생각을 했고, 원본 데이터의 통계적 특성과 구조를 최대한 보존해서 모델에 학습시키는 방향으로 실험을 전개하려고 했습니다.


<a id="experimental-progression"></a>

## 🚀 Experimental Progression
### Phase 1. KoBART Baseline & Hyper-Optimization
- Special Token 최적화 : `#Person1#`, `#Price#` 등 대화 내 핵심 개체를 단순 문자열이 아닌 독립적 의미 단위로 인식하도록 토크나이저를 확장(30,000 -> 30,022)하여 NER 손신을 방지하고자 했습니다.
- EDA 기반 시퀀스 확장 (Max Length 512 -> 1024) : 요약 핵심 단서가 대화 전반부에 집중되어 있다는 점과 95% 커버리지를 고려해서 전략적으로 컷오프를 다음과 같이 설정하였습니다.
- Minimal Cleansing 전략 : 무리한 특수문자 (HTML의 <br> 태그나 ㅋㅋ, ㅎㅎ 같은 이모지 등..) 제거가 문맥 손실을 유밤함을 확인하고, 원본 데이터를 99% 보존하되 화자 태그와 조사 사이의 공백만 정규식으로 제거하여 ROUGE 점수를 방어하고자 했습니다.

---

### Phase 2. Data-Centric Agile Cycle & Curriculum Learning
모델의 파라미터 튜닝 이전에 데이터의 품질과 학습 구조를 고도화하여 `GIGO` 를 방어하고 성능의 하한선을 끌어올리는 데 집중했습니다.
- 말투 통일(~한다) 및 데이터 경량화 : '정답지' 내 격식체와 해라체가 혼용되어 모델의 Attention 자원이 불필요한 어조 학습에 낭비되는 것을 확인했습니다.

    - 종결 어미를 관찰자 시점(~한다 / 다)으로 100% 통일하고 MaxLength 값을 타이트하게 조정해서 학습 안정성을 확보하려고 했습니다.
- 2-Stage Curriculum Learning 파이프라인 :
    - Stage1 : Solar API 기반 증강 데이터(2.4만건)로 대화 문맥에 대한 일반화 성능확보.
    - Stage2(Precision) : 순정 데이터(1.2만건)로 최종 영점 조절을 수행

    - 하지만 해당 파이프라인 구현 중 초기 실험에서 무작위로 증강한 14,000 건의 데이터가 오히려 모델의 추리 논리를 훼손하고 Score 를 하락시키는 현상을 포착했습니다.
    - 따라서 정성적 분석을 통해 해당 데이터가 `GIGO` 를 유발하는 저품질 노이즈임을 정의하고, <b>1.4만 건의 데이터를 과감히 전면 폐기했습니다.</b>
      - 해결책 : 데이터의 양보다 도메인 정렬이 핵심임을 인지하였습니다. Few-Shot 프롬프팅을 통해 데이터 포맷과 팩트 정합성이 검증된 표본 데이터를 재생성하여 2-Stage 학습을 재수행하고, 모델 요약의 신뢰도를 회복하였습니다.

---

### Phase 3. LLM Pivot & Infra-Resource Engineering
KoBART의 태생적 한계인 화자 혼동을 해결하기 위해, 거대 파라미터 기반의 <b>Decoder-Only</b> 모델로 피벗하여 H/W 제약 돌파 실험을 진행했습니다.

- Dynamic Few-Shot 프롬프팅 : `multilingual-e5-base` 임베딩 모델을 활용, 입력 대화와 의미적으로 가장 유사한 예시를 검색해서 동적 제공함으로써 요약 품질의 일관성을 확보하려고 했습니다.
- Infra Optimization (Unsloth & QLoRA) : 해당 Decoder-Only 모델을 사용하다 보니 단일 24GB VRAM 환경에서 Qwne3-14B, SLOAR-10.7B 모델 로드 시 발생하는 `Out Of Memory` 문제에 직면하였습니다.
    - 해결 : Unsloth 라이브러리를 도입해서 메모리 사용량을 획기적으로 절검하고, 학습 속도를 약 1.6배 향상시킴으로써 제한된 자원 내에서의 거대 모델 학습 가능성을 증명했습니다.
- Analysis : 실험 결과, 파라미터 수의 증가가 본 태스크의 ROUGE Score 상승과 직결되지 않음을 확인했습니다. 이를 통해 "중소규모 도메인 특화 요약에는 최적화된 Ecoder-Decoder 아키텍처가 비용 효율성 면에서 우위에 있다"는 부분과, 더 나아가 모든지 딥러닝이 머신러닝 보다 항상 나은게 아닌 것 처럼 큰모델이 항상 정답은 아니구나 라는 기술적 통찰을 얻게되었습니다.


<a id="final-sota-architecture"></a>

## 🧪 Final SOTA Architecture & Result
### 최종 아키텍처 도출
단일 모델 실험(Stage Phase 1~3) 을 통해 확보한 <b>최적의 시퀀스 길이(1024)</b> 와 <b>말투 통일 및 노이즈 정제 데이터셋</b> 을 프로젝트의 핵심 자산으로 확정했습니다. <br>
이 기반 위에서 모델의 변동성을 최소화하고 리더보드 점수를 극대화하기 위해, 팀 협업을 통해 <b>5-Fold 교차 검증 및 Label Smoothing 전략</b> 을 최종 파이프라인으로 채택했습니다. <br>

### 핵심 기술 스택
- 5-Fold Cross-Validation : 데이터를 5개의 폴드로 나눠서 독립적인 모델 5개를 학습시켰습니다. 이는 특정 검증 셋에 과적합 되는 것을 방지하고, 리더보드의 Private Score 하락을 막는 결정적인 방어 기제가 되었습니다.
- Label Smoothing (factor = 0.1) : 요약문 생성 시 모델이 특정 단어에 과도하게 편향되는 것을 막아, 생성 품질의 유연성을 확보하고 할루시네이션 발생률을 낮추었습니다.
- Inference Optimization : 5개 모델의 예측치를 결합하는 앙상블 추론과 `num_beams=5` 설정을 통해, 단순 생성보다 훨씬 정교하고 팩트에 충실한 요약문을 도출했습니다.

### 🏆 Final Performance & Leaderboard
- Final Model : KoBART (Encoder-Decoder, 5-Fold Ensemble) <br>

<img width="981" height="391" alt="Image" src="https://github.com/user-attachments/assets/efb017e7-2586-4e94-9b36-5c1df1216d7d" />

- Final Score :
    - Rouge1 : 0.5721
    - Rouge2 : 0.3780
    - RougeL : 0.4902
    - Final_result : 48.0093

Rank : 🥉 3rd


<a id="troubleshooting-engineering"></a>

## 🛠️ Troubleshooting & Engineering
## 1. 단일 24GB VRAM 환경에서의 거대 모델(10B+) OOM 극복 및 학습 최적화
### 문제 정의
24GB 단일 GPU 환경에서 Solar-10.7B, Qwen3-14B 와 같은 거대 파라미터 언어 모델을 파인튜닝 하는 과정에서 `OOM(Out Of Memory)` 문제가 반복적으로 발생하여 파이프라인 진행이 어려웠습니다.

### 원인 분석
10B 이상의 파라미터를 가진 모델은 기본 가중치 외에도 옵티마이저 상태, 그레디언트 메모리가 막대하게 요구되어서 물리적인 VRAM 한계를 훨씬 많이 초과된다는 인사이트를 얻었습니다.

### 해결 방안
메모리 최적화를 위해 `QLoRA(4-bit 양자화)` 기법과 `Unsloth` 라이브러리를 선제적으로 도입했습니다. 추가로 물리적 Batch Size 를 1로 줄이는 대신 `gradient_accumulation_steps=32` 를 설정하여 메모리 낭비 없이 가상으로 큰 배치 사이즈의 안정적인 가중치 업데이트가 가능하도록 조치했습니다.

### 인사이트
이를 통해 VRAM 사용량을 극한으로 압축하고 학습 속도를 2배 이상 단축시켰습니다. 제한된 하드웨어 자원 속에서도 최신 경량화 프레임워크를 적극 도입하고 메모리 연산을 최적화하면, 거대 모델도 충분히 핸들링 할 수 있다는 실무적인 리소스 관리 역량을 확보했습니다. 

---

## 2. 룰 기반 전처리의 함정 타파와 Data-Driven 롤백
### 문제 정의
요약문의 자연스러움을 위해서 `#Person1` 와 같은 토큰을 가상 이름으로 치환하고, 프롬프트 전면에 `[Topic]` 키워드를 강제 주입하는 <b>Topic Strategy</b> 를 시도했으나, LLM 이 가상 이름을 그대로 베껴 쓰는 할루시네이션 병목 현상 및 전체 Rouge Score 하락이 발생했습니다.

### 원인 분석
개발자의 주관적 '직관' 에 의존한 전처리가 원본 데이터의 구조적 특성과 충돌했습니다. 또한 실제 추론 환경(리더보드에 존재하는 Private Data)에는 존재하지 않을 임의의 태그(Topic)가 오히려 모델의 어텐션을 교란하는 노이즈로 작용했다고 생각했습니다.

### 해결 방안
EDA 결과 정답 데이터의 82.4% 가 특수 태그를 그대로 유지하고 있고, 통계적 검증을 통해서 'Topic Strategy' 가 점수에 악영향을 미친다는 명확한 사실을 확인하여 해당 로직을 전면 폐기하기로 했습니다. 또한 디코더 최대 길이를 50으로 줄이고 "핵심 행동만 요약하라"는 통제 지시문만 남겨서 파이프라인을 순정 상태로 롤백 했습니다.

### 인사이트
LLM Prompt 설계나 전처리 파이프라인은 '그럴만한데?' 와 같은 직관이 아닌, 철저하게 데이터의 통계적 패턴(EDA 를 통해 나온 데이터 지표)과 정략적 평가 결과에 근거해 구축되어야만 `GIGO` 를 막을 수 있음을 깊이 체감했습니다.

---

## 3. 데이터 편향성 극복을 위한 앙상블 적용과 리소스 트레이드오프
### 문제 정의
EDA 결과 '음식 주문' 과 같은 특정 소수 토픽에 데이터가 과도하게 편향되어 있는 롱테일 불균형 문제를 확인하였고, 이로 인한 모델의 범용적인 요약 성능 저하 리스크가 존재했습니다.

### 원인 분석
단일 모델 학습만으로는 희귀 상황 데이터에 대한 일반화 성능을 보장하기 어려우며, 특정 다수 데이터 패턴에만 과적합 될 확률이 매우 높다고 생각했습니다.

### 해결 방안
데이터 불균형 방어벽을 세우기 위해 팀 차원에서 5-Fold 교차 검증 및 앙상블 기법을 과감하게 도입해보고자 했습니다. 단, 10B 이상의 LLM 과 결합할 경우 VRAM 및 추론 시간이 기하급수적으로 팽창 할 수 있겠다 생각하여, 최종 SOTA 앙상블은 비용 효율이 높은 최적화된 Encoder-Decoder 모델(KoBART)을 베이스로 채택하여 제출했습니다.

### 인사이트
성능 향상을 위한 복잡한 기법의 도입도 중요하지만, <b>모델의 파라미터 크기 vs 앙상블을 통한 일반화성능 vs 주어진 컴퓨팅 예산</b> 사이의 트레이드오프를 정밀하게 조율하는 것과 모델 사이즈가 크다고해서 모든 성능이 좋은 건 아니구나 와 같은 실제 서비스 환경을 고려하는 엔지니어의 핵심 덕목임을 깨달았습니다.


<a id="teamleadership-management"></a>

## 👥 Team Leadership & Management 
단순 코드 병합 중심의 개발을 넘어, '실험 결과와 인사이트의 병합' 이 핵심인 프로젝트 특성에 맞춰 다음과 같은 엄격한 연구 협업 룰을 세팅하고 리드했습니다.

1. 1일 1회 리더보드 제출 : 완벽주의에 빠져서 로컬 환경에서 실험만 반복하는 것을 방지하고자 했습니다. 매일 정략적 지표를 강제로 확인하게 하여 파이프라인의 방향성을 끊임없이 수정할 수 있게 리드했습니다.
2. 데이터 기반 소통 규칙 : 추상적인 텍스트 공유를 금지했습니다. EDA 결과나 실험 인사이트를 Slack 에 공유할 때는 반드시 시각화된 데이터나 통계 지표를 첨부하도록 규정하여 팀 내 커뮤니케이션의 객관성을 확보하고자 했습니다.
3. 데일리 랩업 : 매일 정규 시간 전, 각자가 개별적으로 진행한 파이프라인 실험 결과와 성능 향상 로직을 투명하게 공유했습니다. 이를 통해 성공적인 실험 요소들이 팀원 전체의 파이프라인에 즉각적으로 이식될 수 있는 선순환 구조를 만들고자 했습니다.
4. W&B 기반 실험 트래킹 : 개인 로컬 환경에서 발생하는 실험 파편화를 막기 위해 Weight & Biases 를 연동하여 프로젝트 관리를 지시했습니다. 모든 실험의 하이퍼파라미터와 평가지표를 실시간으로 중앙 집중화하여, 주관적 판단이 아닌 Metric 기반의 판단 시스템을 정착시키고자 했습니다.

<img width="1845" height="784" alt="Image" src="https://github.com/user-attachments/assets/677bdbf0-017c-4b19-a0be-900484b347ae" />
협업 플랫폼 : Slack, Zoom


<a id="retrospective-futurework"></a>

## 📈 Retrospective & Future Work
### 📌 회고
Computer Vision 과 관련된 딥러닝 프로젝트의 파이프라인에 대한 개념이 고착화 된 상태에서 텍스트를 받아들이는 프로젝트를 진행하면서 많은 점을 느꼈던 요약 생성 대회였습니다.
특히 사진을 전처리 하는 요소보다 '글자' 라는 개념은 우리가 평상시에 사용하는 학문이다 보니 전처리에 대한 전략이나 데이터를 이해하는데 많은 어려움은 없겠다 라는 생각을 가지고 뛰어 들었는데 실제는 이런 생각이 오만함 이였다 라는 점을 깨달았습니다.
실질적으로 사람이 바라보는 시선 과 주관적인 생각 에서만 데이터를 바라보고 생각하면 어느정도 한계점이 일찍 도달하겠다 라는 생각이 들었고, 다시 한번 데이터를 바라보는 시선은 다양한 방면에서 바라봐야 모델에 높은 점수와 좋은 성능을 끌어 올릴 수 있겠구나 라는 소중한 GIGO 인사이트를 몸소 느껴볼 수 있었던 프로젝트 였던 것 같습니다.

이번 대회를 통해서 '어떤 특정 분야에서 강점을 가지는 모델' 의 중요성보다 '좋은 데이터, 분포도가 골고루 퍼진 데이터' 의 중요성을 깨닫게 되었고, 또 한정된 리소스 자원을 최대한 활용해서 우리가 취하고자 하는 모델을 사이즈에 맞춰 서빙하는 리소스 자원 관리에 대한 여러 인사이트도 얻게 되엇 뜻 깊었던 프로젝트 였습니다.

### 📗 향후계획
EDA 를 진행하면서 특정 Topic 에만 데이터가 몰려 있는 현상을 발견해서 이러면 특정 Topic 에만 과적합이 발생해서 문제가 생길 수 있겠다 라고 판단하여 다른 Topic 에도 골고루 데이터를 증강하는 전략을 세우고 진행했었는데 프롬프트 부여에 정교함과 데이터 본질에 맞지 않게 설정하고 증강을 해서 기존 포맷에 맞지 않는 노이즈 데이터를 생성하는 바람에 시간을 많이 할애했던 점이 있었습니다. 추후에 데이터가 잘못된 데이터임을 인지한 후에 프롬프트를 정교화하고 본질에 맞는 데이터를 생성했는데 제공된 GPU 마감일 과 프로젝트 기간 관계상 완벽하게 세팅된 데이터를 많이 증강해보지 못한게 아쉬운 점으로 남는 것 같습니다. 그래서 추후에 이 부분을 발판 삼아 다른 태스크에서 양질의 데이터를 증강해보고 싶고,

현업에서 강조되는 <b>제한된 자원속에서 리소스 관리하는 Solution</b> 에 대한 부분을 알게됐지만 조금 더 정교화 시켜서 다른 방법이 또 존재하는지에 대한 여부와 고도화 시켜 효율적인 리소스 자원관리를 조금 더 진행해보고 싶습니다.
