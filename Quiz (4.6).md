## 동건
문제1: log를 쓰지 않고 sigmoid 함수만으로 logistic cost 를 정의할 수 없는 이유는?

현아) sigmoid 함수만을 쓰면, cost function의 모양이 구불구불하여 global minimum을 구하기 어렵기 때문이다. 따라서 log를 활용하여 cost function을 조정해야 한다.

---
문제2:

x = 
[[[[ 0  1]
   [ 2  3]
   [ 4  5]]]


 [[[ 6  7]
   [ 8  9]
   [10 11]]]]
   
 x의 shape은?
 
 현아) shape = [2, 1, 3, 2]
 
---

## 아영
문제1: logistic (regression) classification의 cost function을 코드로 구현하면? 

현아) cost = -tf.reduce_mean(Y * tf.log(hypothesis) + (1-Y) * tf.log(1-hypothesis))

---
문제2: softmax classification 문제\
\
all = sess.run(hypothesis, feed_dict={X: [[1, 1, 0, 1], \
                                         [1, 3, 4, 3], \
                                         [1, 11, 7, 9]]}) \
    print(all, sess.run(tf.arg_max(all, 1)))에서 \
    all이 [[1.8881691e-08   3.6499070e-04   9.9963498e-01] \
 [8.7091011e-01   1.1618520e-01   1.2904739e-02] \
 [4.7080261e-03   9.9528199e-01   9.9369563e-06]]으로 나왔다면 \
 sess.run(tf.arg_max(all, 1))의 실행값은?
     
현아) [2 0 1]
     
---

## 현아
문제1: hypothesis = tf.sigmoid(tf.matmul(X,w) + b)로 선언했을 때, hypothesis의 값은 0.1, 0.8 등 0~1 사이의 다양한 값을 가질 수 있다.
이렇게 다양한 hypothesis의 값을 1.0, 0.0이라는 2가지의 값으로 바꾸는 작업을 tensorflow 코드로 표현하시오. 

현아) predicted = tf.cast(hypothesis > 0.5, dtype = tf.float32)

---
문제2: [A]와 [B]에 들어갈 알맞은 말을 쓰시오.\
\
logistic classifier로 계산된 값이 softmax 함수를 통과하고 나면 값이 변화하는데, 이렇게 변화된 결과 값은 [A] 사이에 있는 값이고, 합치면 [B]이 된다는 특성이 있다

현아) [A]: 0과 1   [B]: 1

---
## 승렬
문제1.logistic classification을 사용하면 좋을 케이스의 예를 3가지 들어보시오(스팸이랑 시험 pass fail 제외).

현아) 악성 종양 vs. 양성 종양 // 지금 이 주식을 살까 vs. 팔까 // 이 고객이 돈을 갚을까 vs. 안 갚을까

---
문제2. cross entropy는 무엇이고 어떤 이유로 사용하는지 설명하시오.

현아) ??????????????????????

## 정우

문제 1. linear Regression을 통해 classification을 하면 생기는 문제 2가지에 대해 설명해 보세요

현아) 직선으로 data를 분류하려고 하는 경우, 직선의 기울기에 따라 정확하게 분류가 안 되는 경우가 발생한다. / classification에서는 0 또는 1의 값이 나와야 하는데, H(x) = Wx + b라는 linear regression의 식의 결과값은 매우 크게 나올 수도 있다.

---

문제2. cross entropy의 loss와 cost를 구하는 방법은 두가지로 코딩할 수 있습니다 두가지를 모두 

현아) [방법1] cost = tf.reduce_mean(-tf.reduce_sum(Y * tf.log(hypothesis), axis=1))  
[방법2] cost_i = tf.nn.softmax_cross_entropy_with_logits(logits=logits, labels=Y_one_hot)

cost = tf.reduce_mean(cost_i)

