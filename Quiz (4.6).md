## 동건
문제1: log를 쓰지 않고 sigmoid 함수만으로 logistic cost 를 정의할 수 없는 이유는?

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
 
---

## 아영
문제1: logistic (regression) classification의 cost function을 코드로 구현하면? 

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
     
---

## 현아
문제1: hypothesis = tf.sigmoid(tf.matmul(X,w) + b)로 선언했을 때, hypothesis의 값은 0.1, 0.8 등 0~1 사이의 다양한 값을 가질 수 있다.
이렇게 다양한 hypothesis의 값을 1.0, 0.0이라는 2가지의 값으로 바꾸는 작업을 tensorflow 코드로 표현하시오. 

---
문제2: [A]와 [B]에 들어갈 알맞은 말을 쓰시오.\
\
logistic classifier로 계산된 값이 softmax 함수를 통과하고 나면 값이 변화하는데, 이렇게 변화된 결과 값은 [A] 사이에 있는 값이고, 합치면 [B]이 된다는 특성이 있다

---
## 승렬
문제1.logistic classification을 사용하면 좋을 케이스의 예를 3가지 들어보시오(스팸이랑 시험 pass fail 제외).

---
문제2. cross entropy는 무엇이고 어떤 이유로 사용하는지 설명하시오.
