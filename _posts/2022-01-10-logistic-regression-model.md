---
title:  "Logistic regression model"
excerpt: "앤드류 응 교수님 코세라 강의에서 발췌 "

categories:
  - Machine Learning
tags:
  - [Machine Learning]

toc: true
toc_sticky: true
 
date: 2022-01-10
last_modified_at: 2022-01-10
---

1. cost function
    
    logistic regression은 비볼록함수를 갖고
    
    비볼록함수(non-convex)는 global minimum 값을 찾기 어렵다 
    
    → 다른 cost function이 필요
    
    $$ J(\theta) = \frac{1}{m} \sum_{i=1}^{m} \left[ -y^{(i)} \log\left(h_\theta\left( x^{(i)} \right) \right) - \left( 1 - y^{(i)}\right) \log \left( 1 - h_\theta\left( x^{(i)} \right) \right) \right]$$
     
    만약 y=1일때 가설값이 0이라면 cost function은 무한대이다. 즉 그만큼 패널티를 줘서 맞추게 하는 것이다. 만약 가설값이 1이라면 옳게 되므로 cost function은 0이다. 
    

2. simplified cost function and gradient descent
    
    $$ \frac{\partial J(\theta)}{\partial \theta_j} = \frac{1}{m} \sum_{i=1}^m \left( h_\theta \left( x^{(i)} \right) - y^{(i)} \right) x_j^{(i)} $$
    
    minimum J(theta) → gradient descent(편미분 통해서)
    

3. optimization
    
    gradient descent외에도 다양한 알고리즘이 존재
    
    conjugate gradient, BFGS, L-BFGS 등
    
    복잡하지만 알파를 매뉴얼하게 픽할 필요없고 속도가 굉장히 빠르다.
    
    → library 활용