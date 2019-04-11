## 동건

### 문제1
역전파 알고리즘을 사용하는 이유는?

### 풀이
- 동건: 
- 정우: 
- 현아:
- 아영:
- 승렬:
- 지원: 각각의 변수가 결과값에 미치는 영향을 확인하기 위해

### 문제2
f(x) = x^2, g(x) = x+b 일때, x의 변화량에 대한 f(g(x))의 변화량은?

### 풀이
- 동건:
- 정우: 
- 현아:
- 아영:
- 승렬:
- 지원: 2x+b+1
---
## 정우

### 문제1
Layer가 3개이며, layer1은 2개를 입력받고, layer 2는 3개 입력, 1ayer 3은 4개를 입력받고 5개를 출력하는 NN을 코딩해보시오. (W1 = ~에서 시작해서,hypothesis = ~ 라인까지만 하시면 됩니다)

### 풀이
- 동건: 
- 정우: 
- 현아: 
- 아영:
- 승렬: 
- 지원:
W1=tf.Variable(tf.random_normal([2,3]), name=’weight1’)
b1=tf.Variable(tf.random_normal([3]), name=’bias1’)
layer1=tf.sigmoid(tf.matmul(X,W1)+b1)
W2=tf.Variable(tf.random_normal([3,4]), name=’weight2’)
b2=tf.Variable(tf.random_normal([4]), name=’bias2’)
layer2=tf.sigmoid(tf.matmul(X,W2)+b2)
W3=tf.Variable(tf.random_normal([4,5]), name=’weight3’)
b3=tf.Variable(tf.random_normal([5]), name=’bias3’)
layer3=tf.sigmoid(tf.matmul(X,W3)+b3)
W4=tf.Variable(tf.random_normal([5,1]), name=’weight4’)
b4=tf.Variable(tf.random_normal([1]), name=’bias4’)
hypothesis=tf.sigmoid(tf.matmul(K,W3)+b3)


### 문제2
F(X) = 3(2X + Y)^2을 X에대해 편미분해 보시오
### 풀이
- 동건:
- 정우: 
- 현아:
- 아영:
- 승렬:
- 지원: 12(2x+y)
---

## 승렬

### 문제1. 
Find another W and b for the XOR. (lec9-1 11:43 그림 참조)

### 풀이
- 동건: 
- 정우: 
- 현아: 
- 아영:
- 승렬: 
- 지원: ([5/5],-8) / ([-7/-7],-3) / ([-11/-11],-6)

### 문제2
Tensorboard에서 learning rate를 다르게 한 두개 이상의 그래프를 한번에 visualize 하기 위해서는 어떻게 해야 하는가?
### 풀이
- 동건:
- 정우: 
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
- 정우: 
- 현아: 
- 아영:
- 승렬: 
- 지원: wide-output이 많은 것 / deep-layer가 많은 것

### 문제2
TensorBoard를 사용하는 5가지 단계에 대해 설명하시오.

### 풀이
- 동건:
- 정우: 
- 현아:
- 아영:
- 승렬:
- 지원: 1. 어떤 값에 log를 취할건지 정함 / 2. 한 번에 쓰기 위해 merge / 3. session에 들어가서 파일의 위치를 정하고 그래프를 넣음 / 4. summary(tensor) 실행하고 파일에 기록 / 5. tensorboard 실행
---

## 아영

### 문제1
g=wx, f=g+b이고 δg/δw=3, δf/δg=1일 때 w가 f에 미치는 영향을 값으로 표현하면?

### 풀이
- 동건: 
- 정우: 
- 현아:
- 아영:
- 승렬: 
- 지원: 3

### 문제2
learning rate가 0.1일때와 learning rate가 0.01일때의 그래프를 비교해서 보려고 한다. tensorboard를 사용해 어떻게 그래프를 구현할 수 있을까? (간단히 설명)

### 풀이
- 동건:
- 정우: 
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
- 정우: 
- 현아:
- 아영:
- 승렬: 
- 지원:

### 문제2
back propagation을 간략히 서술하시오.

### 풀이
- 동건:
- 정우: 
- 현아:
- 아영:
- 승렬:
- 지원:
---
