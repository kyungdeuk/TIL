# Anaconda

> **아나콘다**(Anaconda)는 패키지 관리와 디플로이를 단순케 할 목적으로 과학 계산(데이터 과학, 기계 학습 애플리케이션, 대규모 데이터 처리, 예측 분석 등)을 위해 파이썬과 R 프로그래밍 언어의 자유-오픈 소스 배포판이다.



## 1. 가상환경 생성 및 실행

### 1.1 가상환경 생성

```shell
conda create -n <가상환경 이름>
```

```shell
conda create -n <가상환경 이름> python=3.6
```



### 1.2 가상환경 리스트

```shell
conda info --env
```



### 1.3 가상환경 제거

```shell
conda remove -n <가상환경 이름> -all
```



### 1.4 가상환경 활성화 & 비활성화

```shell
conda activate <가상환경 이름> # 활성화
conda deactivate # 비활성화
```



### 1.5 가상환경에 설치된 패키지 리스트

```shell
conda list # 해당 가상환경을 활성화 시켰을 때
conda list -n <가상환경 이름> # base에서 보고 싶을 때
```



## 2. PyTorch

### 2.1 PyTorch 설치

```shell
conda install pytorch torchvision cudatoolkit=10.2 -c pytorch
```



### 2.2 PyTorch 설치 확인

```python
from __future__ import print_function
import torch
x = torch.rand(5, 3)
print(x)
```

```python
import torch
torch.cuda.is_available()
```



### 3. Tensorflow2

### 3.1 Tensorflow2 설치

```shell
conda create -n tf2 python=3.6
conda activate tf2
conda install tensorflow-gpu==2.0.0
```



### 3.2 Tensoflow2 설치 확인

```python
import tensorflow as tf
print(tf.__version__)
tf.test.is_gpu_available()
```

