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

## 정우

문제1: classification을 linear regression으로 진행하면 생기는 문제점 2가지는?

---

문제2: Cross entropy의 loss/cost는 2가지로 코딩이 가능하다. 두 가지 코드를 모두 쓰세요
