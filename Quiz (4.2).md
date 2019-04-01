## 동건
문제1: 
```
cost = tf.reduce_sum(tf.square(hypothesis - y_train))
````
위는 선형회귀의 비용함수이다. 코드에서 잘못된 부분을 찾고 그 이유를 설명하시오.  

---
문제2:  
gradient descent 학습 알고리즘에서 gradient는 local minimum으로 가는 최단 방향을 의미한다고 할 수 있다.  
그렇다면, desecent와 learning rate은 무엇을 의미하는가?

---
문제3:  
40명인 한 학급을 대상으로 음악, 미술, 국어, 수학 성적을 통해 EQ(감성지능)을 예측하려고 한다.  
이 때, X의 shape은 어떤 형태이며 아래의 코드에서 ?에 들어갈 숫자는?
```
X = tf.placeholder(tf.float32, shape=[?,?])
W = tf.Variable(tf.random_normal([?, ?]), name='weight')
```

## 현아
문제1:  
(A)와 (B)에 알맞은 말을 쓰시오.
```
Linear regression에서 어떤 hypothesis가 좋은지를 판단하기 위해 ( A )를 사용하고, ( A )를 구체적인 수식으로 표현하면 ( B )이다. 
```
---
문제2:  
Gradient descent algorithm에 대해서 설명하고, gradient descent algorithm이 항상 같은 답을 찾아낼 수 있게 하기 위한 조건을 서술하시오.

---
문제3:  
(A)와 (B)에 알맞은 말을 쓰시오.
```
multi-variable linear regression에서 H(x)를 계산할 때는 ( A )를 사용하는데, 그 이유는 ( B )가 많을 때 ( A )를 사용하면 계산이 편하기 때문이다.
```

## 지원
문제1:
cost function을 최소화하는 코드를 작성하시오. "cost"를 cost function으로 코딩된 변수로 간주.

---

문제2:
(A)와 (B)에 알맞은 말을 쓰시오.
```
cost function을 최소화하는 것은 (A)의 (B)을 찾는 원리와 같다.
```

---

문제3:
Matrix의 장점을 서술하시오.

---
문제4:
(A)와 (B)에 들어갈 숫자를 작성하시오.
```
변수의 갯수가 4개, Instance의 갯수가 7인 linear regression의 weight matrix는 (A) by (B)의 matrix이다.
```

## 아영
문제1:
Linear regression을 tensorflow로 구현할 때 W, b를 실행하기 전 반드시 입력해야 하는 함수는?

---
문제2:
3차원 공간에서 cost function을 설계할 때 확인해야 하는 것은?

---
문제3:
matrix에서 instance의 개수(n)는 numpy와 tensorflow에서 각각 어떻게 표시하는가?

## 정우
문제 1 :
Tensorflow mechanism 3단계를 설명해주세요

---

문제 2:
	H = X   W
[10, 5] [?, ?] [10, 2]
?를 채우고 밑줄 친 4 개의 값이 어떤 것을 뜻하는 지 각각 구하시오 

---
문제 3:
경사하강법에서 나타날 수 있는 문제점은 무엇인가요


## 승렬
문제 1:
Tensorflow에서 사용되는 placeholder는 무엇인지 설명하시오.

문제 2:
경사하강법을 사용할 때 learning rate를 너무 크거나 너무 작게 설정하면 나타날 수 있는 문제점을 서술하시오.

문제 3:
loadtext로 csv파일을 읽어오는 것의 단점을 서술하고 queue runner의 장점을 서술하시오.
