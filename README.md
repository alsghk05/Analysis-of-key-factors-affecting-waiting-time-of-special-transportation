# 장애인 특별 교통 수단의 대기시간에 영향을 미치는 주요 요인 분석과 최적화 전략

- 2024.08.10 ~ 2024.10.31
- 장애인 특별 교통 수단인 “두리발” 운행 데이터를 바탕으로 대기시간이 오래 걸리는 요인을 분석하고 배차 최적화 방안을 제시함
- 머신러닝을 통해 두리발의 대기시간을 예측하는 알고리즘을 개발함

> **핵심 전략**
> 
> 1. **데이터 암호화 문제 해결**
>     - **문제 원인**: 위경도(위치) 데이터가 암호화되어 있어 분석 및 모델링이 어려웠음
>     1. 암호화된 데이터가 단순히 순차적으로 변환된 값임을 확인하고, 정렬을 통해 패턴 분석
>     2. 가장 먼 거리와 가장 짧은 거리가 동일하게 유지되는 것을 통해, 실제 값으로 복원하지 않아도 거리 계산 및 방향성 분석에는 문제가 없음을 판단
>     3.  원래 데이터로 변환하는 대신, 암호화된 데이터 그대로 상대적인 거리와 방향을 활용하여 분석을 진행
> 2. **학습 속도 최적화**
>     - **문제 원인**: 데이터가 많아서 학습 속도가 느림
>     1. 데이터 샘플링 기법을 적용하여 학습에 사용하는 데이터의 양을 줄이기 위해 feature selection을 진행

### 1. 개발 배경

- 부산시 장애인 특별 교통 수단인 ‘두리발’ 콜택시는 교통 약자, 특히 장애인의 이동권 보장을 위한 교통수단임
- 그러나, 두리발은 긴 대기시간 문제로 탑승이 원활하지 않아 많은 이용자의 불편을 야기하고 있음
- 이를 해소하고자 두리발 서비스의 대기시간 문제를 다차원적으로 분석하고, 데이터에 기반한 차량 배치 및 운영의 최적화 방안을 제안

### 2. 기대 효과

- 분석을 통한 최적화 방안으로 효율적인 차량 분배에 도움이 될 수 있고, 배차를 최적화 함으로써 긴 대기시간을 줄일 수 있음
- 머신러닝을 통해 두리발의 대기시간을 예측하여 해당 정보를 제공함으로써 사용자들이 두리발을 이용하기 전 대기시간에 대한 정보를 알 수 있고, 약속시간을 변경하거나 조금 더 일찍 나서는 등의 조치를 취할 수 있음

### 3. 아키텍쳐

- 데이터 수집 및 전처리 → 각 요인별 EDA를 통한 대기시간 분석 및 corrleation 분석 → ANOVA 검증→ 최적화 전략 제안
- 데이터 수집 및 전처리 → 모델링(XGBC, KNNC, GBC, RFC, DTC, LR) → 모델 학습 및 평가(Accuracy, precision, recall, f1 score) → 하이퍼 파라미터 튜닝(Optuna)을 통한 최적화

### 4. 사용 기술

- Python, Data Preprocessing, EDA, Data visualization
- Machine Learning (XGBC, KNNC, GBC, RFC, DTC, Logistic Regression)

### 5. 라이브러리

- Numpy, Scipy, Pandas, Sklearn, Matplotlib, Seaborn 등

### 6. 개발 환경

- 언어 : Python 3.10.9
- OS : Window 11
- IDE : Jupyter Notebook, VS Code

<aside>


### **🚀성과**

- **장애인 특별 교통 수단의 대기시간에 영향을 미치는 주요 요인 분석과 최적화 전략** ([학술지 게재](https://www.dbpia.co.kr/Journal/articleDetail?nodeId=NODE12025257))
- **대학생 논문 경진대회 금상**
</aside>
