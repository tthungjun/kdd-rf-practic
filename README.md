# Network Intrusion Detection using RandomForest (KDD Dataset)

## 📖 1. 프로젝트 개요

본 프로젝트는 네트워크 트래픽 데이터를 기반으로 정상/공격 여부를 분류하는  
침입 탐지 시스템(Intrusion Detection System, IDS) 모델을 구현하는 것을 목표로 한다.

공개 데이터셋인 KDD 데이터를 활용하여 머신러닝 기반 이진 분류 모델을 구축하였다.

---

## 📊 2. 사용 데이터셋

- KDD Intrusion Detection Dataset
- 정상 트래픽(0) / 공격 트래픽(1) 이진 분류

KDD 데이터는 고전적인 IDS 벤치마크 데이터셋으로,  
네트워크 보안 및 침입 탐지 연구에서 널리 사용되는 공개 데이터이다.

---

## 🛠 3. 기술 스택

- Python
- scikit-learn
- pandas
- numpy
- matplotlib

---

## ⚙ 4. 모델링 과정

### 1️⃣ 데이터 전처리
- 불필요 컬럼 제거
- 범주형 데이터 인코딩
- 학습/테스트 데이터 분리

### 2️⃣ Pipeline 구성
scikit-learn의 Pipeline을 사용하여  
전처리와 모델 학습을 하나의 흐름으로 구성하였다.

→ 재현성 및 코드 관리 용이성 확보

### 3️⃣ 모델
- RandomForestClassifier 사용
- Train/Test 분리를 통한 일반화 성능 평가

---

## 📈 5. 모델 성능

### 🔹 Classification Report

- Accuracy: 99.9% 이상
- Precision: 1.00
- Recall: 1.00
- F1-score: 1.00

### 🔹 Confusion Matrix

[[13468, 1],
[ 4, 11722]]


총 25,195개 중 5개만 오분류 발생

- False Positive: 1
- False Negative: 4

→ 매우 높은 탐지 성능 확인

---

## 💡 6. 프로젝트 의의

- 머신러닝 기반 침입 탐지 모델 구현 경험
- Pipeline을 활용한 구조화된 모델 설계
- 보안 데이터셋을 활용한 실전 분류 문제 경험

---

## ⚠ 7. 한계점 및 개선 방향

- KDD 데이터는 오래된 데이터셋으로 실제 최신 네트워크 트래픽과 차이가 존재
- 실환경 데이터에 대한 추가 검증 필요
- XGBoost, LightGBM 등 다른 모델과 성능 비교 가능
- 실시간 탐지 시스템으로 확장 가능

---

## 🚀 8. 향후 확장 아이디어

- 클라우드 환경(AWS 등)에서 IDS 모델 배포
- Docker 기반 컨테이너화
- 실시간 로그 스트림 기반 탐지 시스템 구축
