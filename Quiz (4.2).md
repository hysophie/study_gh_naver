##test - test

## 동건
문제1: 
```
cost = tf.reduce_sum(tf.square(hypothesis - y_train))
````
위는 선형회귀의 비용함수이다. 코드에서 잘못된 부분을 찾고 그 이유를 설명하시오.  

- 동건) tf.reduce_sum -> tf.reduce_mean 평균이 아닌 합으로 하면 정확도와 상관없이 인스턴스가 증가함에 따라서 비용이 증가한다.
- 정우) tf.reduce_mean으로 바꿔야합니다. 
---
문제2:  
gradient descent 학습 알고리즘에서 gradient는 local minimum으로 가는 최단 방향을 의미한다고 할 수 있다.  
그렇다면, desecent와 learning rate은 무엇을 의미하는가?

- 동건) desecent는 기울기의 반대방향으로 하강한다는 의미이다. 즉 weight를 learning 할 때 gradient앞에 '-'가 붙는 것과 상응된다. 
learning rate은 보폭에 비유할 수 있는데, 기울의 반대방향으로 얼머만큼 갈 지를 정하는 부분으로 '알파'라고도 한다. 

---
문제3:  
40명인 한 학급을 대상으로 음악, 미술, 국어, 수학 성적을 통해 EQ(감성지능)을 예측하려고 한다.  
이 때, X의 shape은 어떤 형태이며 아래의 코드에서 ?에 들어갈 숫자는?
```
X = tf.placeholder(tf.float32, shape=[?,?])
W = tf.Variable(tf.random_normal([?, ?]), name='weight')
```

- 동건) 40,4,4,1

## 현아
문제1:  
(A)와 (B)에 알맞은 말을 쓰시오.
```
Linear regression에서 어떤 hypothesis가 좋은지를 판단하기 위해 ( A )를 사용하고, ( A )를 구체적인 수식으로 표현하면 ( B )이다. 
```

- 동건) A=MSE B=(1/m)*sigma(y-yhat)*2

---
문제2:  
Gradient descent algorithm에 대해서 설명하고, gradient descent algorithm이 항상 같은 답을 찾아낼 수 있게 하기 위한 조건을 서술하시오.  

- 동건) 목표지점에 이르는 가장 빠른 경사를(gradient)를 찾아 경사의 반대방향(descent)로 학습하는 최적화 알고리즘.  
미분 가능해야하며 하나의 global minimum 이 존재. 

---
문제3:  
(A)와 (B)에 알맞은 말을 쓰시오.
```
multi-variable linear regression에서 H(x)를 계산할 때는 ( A )를 사용하는데, 그 이유는 ( B )가 많을 때 ( A )를 사용하면 계산이 편하기 때문이다.
```

- 동건) A: matrix B: varible의 수

## 지원
문제1:
cost function을 최소화하는 코드를 작성하시오. "cost"를 cost function으로 코딩된 변수로 간주.

- 동건) train = tf.train.GradientDescentOptimizer(learning_rate=0.1).minimize(cost)

---

문제2:
(A)와 (B)에 알맞은 말을 쓰시오.
```
cost function을 최소화하는 것은 (A)의 (B)을 찾는 원리와 같다.
```
---

- 동건) A: cost funtion의 편미분 함수 B: 값이 0이 되는 지점을  

문제3:
Matrix의 장점을 서술하시오.

- 동건) 연산을 간단하게 할 수 있다.  

---
문제4:
(A)와 (B)에 들어갈 숫자를 작성하시오.
```
변수의 갯수가 4개, Instance의 갯수가 7인 linear regression의 weight matrix는 (A) by (B)의 matrix이다.
```

- 동건) A=4 B=1

## 아영
문제1:
Linear regression을 tensorflow로 구현할 때 W, b를 실행하기 전 반드시 입력해야 하는 함수는?

- 동건) sess.run(tf.global_variables_initializer())

---
문제2:
3차원 공간에서 cost function을 설계할 때 확인해야 하는 것은?

- 동건) input과 output의 shape 

---
문제3:
matrix에서 instance의 개수(n)는 numpy와 tensorflow에서 각각 어떻게 표시하는가?

- 동건) -1, None // np.float, tf.float32

## 정우
문제 1 :
Tensorflow mechanism 3단계를 설명해주세요

- 동건)  
1. graph를 그리기
2. sess.run을 통해 데이터를 입력하고 학습을 시작하기.
3. 학습을 하면서 값을 업데이트하고 리턴하기. 

---

문제 2:
	H = XW  
[10, 1] = [?, ?] [5, 1]  
?를 채우고 밑줄 친 4 개의 값이 어떤 것을 뜻하는 지 각각 구하시오 

- 동건) 10,5

---
문제 3:
경사하강법에서 나타날 수 있는 문제점은 무엇인가요

- 동건) local minimum이 여러개 일 수 있다. 

## 승렬
문제 1:
Tensorflow에서 사용되는 placeholder는 무엇인지 설명하시오.

- 동건) 변수 타입을 미리 설정해놓고 필요한 변수를 나중에 받아서 실행시킬 수 있는 것. 특히 인스턴스의 개수를 모를 때 값을 None으로 할당하고 그래프를 먼저 그리면(1단계), sess.run(2단계)에서 feed_dict을 통해 데이터를 주고 학습을 시킬 수 있다.  

문제 2:
경사하강법을 사용할 때 learning rate를 너무 크거나 너무 작게 설정하면 나타날 수 있는 문제점을 서술하시오.

- 동건) 너무 크면 local minimum으로 수렴하지 않을 수 있고 너무 작으면 시간이 너무 오래걸린다. 

문제 3:
loadtext로 csv파일을 읽어오는 것의 단점을 서술하고 queue runner의 장점을 서술하시오.

- 동건) 데이터의 자료형이 동일해야한다. 대용량 데이터를 사용할 때, 메모리를 효율적으로 사용할 수 있다. 
