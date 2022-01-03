---
title:  "Multivariate Linear Regression"
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

1. notation
    
    n = number of features
    
    $x^i$ = i번째 example 의 feature vector : [1,2,3,4]
    
    $(x_j)^i$ = $x^i$의 j번째
    
    $h(x) = a + bx + cx^2 + dx^3 + ex^4$
    
     = Transpose(theta) * x (내적) (x0 = 1인 경우 일 때)
    
    ![Untitled](multivariate%20linear%20regression%20bc2139cebca8437dbb251dbdda5b3823/Untitled.png)
    

2. gradient descent for multiple variables
    
    ![Untitled](multivariate%20linear%20regression%20bc2139cebca8437dbb251dbdda5b3823/Untitled%201.png)
    

3. feature scaling
    
    각 feature의 스케일이 다르다면 gradient descent가 굉장히 오래 걸림 → 그래서 feature를 비슷한 스케일로 맞추어야 한다.
    
    보통 -1에서 1사이로 맞춘다. (융통성있게 접근)
    
    - mean normalization
        
        $(x- average value) / range(max-min or standard derivation)$
        
        ![Untitled](multivariate%20linear%20regression%20bc2139cebca8437dbb251dbdda5b3823/Untitled%202.png)
        

4. learning rate
    
    각 iteration마다 j(t) 감소하지만 점점 수렴
    
    - automatic convergence test : 한번 반복할때 e-3보다 작게 감소하면 수렴했다 선언
    
    만약 j(t)가 증가하거나 수렴하지 않으면 gradient descent 가 제대로 되지 않았기 때문에 learning rate를 감소
    
    너무 작다면 천천히 수렴
    

5. polynomial regression
    
    2차식 대신 3차식.. (그래프가 커졌다가 하강하기 때문)
    
    x1 = size, x2 = size 제곱 x3 = size 세제곱
    
    제곱근함수(루트 사이즈)
    

6. computing parameters analytically
    - normal equation
        
        theta를 분석적으로 구하는 방법
        
        만약 theta가 실수라면 미분해서 최솟값 구하면 되지만 보통 theta는 n+1 dim의 벡터이다.
        
        → 편미분하면 모든 1...n까지 theta 값 구할 수 있음
        
        ![Untitled](multivariate%20linear%20regression%20bc2139cebca8437dbb251dbdda5b3823/Untitled%203.png)
        
        feature scaling, 알파, iteration필요 없음
        
        n이 커질 때 시간너무 오래 걸림(역행렬 계산 o(n^3))
        
        $n ≤ 1000$ 인 경우만 사용
        
        ↔ gradient descent는 알파를 선택하고, 많은 iteration 필요
        
        그리고 n이 클때 잘 돌아감(1만 이상)
        
    
    - 만약 역행렬이 존재하지 않는다면?
        
        거의 없다. (pseudo - inverse 활용)
        
        만약 역행렬이 없다면
        
        1. feature가 linearly dependent한 경우
        2. 너무 많은 feature (m < n) → feature 없애거나 regularization 사용