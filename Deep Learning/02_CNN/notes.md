# CNN 실습 요약 (CNN)

## 1. 개요
- 목표 : 훈련용 데이터를 가지고 학습 후 테스트용 데이터로 예측하는 CNN 모델
- 사용 데이터 : 0 ~ 9 까지의 손글씨로 이루어진 제공되는 데이터셋(MNIST)
- 도구 : numpy, matplotlib, torch, torchvision

---

## 2. 데이터 생성 및 시각화
- `train_data = datasets.MNIST()` : MNIST 데이터셋 
- `test_data = datasets.MNIST()` : MNIST 데이터셋

* `train_data[0]`: 60000개중 첫 번째 데이터셋
* 반복문과 랜덤 함수를 통해 시각화 

---

## 3. 미니배치
- 연산 속도 향상, 코드 간결화를 위한 로더 연결

---

## 4. CNN 클래스 선언

이 모델은 **2개의 Convolutional Layer**와 **1개의 Fully-connected Layer**로 구성되어 있다.

- `__init__` 파트는 어떠한 레이어들을 모듈로 쓸지 선언  
     layer1, 2는 **Conv → ReLU → MaxPool** 과정을 지나며 마지막에 **Fully-connected layer**를 거친다.
       
* `forward` __init__에서 정의를 내린 레이어들을 **forward**에서 사용
---

## 5. 모델 훈련 단계
- 로더 연결된 훈련용 데이터를 변수들을 거쳐 훈련한다.

---

## 6. 결과
- 훈련을 거친 결과 헷갈리게 써진 손글씨는 정답이 아닌 경우가 존재한다. 




