## 동건

### 문제1
역전파 알고리즘을 사용하는 이유는?

### 풀이
- 동건: 
- 정우: 
- 현아:
- 아영:x1이 y(햇)에 미치는 영향을 알아야 W를 조절할 수 있는데 forward로는 계산량이 너무 많고 미분이 복잡해지기 때문에
- 승렬:
- 지원:

### 문제2
f(x) = x^2, g(x) = x+b 일때, x의 변화량에 대한 f(g(x))의 변화량은?

### 풀이
- 동건:
- 정우: 
- 현아:
- 아영:2x+2b
- 승렬:
- 지원:
---
## 정우

### 문제1
Layer가 3개이며, layer1은 2개를 입력받고, layer 2는 3개 입력, 1ayer 3은 4개를 입력받고 5개를 출력하는 NN을 코딩해보시오. (W1 = ~에서 시작해서,hypothesis = ~ 라인까지만 하시면 됩니다)

### 풀이
- 동건: 
- 정우: 
- 현아: 
- 아영:
W1 = tf.Variable(tf.random_normal([2, 3]), name='weight1')
b1 = tf.Variable(tf.random_normal([3], name='bias1')
layer1 = tf.sigmoid(tf.matmul(X, W1) + b1)

W2 = tf.Variable(tf.random_normal([3, 4]), name='weight2')
b2 = tf.Variable(tf.random_normal([4], name='bias2')
layer2 = tf.sigmoid(tf.matmul(layer1, W2) + b2)

W3 = tf.Variable(tf.random_normal([4, 5]), name='weight3')
b3 = tf.Variable(tf.random_normal([5], name='bias3')
hypothesis = tf.sigmoid(tf.matmul(layer2, W3) + b3)
- 승렬: 
- 지원:

### 문제2
F(X) = 3(2X + Y)^2을 X에대해 편미분해 보시오
### 풀이
- 동건:
- 정우: 
- 현아:
- 아영:24x+12y
- 승렬:
- 지원:
---

## 승렬

### 문제1. 
Find another W and b for the XOR. (lec9-1 11:43 그림 참조)

### 풀이
- 동건: 
- 정우: 
- 현아: 
- 아영:(w1=[4, 4], b1=-6) (w2=[-8, -8], b2=4), (w3=[-12, -12], b3=7)
- 승렬: 
- 지원:

### 문제2
Tensorboard에서 learning rate를 다르게 한 두개 이상의 그래프를 한번에 visualize 하기 위해서는 어떻게 해야 하는가?
### 풀이
- 동건:
- 정우: 
- 현아:
- 아영:상위 폴더(logs)를 동일하게 설정한 후 하위 폴더를 따로 둔다 / 텐서보드를 실행할 때는 상위폴더로 디렉토리 옵션 설정
- 승렬:
- 지원:
---

## 현아

### 문제1
Neural Network가 deep하다 & wide하다는 것의 의미를 각각 서술하시오.

### 풀이
- 동건: 
- 정우: 
- 현아: 
- 아영: wide하다-출력 값을 증가시켜 다음 layer의 입력값이 많아지도록 한다
deep하다-layer이 많다
- 승렬: 
- 지원:

### 문제2
TensorBoard를 사용하는 5가지 단계에 대해 설명하시오.

### 풀이
- 동건:
- 정우: 
- 현아:
- 아영:
1. tensorflow 그래프에서 어떤 값을 로깅해올지 정한다
2. 일일이 돌려주지 않고 모든 summary를 merge
3. 세션을 어디에 저장할 것인지 + 그래프
4. summary를 실행시키고 기록
5. tensorborad 실행
- 승렬:
- 지원:
---

## 아영

### 문제1
g=wx, f=g+b이고 δg/δw=3, δf/δg=1일 때 w가 f에 미치는 영향을 값으로 표현하면?

### 풀이
- 동건: 
- 정우: 
- 현아:
- 아영:3
- 승렬: 
- 지원:

### 문제2
learning rate가 0.1일때와 learning rate가 0.01일때의 그래프를 비교해서 보려고 한다. tensorboard를 사용해 어떻게 그래프를 구현할 수 있을까? (간단히 설명)

### 풀이
- 동건:
- 정우: 
- 현아:
- 아영:상위 폴더(logs)를 동일하게 설정한 후 하위 폴더를 따로 둔다 / 텐서보드를 실행할 때는 상위폴더로
- 승렬:
- 지원:
---

## 지원

### 문제1
하나의 Neural Network를 구성하는 K(X)와 H(X)에 관한 코드를 한 줄씩 작성하시오.

### 풀이
- 동건: 
- 정우: 
- 현아:
- 아영:K(x) = sigmoid(XW1+b1)
H(X) = sigmoid(K(x)W2+b2)
- 승렬: 
- 지원:

### 문제2
back propagation을 간략히 서술하시오.

### 풀이
- 동건:
- 정우: 
- 현아:
- 아영:뒤에서부터 앞으로 미분값과 실제값을 계산
- 승렬:
- 지원:
---
=======
## 동건

### 문제1
역전파 알고리즘을 사용하는 이유는?

### 풀이
- 동건: 
- 정우: 각각의 입력값이 y에 미치는 영향(미분값)을 알아야 각각의 w를 조절할 수 있는데 기존의 방법으로는 게산이 너무 복잡해서 불가능하다고 여겨짐, 이를해결하기 위해서 역전파 알고리즘을 
- 현아:
- 아영:
- 승렬:
- 지원:

### 문제2
f(x) = x^2, g(x) = x+b 일때, x의 변화량에 대한 f(g(x))의 변화량은?

### 풀이
- 동건:
- 정우:2(x+b) 
- 현아:
- 아영:
- 승렬:
- 지원:
---
## 정우

### 문제1
Layer가 3개이며, layer1은 2개를 입력받고, layer 2는 3개 입력, 1ayer 3은 4개를 입력받고 5개를 출력하는 NN을 코딩해보시오. (W1 = ~에서 시작해서,hypothesis = ~ 라인까지만 하시면 됩니다)

### 풀이
- 동건: 
- 정우: W1 = tf.Variable(tf.random_normal([2,3]), name = 'weight1')
b1 = tf.Variable(tf.random_normal([3]), name = 'bias1')
layer1 = tf.sigmoid(tf.matmul(X, W1) + b1)

W2 = tf.Variable(tf.random_normal([3,4]), name = 'weight1')
b2 = tf.Variable(tf.random_normal([4]), name = 'bias1')
layer2 = tf.sigmoid(tf.matmul(layer1, W2) + b2)

W3 = tf.Variable(tf.random_normal([4,5]), name = 'weight2')
b3 = tf.Variable(tf.random_normal([5]), name = 'bias2')
hypothesis = tf.sigmoid(tf.matmul(layer2, W3) + b3)
- 현아: 
- 아영:
- 승렬: 
- 지원:

### 문제2
F(X) = 3(2X + Y)^2을 X에대해 편미분해 보시오
### 풀이
- 동건:
- 정우: 12(X+Y)
- 현아:
- 아영:
- 승렬:
- 지원:
---

## 승렬

### 문제1. 
Find another W and b for the XOR. (lec9-1 11:43 그림 참조)

### 풀이
- 동건: 
- 정우: w1 = [3,3] b1 = -5, w2 = [-8,-8] b2 = 6 w3 = [-5,-5], b3 = 3 
- 현아: 
- 아영:
- 승렬: 
- 지원:

### 문제2
Tensorboard에서 learning rate를 다르게 한 두개 이상의 그래프를 한번에 visualize 하기 위해서는 어떻게 해야 하는가?
### 풀이
- 동건:
- 정우: multiple run. write하는 부분에서 하나의 디렉토리안에 여러개의 디렉토리를 저장. 그리고 부모 디렉토리를 run한다 
- 현아:
- 아영:
- 승렬:
- 지원:
---

## 현아

### 문제1
Neural Network가 deep하다 & wide하다는 것의 의미를 각각 서술하시오.

### 풀이
- 동건: 
- 정우: WIDE: 출력값과 입력값, DEEP: 레이어의 개수
- 현아: 
- 아영:
- 승렬: 
- 지원:

### 문제2
TensorBoard를 사용하는 5가지 단계에 대해 설명하시오.

### 풀이
- 동건:
- 정우: 1. 어떤 값을 logging 할것인지 정하고 값을  2.서머리를 머지 3. 파일의 위치를 정하고 그래프를 넣어줌 4. 서머리를 실행하고 파일에 기록 5. 텐서보드 실행 
- 현아:
- 아영:
- 승렬:
- 지원:
---

## 아영

### 문제1
g=wx, f=g+b이고 δg/δw=3, δf/δg=1일 때 w가 f에 미치는 영향을 값으로 표현하면?

### 풀이
- 동건: 
- 정우:3 
- 현아:
- 아영:
- 승렬: 
- 지원:

### 문제2
learning rate가 0.1일때와 learning rate가 0.01일때의 그래프를 비교해서 보려고 한다. tensorboard를 사용해 어떻게 그래프를 구현할 수 있을까? (간단히 설명)

### 풀이
- 동건:
- 정우: multiple run. write하는 부분에서 하나의 디렉토리안에 여러개의 디렉토리를 저장. 그리고 부모 디렉토리를 run한다 
- 현아:
- 아영:
- 승렬:
- 지원:
---

## 지원

### 문제1
하나의 Neural Network를 구성하는 K(X)와 H(X)에 관한 코드를 한 줄씩 작성하시오.

### 풀이
- 동건: 
- 정우: K = tf.sigmoid(tf.matmul(X, W1) + b1), H = tf.sigmoid(tf.matmul(K, W2) + b2)
- 현아:
- 아영:
- 승렬: 
- 지원:

### 문제2
back propagation을 간략히 서술하시오.

### 풀이
- 동건:
- 정우: 출력값과 실제값을 비교해서 거기에서나오는 cost를 뒤에서 부터 비교해서 영향(미분값을 계산하겠다.)
- 현아:
- 아영:
- 승렬:
- 지원:
---