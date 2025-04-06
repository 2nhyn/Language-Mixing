# Language-Mixing

### 코드 설명
temp1 : 간단히 모델이 어떤 식으로 작동하는지 확인, orpo 기반 log likelihood 코드 구현 등 수행해보았음.

orpo_finetuning : 
- 모델별로 test dataset에 대해 log likelihood를 어떻게 평가하는지 알아봄
- wpr / lpr 구하는 함수 구현 (fasttext 이용)
- orpo fine tuning 함수 구현 (fine tuning 전 후 결과 평가)
-> log likelihood로 평가했을 땐 유의미한 개선점이 있었음 !!!

---
### 할 일
- 실험 방법론 보충해서 업데이트
- 사용한 데이터셋 업로드
- orpo fine tuning용 데이터셋 더 구축 (5000개 이상) -> 현재 가지고 있는 건 700rows 정도 됨. 
