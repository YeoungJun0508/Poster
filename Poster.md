주요 네트워크 구조 -  ResNet, EfficientNet 




#### 손실함수
CircleLoss, SupConLoss, LabelSmoothingCrossEntropy, SoftTargetCrossEntropy 등의 손실 함수들이 정의

#### 전처리
train_transform, val_transform 등의 데이터 전처리 방법이 정의


#### 이미지 입력

데이터는 train_loader, val_loader 등을 통해 미니배치 형태로 입력
#### 전처리

train_transform, val_transform 함수를 사용하여 이미지 데이터를 텐서로 변환하고, 필요에 따라 데이터 증강(augmentation)을 수행
#### 모델 통과

데이터는 ResNet 모델을 통과하여 특징(feature)으로 변환, ResNet은 여러 층의 합성곱(convolutional) 및 풀링(pooling) 층을 통해 이미지의 공간적 특징을 추출
#### 특징 추출

최종적으로 추출된 특징은 CircleLoss, SupConLoss 등의 손실 함수를 계산하는 데 사용, 이 손실 함수들은 모델의 출력과 정답 레이블 간의 차이를 계산하여 학습 과정에서 최적됩니다.
