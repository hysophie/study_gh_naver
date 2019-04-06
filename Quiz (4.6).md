## 동건
문제1: log를 쓰지 않고 sigmoid 함수만으로 logistic cost 를 정의할 수 없는 이유는?

- 동건) 다수의 local minimun이 생기게 된다.

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

- 동건) (2,1,3,2)
---

## 아영
문제1: logistic (regression) classification의 cost function을 코드로 구현하면? 

- 동건)  -tf.reduce_mean(Y * tf.log(hypothesis) + (1 - Y) * tf.log(1 - hypothesis))


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
   
 
- 동건) [[0,0,1],[1,0,0],[0,1,0]]
---

## 현아
문제1: hypothesis = tf.sigmoid(tf.matmul(X,w) + b)로 선언했을 때, hypothesis의 값은 0.1, 0.8 등 0~1 사이의 다양한 값을 가질 수 있다.
이렇게 다양한 hypothesis의 값을 1.0, 0.0이라는 2가지의 값으로 바꾸는 작업을 tensorflow 코드로 표현하시오. 

- 동건)  tf.cast(hypothesis > 0.5, dtype=tf.float32)

---
문제2: [A]와 [B]에 들어갈 알맞은 말을 쓰시오.\
\
logistic classifier로 계산된 값이 softmax 함수를 통과하고 나면 값이 변화하는데, 이렇게 변화된 결과 값은 [A] 사이에 있는 값이고, 합치면 [B]이 된다는 특성이 있다

- 동건) A= 0~1, B=1

---
## 승렬
문제1.logistic classification을 사용하면 좋을 케이스의 예를 3가지 들어보시오(스팸이랑 시험 pass fail 제외).

- 동건) 보험사기, 부도심사 

---
문제2. cross entropy는 무엇이고 어떤 이유로 사용하는지 설명하시오.

- 동건) 식: -sigma(yi*log(g(xi))), 클라스가 여러개인 분류모델의 비용을 측정하는 데 사용. 

## 정우

문제 1. linear Regression을 통해 classification을 하면 생기는 문제 2가지에 대해 설명해 보세요

- 동건) 연속적인 값이므로 분류기준을 정하기 어렵다. 

---

문제2. cross entropy의 loss와 cost를 구하는 방법은 두가지로 코딩할 수 있습니다 두가지를 모두 

- 동건) tf.reduce_mean(-tf.reduce_sum(Y * tf.log(hypothesis), axis=1))  
cost = tf.reduce_mean(tf.nn.softmax_cross_entropy_with_logits_v2(logits=logits,labels=tf.stop_gradient([Y_one_hot])))


## 지원

문제 1. 
x_data=[[1,2],[2,3],[3,1],[4,3],[5,3],[6,2]]
y_data=[[0],[0],[0],[1],[1],[1]]
일 때 다음 코드가 맞으면 O를 틀리면 X를 적고 만약 틀렸을 경우 코드를 수정하시오.
X=tf.placeholder(tf.float32, shape=[2,None])	(     )
Y=tf.placeholder(tf.float32, shape=[6,1])	(     )

- 동건) X, [6,2] / O

---

문제 2.
one-hot encoding에 대해 설명하고 이를 구현하는 코드가 무엇인지 작성하시오.

- 동건) 실수값을 0과 1로 코딩하는 것. Y_one_hot = tf.one_hot(Y, nb_classes) ; Y_one_hot = tf.reshape(Y_one_hot, [-1, nb_classes])

