---
title:  "머신러닝의 정의"
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

# 머신러닝의 정의

1. arthur samuel : 일을 반복하면 특정 수준을 뛰어넘는다.

2. tom mitchell : A computer program is said to learn from experience E with respect to some class of tasks T and performance measure P, if its performance at tasks in T, as measured by P, improves with experience E.
    
    E : 같은 게임을 수만 번 반복하는 과정
    
    T : 게임을 수행하는 행위
    
    P  : 다음 판 게임에서 이길 확률
    

3. supervised learning
    
    데이터에 정답 존재 → 알고리즘 → 정답을 예측
    
    regression(연속값), classification(불연속적 값)
    
    특성이 무한히 김 → 다양한 알고리즘 개발
    
4. unsupervised learning
    
    데이터에 정답x → 구조 찾기 (클러스터 찾기)
    
    - 구글 뉴스 : 연관성 있는 뉴스
    - dna 통해 사람들을 특정 분류로 나눔
    - 소셜네트워크 분석(적절한 친구 찾기)
    - 세분화된 시장 찾기
    
    칵테일 파티 문제 : 동시에 말할때 거리가 다른 마이크에 녹음
    
    → 음성 소스 분리