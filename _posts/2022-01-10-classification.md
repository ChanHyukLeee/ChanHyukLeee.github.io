---
title:  "Definition of classification"
excerpt: "앤드류 응 교수님 코세라 강의에서 발췌 "

categories:
  - Machine Learning
tags:
  - [Machine Learning]

toc: true
toc_sticky: true
 
date: 2022-01-03
last_modified_at: 2022-01-03
---

선형 회귀(linear regression)시

h≥ 0.5 → y= 1

h≤ 0.5 → y = 0

그때 이상치가 존재한다면 올바른 가설이 세워지지 않음

혹은 y=0,1일때 → h는 1보다 클 수도 혹은 0보다 작을 수 있음

만약 logistic regression을 사용한다면 0-1사이에서 h(결과값)를 고정시킬수 있다.

$$ h_\theta(x) = g(\theta^T x)$$

g(x) = sigmoid function = logistic function

$$ g(z) = \frac{1}{1+e^{-z}}$$

$h =P(\y=1| \x; \theta)$ : y=1일때 theta에 의해 파라미터화된 x에 주어진 확률

당연히 y=1 , y=0인 확률을 더하면 1


- decision boundary

y = 1→  g ≥ 0.5 → z≥0 → theta * X≥0

이 공식을 바탕으로  theta(parameter)를 알 때 decision line이 결정 

물론 non-linear한 decision boundary도 있음


- multiclass classification

class가 n 개 → n개 binary classification으로 쪼개서 생각

각 class만 positive라고 가정하고 나머진 negative로 생각해서 classification