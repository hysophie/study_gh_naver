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
```
(A)와 (B)에 알맞은 말을 쓰시오.
```
Linear regression에서 어떤 hypothesis가 좋은지를 판단하기 위해 ( A )를 사용하고, ( A )를 구체적인 수식으로 표현하면 ( B )이다. 

---
문제2:  
Gradient descent algorithm에 대해서 설명하고, gradient descent algorithm이 항상 같은 답을 찾아낼 수 있게 하기 위한 조건을 서술하시오.

---
문제3:  
(A)와 (B)에 알맞은 말을 쓰시오.
```
multi-variable linear regression에서 H(x)를 계산할 때는 ( A )를 사용하는데, 그 이유는 ( B )가 많을 때 ( A )를 사용하면 계산이 편하기 때문이다.
```
