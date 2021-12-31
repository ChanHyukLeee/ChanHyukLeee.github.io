---
title:  "cost function and parameter learning"
excerpt: "앤드류 응 교수님 코세라 강의에서 발췌 "

categories:
  - Machine Learning
tags:
  - [Machine Learning]

toc: true
toc_sticky: true
 
date: 2021-12-28
last_modified_at: 2020-12-31
---


# cost function and parameter learning

- Notation
    
    m : example 수
    
    x : input variable, feature
    
    y : output variable, target
    
    (x,y) : one train example
    
    h : hypothesis (x를 입력값으로 y 추정)
    
- 모델과 cost function
    
    real-valued output 예측
    
    선형회귀 : h가 일차함수 (a + bx)
    
    → 파라미터 찾기
    
    → minimize of (h(x) - y)^2 : squared error function
    
    ![Untitled](cost%20function%20and%20parameter%20learning%2016ac5cd0023c4e0b9ff400374608b59b/Untitled.png)
    
    J(cost function)를 가장 작게 만드는 a,b 찾기
    
- gradient descent
    
    general function에서도 사용 가능 J(a,b,c,d, ...)
    
    각 파라미터를 보면서 체크
    
    알파 : learning rate (기울기 하강 정도)
    
    simultaneous update
    
    ![Untitled](cost%20function%20and%20parameter%20learning%2016ac5cd0023c4e0b9ff400374608b59b/Untitled%201.png)
    
    알파가 너무 작으면 gradient descent slow
    
    알파가 너무 크면 minimum을 overshoot할 가능성 높아짐
    
    만약 slope 가 0 면 파라미터는 유지
    
    최솟값에 가까워 질수록 derivative가 작아지므로 step이 작아짐
    
    → 알파가 감소할 필요는 없음
    
    convex function : global minimum으로 가게 됨
    
    batch gradient descent :  모든 집합을 gradient descent
    
- 선형대수학 복습
    
    vector : nx1 matrix
    
    mxn * nx1 = mx1 : 동시에 y값 찾을 때 사용
    
    mxn * nxk = mxk : 여러 가설을 이용해 y값 구하기
    
    AxB ≠ BxA
    
    AxBxC = Ax(BxC)  = (AxB)xC
    
    identity matrix는 교환법칙 성립
    
    역행렬을 가지지 않는 matrix : singular,  degenerate