## 동건

### 문제1
역전파 알고리즘을 사용하는 이유는?

### 풀이
- 동건: 
- 정우: 
- 현아:
- 아영:
- 승렬: 예측한 값과 실제값을 비교해 나온 에러로부터 앞의 Weight과 bias를 조정해 학습시키기 위해서
- 지원:

### 문제2
f(x) = x^2, g(x) = x+b 일때, x의 변화량에 대한 f(g(x))의 변화량은?

### 풀이
- 동건:
- 정우: 
- 현아:
- 아영:
- 승렬: 2x
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
- 승렬: 
W1 = tf.Variable(tf.random_normal([2, 3]), name='weight1')
b1 = tf.Variable(tf.random_normal([3]), name='bias1')
layer1 = tf.sigmoid(tf.matmul(X, W1) + b1)

W2 = tf.Variable(tf.random_normal([3, 4]), name='weight2')
b2 = tf.Variable(tf.random_normal([4]), name='bias2')
layer2 = tf.sigmoid(tf.matmul(layer1, W2) + b2)

W3 = tf.Variable(tf.random_normal([4, 5]), name='weight3')
b3 = tf.Variable(tf.random_normal([5]), name='bias3')
hypothesis = tf.sigmoid(tf.matmul(layer2, W3) + b3)

- 지원:

### 문제2
F(X) = 3(2X + Y)^2을 X에대해 편미분해 보시오
### 풀이
- 동건:
- 정우: 
- 현아:
- 아영:
- 승렬: 12(2X + Y)
- 지원:
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
W1=[ 6, 6] , b1= -9      (1,1)일때만 1이도록  
W2=[-6,-6] , b2= 2       (0,0)일때만 1이도록  
W3=[-10,-10] , b3= 7     (0,0)일때만 1이도록  

- 지원:

### 문제2
Tensorboard에서 learning rate를 다르게 한 두개 이상의 그래프를 한번에 visualize 하기 위해서는 어떻게 해야 하는가?
### 풀이
- 동건:
- 정우: 
- 현아:
- 아영:
- 승렬: 하나의 parent directory를 만들고 그 밑에 각 그래프마다 하위 디렉토리를 만들어준다.
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
- 승렬: Deep 하다: layer가 여러개이다.  
        wide 하다: 하나의 layer를 거친 후의 출력 값이 훨씬 많아진다.
- 지원:

### 문제2
TensorBoard를 사용하는 5가지 단계에 대해 설명하시오.

### 풀이
- 동건:
- 정우: 
- 현아:
- 아영:
- 승렬:
1. 어떤 tensor를 log할건지 고르기
2. summary 만들기
3. 세션에 들어가서 어느 위치에 기록할 것인지 정한 다음에 세션에 그래프 넣어주기
4. summary 실행시키고 writer에 넣어주기
5. launch Tensorboard
- 지원:
---

## 아영

### 문제1
g=wx, f=g+b이고 δg/δw=3, δf/δg=1일 때 w가 f에 미치는 영향을 값으로 표현하면?

### 풀이
- 동건: 
- 정우: 
- 현아:
- 아영:
- 승렬: 3
- 지원:

### 문제2
learning rate가 0.1일때와 learning rate가 0.01일때의 그래프를 비교해서 보려고 한다. tensorboard를 사용해 어떻게 그래프를 구현할 수 있을까? (간단히 설명)

### 풀이
- 동건:
- 정우: 
- 현아:
- 아영:
- 승렬: 하나의 디렉토리 안에 하위 디렉토리를 2개 만든 후 parent directory를 실행시킨다.
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
K = tf.sigmoid(tf.matmul*X, W1) + b1)
hypothesis = tf.sigmoid(tf.matmul(K, W2) + b2)
- 지원:

### 문제2
back propagation을 간략히 서술하시오.

### 풀이
- 동건:
- 정우: 
- 현아:
- 아영:
- 승렬: forward propagation을 통해 나온 예측값의 에러를 가지고 다시 돌아가면서 W와 b의 값들을 조정하는 것.
- 지원:
---
