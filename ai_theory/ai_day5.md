# 신경망의 분류

 * 신경망의 분류 모델을 만들 때 2진 분류인지 다범주 분류인지에 따라 출력층 노드의 활성함수를 다르게 구성한다.

 * 이진 분류 문제(스팸 메일 판별, 대출 승인 등)일 경우 출력노드는 1개, 활성함수의 최댓값과 최소값으로 변경
 * 학습의 규칙과 비용함수로는 Cross entrophy를 사용한다.
 * 다범주 분류 (그림에 쓰인 숫자 판독하기) 문제에서는 출력 노드는 범주의 갯수만큼 구성한다. 출력함수의 활성함수로는 소프트 맥스로 구성한다.


 # 딥러닝

 * 딥러닝 : 심층 신경망을 이용한 머신러닝 기법

 ## 심층 신경망의 성능 개선

 ### 그래디언트 소실

 * 역전파 알고리즘(출력층의 오차를 은닉층으로 역전파시켜 신경망을 학습시킴)으로 심층 신경망을 학습시키면 출력층에서 멀어질수록 신경망의 출력 오차가 반영되지 않는 현상.

> 대처방안 : ReLU 함수로 바꾸기

* ReLU 함수 : 0 이하는 전부 0을 출력하고, 0 이상은 그대로 출력

### 과적합

> 대처방안 : 드롭아웃

드롭아웃은 신경망 전체를 다 학습시키지 않고 일부 노드만 무작위로 골라 학습시키는 기법이다.

## 컨볼루션 신경망

* 영상 인식에 특화된 심층 신경망이다.
## 컨브넷

* 특정 추출기를 수작업으로 설계하지 않고 신경망의 학습 과정에 포함시켜 일괄 처리 한다.
* 신경망의 가중치도 학습을 통해 결정해 사람들이 직접 설계하던 특징 추출 작업을 자동화했다.

##  컨볼루션 계층

* 입력이미지에서 고유한 특징을 부각시킨 이미지를 새로 만들어내는 역할을 한다.
* 이러한 이미지를 FEATURE MAP이라고 한다.
* 연결 가중치와 가중합 등이 없고 입력 이미지를 다른 이미지로 변환시키는 필터가 들어있다.
## 풀링 계층

* 이미지의 크기를 줄이는 역할을 한다.
* 입력 이미지에서 특정 영역에 있는 픽셀들을 묶어서 하나의 대표값으로 축소한다.