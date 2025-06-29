# 선형 회귀 실습 요약 (Linear Regression)

## 1. 개요
- 목표 : 입력 X에 대한 연속적인 출력 y를 예측하는 선형 회귀 모델 학습
- 사용 데이터 : 임의로 생성한 정렬된 X, y 값 + noise
- 도구 : numpy, matplotlib, scikit-learn

---

## 2. 데이터 생성 및 시각화
- X, y 데이터를 np.sorted(np.random.rand())로 정렬 후 생성
- plt.scatter(X, y)로 데이터 분포 시각화

> 시각화 결과 : 대체적으로 증가하는 패턴, 노이즈로 인해 살짝 오차는 있긴 함

---

## 3. 데이터 분할
- train_test_split 함수로 전체 데이터를 훈련용 데이터 80%, 테스트용 데이터 20%로 나눠줌
- X_train, X_test, y_train, y_test 생성

> 모델이 train 데이터를 보고 입력 X와 출력 y의 관계를 수학적으로 추론 : 입력에서 출력까지의 패턴 찾기
> y = wX + b // 입력 X, 출력 y // 모델이 찾아야 할 파라미터 w, b 가중치와 편향
---

## 4. 모델 정의 및 학습
- model = LinearRegression()으로 모델 생성
- model.fit(X_train, y_train)으로 훈련 데이터로 학습 수행

> .fit은 X_train과 y_train을 보고 w와 b를 찾는 과정 → 즉 학습한다, 훈련한다 (train)

---

## 5. 모델 파라미터 확인
- model.coef_ : 학습된 기울기(가중치) 
- model.intercept_ : 학습된 절편(편향)

---

## 6. 예측 및 시각화
- predict = model.predict(X_test) : 테스트 데이터 예측
- plt.scatter(X_test, y_test) : 실제 데이터 산점도
- plt.plot(X_test, predict, color='red') : 예측 선 시각화

> 시각화를 통해 학습된 데이터가 예측한 것과 비슷한 결과를 나타내고 있다.

---

## 7. 모델 성능 평가
- model.score(X_train, y_train)` → 학습 데이터 R² 점수
- model.score(X_test, y_test)` → 테스트 데이터 R² 점수

> 📈 R² 점수는 1에 가까울수록 모델 성능이 우수함

---

## 8. 느낀 점
- 단순 선형 회귀는 직관적이고 시각화하면서 보기 쉬움
- 실제로 noise를 제거해보니까 R²이 오르는 것을 확인할 수 있다.
