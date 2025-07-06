# K-최근접 이웃 실습 요약 (K-Nearest Neighbors)

## 1. 개요
- 목표 : 붓꽃 데이터를 활용한 KNN 분류 적용
- 사용 데이터 : 붓꽃 데이터(load_iris)
- 도구 : numpy, matplotlib, scikit-learn, pandas

---

## 2. 데이터 생성
-`iris = load_iris()`: 데이터 생성

---

## 3. 데이터프레임 생성
- `iris_df = pd.DataFrame(data=iris.data, columns=iris.feature_names)`: 구조화된 데이터를 효율적으로 다루기 위한 데이터프레임 생성

## 4. 모델 정의 및 학습
- model = LinearRegression()으로 모델 생성
- model.fit(X_train, y_train)으로 훈련 데이터로 학습 수행

> .fit은 X_train과 y_train을 보고 w와 b를 찾는 과정 → 즉 학습한다, 훈련한다 (train)

---

## 5. 학습용 · 테스트용 데이터 나누기
- `train_test_split`을 사용해 데이터 나누기
---

## 6. KNN  분류 모델 적용

`knn.fit()`: 모델 적용 및 훈련

---

## 7. 예측 및 정확도 평가
-`knn.predict(X_test)`: 예측
- `accuracy_score(y_test, y_pred)`: y 테스트와 X_test 예측을 비교하여 정확도 평가를 함

---

## 8. 시각화
- `figure, contourf, scatter`등을 이용하여 KNN분류한 것들을 시각화하였다.




