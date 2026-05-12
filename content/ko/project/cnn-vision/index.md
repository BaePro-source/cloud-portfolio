---
title: CNN 이미지 분류 모델
summary: PyTorch CNN으로 구현한 이미지 분류 및 객체 탐지 프로젝트
tags:
  - cnn
  - deeplearning
  - ai
date: 2025-05-01
external_link: https://github.com/BaePro-source
image:
  caption: 'CNN Model Architecture'
  focal_point: Smart
  preview_only: false
---

## CNN 기반 이미지 분류 프로젝트

PyTorch를 사용하여 Convolutional Neural Network(CNN)를 직접 설계하고, 이미지 분류 및 특징 추출 모델을 구현한 프로젝트입니다.

### 주요 구현 내용
- **CNN 아키텍처 설계**: Conv2d, BatchNorm, MaxPooling, Dropout 레이어 구성
- **Transfer Learning**: ResNet, VGG 등 사전 학습 모델 파인튜닝
- **데이터 증강**: RandomFlip, RandomCrop, ColorJitter를 이용한 오버피팅 방지
- **모델 평가**: Confusion Matrix, Precision/Recall/F1-Score 분석

### 기술 스택
- Python, PyTorch, torchvision
- NumPy, Matplotlib (시각화)
- CUDA (GPU 가속 학습)
