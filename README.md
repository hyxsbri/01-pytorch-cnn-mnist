# Pytorch를 활용한 MNIST 분류기 모델링

![MNIST](https://github.com/hyxsbri/pytorch-cnn-mnist-classifier/blob/main/img/network.png?raw=true)

## 소개

MNIST 데이터셋을 활용한 PyTorch CNN(Convolutional Neural Network) 분류기의 구현 작업 과정 및 결과물입니다.

## 저장소 내용

### 1. `img` 폴더

* `img` 폴더에 CNN 관련 논문에 제시된 네트워크 이미지입니다. 위 이미지를 참조하며 모델링 작업을 수행했습니다.
* 5x5 Conv. | 2x2 Max Pooling | ReLU | 5x5 Conv. | 0.5 Dropout | 2x2 Max Pooling | ReLU


### 2. `model_checkpoint` 폴더

`model_checkpoint` 폴더에는 저장된 모델 체크포인트들이 포함되어 있습니다. 이 체크포인트들은 훈련 재개 또는 훈련된 모델에 대한 추론 등에 유용하게 사용될 수 있습니다.

### 3. `tensorboard_log` 폴더

`tensorboard_log` 폴더는 훈련 중에 TensorBoard가 생성한 로그들이 저장되어 있습니다. 이 로그들은 메트릭, 시각화 자료, 그리고 계산 그래프 등을 통해 훈련 과정에 대한 중요한 정보를 제공합니다.

### 4. `eval.py`

`eval.py` 스크립트는 테스트 데이터셋에서 훈련된 모델을 평가하는데 사용됩니다. 저장된 모델 파라미터들을 로드하고, 정확도, 정밀도, 재현율, F1 스코어 등 다양한 평가 메트릭을 계산합니다. 또한, 이 스크립트는 모델의 성능에 대한 포괄적인 분석을 제공합니다.

### 5. `train.py`

`train.py` 스크립트는 MNIST 데이터셋에서 CNN 모델을 훈련하기 위한 코드입니다. 데이터 로딩, 모델 초기화, 훈련 루프, 그리고 훈련된 모델 파라미터들의 저장 등을 처리합니다. 또한, 이 스크립트는 학습률, 배치 크기, 훈련 에폭 수 등 다양한 하이퍼 파라미터들을 해당 사용자가 직접 정의할 수 있도록 구성돼있습니다.

## 결과

* 약 60,000개의 훈련 데이터를 배치 단위 분할 후, 열 번의 에폭으로 학습을 진행했습니다.
* 64개의 배치 사이즈를 가진 157 묶음 테스트 데이터에 대해 최종 98.61%의 분류 정확도를 기록했습니다.
