### 데이터셋에 대한 간략한 설명
---

자체 생성한 데이터 : chatgpt, cohere 활용

**- laguage_confusion_eval_200.json**
  - 사용된 곳: temp1.ipynb
  - 데이터 출처: LLM 모델로 자체 생성
  - 데이터 난이도: 매우쉬움 (간단한 수도, 음식 질문 등)
  - 데이터 크기: 데이터 쌍 210개
  - 구성: 'prompt', 'chosen', 'rejected'
  - 태스크: single language QA 로만 이루어짐.
  
**- laguage_confusion_eval_set_complex.json**
  - 사용된 곳: temp1.ipynb
  - 데이터 출처: LLM 모델로 자체 생성
  - 데이터 난이도: 40-100 토큰 사이의 좀 더 복잡한 프롬프트, 전문 지식이 필요한 주제 (역사, 정치, 경제 등)
  - 데이터 크기: 데이터 쌍 60개
  - 구성: 'prompt', 'chosen', 'rejected'
  - 태스크: single language QA 로만 이루어짐. (단순한 의문형으로 끝나는 질문 뿐 아니라
  - '~~에 관하여 논의하시오.' 이런 것도 QA로 분류.)
 

**- laguage_confusion_mkqa_eval.json**
  - 사용된 곳: temp1.ipynb
  - 데이터 출처: [mkqa git](https://github.com/apple/ml-mkqa/)
  - 데이터 난이도: 매우쉬움 (간단한 상식 질문 등)
  - 데이터 크기: 데이터 쌍 7만개
  - 사용된 언어: 정확히는 모르겠는데.. 그냥 훑어만 봐도 15개 이상은 됨.
  - 구성: 'prompt', 'chosen', 'rejected'
  - 태스크: single language QA 로만 이루어짐.
  
  
**- orpo_train_data.json (5000개 정도 선까지 추가 필요)**
  - 모델 fine tuning 용 데이터셋으로 생각하고 만들고 있는 데이터셋임.
  - 사용된 곳: orpo_finetuning.ipynb
  - 데이터 출처: LLM 모델로 자체 생성
  - 데이터 난이도: 하, 중하, 중, 중상으로 구성 (5~100토큰)
  - 데이터 크기: 데이터 쌍 700개
  - 사용된 언어: 14개 언어 (ar, de, en, es, fr, hi, id, it, ja, ko, pt, ru, tr, vi, zh )
  - 구성: 'input', 'chosen', 'rejected', 'preferred', 'input_lang', 'expected_lang', 'task'
  - 태스크: single language QA, translation, summary (3가지의 주요 태스크)

  
**- orpo_test_data (500-1000개 사이로 생각하고 있음. 추가 필요)**
  - 모델 성능 테스트용 데이터셋으로 생각하고 만들고 있음. 
  - 사용된 곳: orpo_finetuning.ipynb
  - 데이터 출처: LLM 모델로 자체 생성
  - 데이터 난이도: 하, 중하, 중, 중상으로 구성 (5~100토큰)
  - 데이터 크기: 데이터 쌍 163개
  - 사용된 언어: 현재까지 7개 언어 en, es, ko, de, zh, fr, ja  (finetuning 모델에 사용했던 것과 유사하게 추가할 계획)
  - 구성: 'input', 'chosen', 'rejected', 'preferred', 'input_lang', 'expected_lang', 'task'
  - 태스크: single language QA, translation, summary (3가지의 주요 태스크)
