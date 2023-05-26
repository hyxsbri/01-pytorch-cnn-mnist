# Pytorch를 활용한 MNIST 분류기 모델링
## 2022.09.13 ~ 2022.09.30

![MNIST](https://upload.wikimedia.org/wikipedia/commons/2/27/MnistExamples.png)

## 소개

MNIST 데이터셋을 활용한 PyTorch CNN(Convolutional Neural Network) 분류기의 구현을 담고 있습니다.

## 저장소 내용

### 1. `img` 폴더

`img` 폴더는 프로젝트와 관련된 이미지와 시각적 자료들이 저장되어 있습니다. 이러한 이미지들은 문서 작성, 시각화 또는 다른 관련 용도로 사용될 수 있습니다.

### 2. `model_checkpoint` 폴더

`model_checkpoint` 폴더에는 저장된 모델 체크포인트들이 포함되어 있습니다. 이 체크포인트들은 훈련 재개 또는 훈련된 모델에 대한 추론 등에 유용하게 사용될 수 있습니다. 체크포인트 파일들은 일반적으로 `.pth` 확장자를 갖습니다.

### 3. `tensorboard_log` 폴더

`tensorboard_log` 폴더는 훈련 중에 TensorBoard가 생성한 로그들이 저장되어 있습니다. 이 로그들은 메트릭, 시각화 자료, 그리고 계산 그래프 등을 통해 훈련 과정에 대한 중요한 정보를 제공합니다.

### 4. `eval.py`

`eval.py` 스크립트는 테스트 데이터셋에서 훈련된 모델을 평가하는 데 사용됩니다. 저장된 모델 파라미터들을 로드하고, 정확도, 정밀도, 재현율, F1 스코어 등 다양한 평가 메트릭을 계산합니다. 이 스크립트는 모델의 성능에 대한 포괄적인 분석을 제공합니다.

### 5. `train.py`

`train.py` 스크립트는 MNIST 데이터셋에서 CNN 모델을 훈련하기 위한 코드를 포함하고 있습니다. 데이터 로딩, 모델 초기화, 훈련 루프, 그리고 훈련된 모델 파라미터들의 저장 등을 처리합니다. 이 스크립트는 학습률, 배치 크기, 훈련 에폭 수 등 다양한 하이퍼 파라미터들을 사용자 정의할 수 있도록 구성되어 있습니다.

## 사용법 및 실행

저장소를 활용하고 코드를 실행하려면 다음 단계를 따르세요:

1. 저장소를 로컬 머신에 클론합니다:

```python
git clone https://github.com/hyxsbri/pytorch-cnn-mnist-classifier.git
```

2. 저장소 디렉토리로 이동합니다:

```python
cd pytorch-cnn-mnist-classifier
```

3. 필요한 종속성을 설치합니다:

```python
pip install -r requirements.txt
```

4. **평가**: `eval.py` 스크립트를 실행하여 훈련된 모델을 평가합니다:

```python
python eval.py
```

5. **훈련**: `train.py` 스크립트를 실행하여 CNN 모델을 훈련합니다:

```python
python train.py
```

이 스크립트는 MNIST 데이터셋을 기반으로 모델을 훈련하고 훈련된 모델 파라미터, 훈련 로그, 체크포인트 등과 같은 관련된 출력물들을 저장합니다.

## 결론

이 저장소는 MNIST 데이터셋에 대한 PyTorch CNN 분류기의 구현을 보여줍니다. `img`, `model_checkpoint`, `tensorboard_log` 폴더, 그리고 `eval.py`, `train.py` 스크립트를 포함하여 딥러닝 개념, 모델 훈련, 평가 기법 등에 대한 저의 기술과 이해력을 보여주고자 해당 작업을 수행했습니다.
