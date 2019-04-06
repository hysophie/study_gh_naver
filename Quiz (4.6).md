## 동건
문제1: log를 쓰지 않고 sigmoid 함수만으로 logistic cost 를 정의할 수 없는 이유는?

현아) sigmoid 함수만을 쓰면, cost function의 모양이 구불구불하여 global minimum을 구하기 어렵기 때문이다. 따라서 log를 활용하여 cost function을 조정해야 한다.

동건) 다수의 local minimun이 생기게 된다.

정우)
그래프를 그리면 울퉁불퉁한 모양이 나오는데 이렇게 되면 local minimum을 global minimum으로 착각하는 일이 벌어짐, 로그를 취해서 그래프 모양을 잡아줘야한다.

승렬) 구불구불해서 global minimum을 찾을수가 없다.


지원: sigmoid 함수만으로 logistic cost를 정의할 경우 시작점에 따라 최저점이 달라질 수 있음

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

동건) (2,1,3,2)
 
 현아) shape = [2, 1, 3, 2]
 
정우)
(3,2,2)

승렬) (2, 1, 3, 2)

## 아영
문제1: logistic (regression) classification의 cost function을 코드로 구현하면? 

현아) cost = -tf.reduce_mean(Y * tf.log(hypothesis) + (1-Y) * tf.log(1-hypothesis))

동건)  -tf.reduce_mean(Y * tf.log(hypothesis) + (1 - Y) * tf.log(1 - hypothesis))

정우)
cost = -tf.reduce_mean( Y * tf.log(hypothesis) + (1 - Y) * tf.log(1- hypothesis))


승렬) cost= tf.reduce_mean(-tf.reduce_sum(Y*tf.log(hypothesis) + (1-Y)*tf.log(1-hypothesis)))

지원: cost=tf.reduce_mean(-tf.reduce_sum(Y*tf.log(hypothesis)+(1-Y)*tf.log(1-hypothesis)))

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
   
동건) [[0,0,1],[1,0,0],[0,1,0]]
 
 정우:
[2 0 ]

승렬) [2 0 1]

---

## 현아
문제1: hypothesis = tf.sigmoid(tf.matmul(X,w) + b)로 선언했을 때, hypothesis의 값은 0.1, 0.8 등 0~1 사이의 다양한 값을 가질 수 있다.
이렇게 다양한 hypothesis의 값을 1.0, 0.0이라는 2가지의 값으로 바꾸는 작업을 tensorflow 코드로 표현하시오. 

현아) predicted = tf.cast(hypothesis > 0.5, dtype = tf.float32)

동건)  tf.cast(hypothesis > 0.5, dtype=tf.float32)

정우)
predicted = tf.cast(hypothesis > 0.5, dtype = tf.float32)

승렬) predicted = tf.cast(hypothesis > 0.5, dtype= tf.float32)

지원: predicted=tf.cast(hypothesis>0.5,dtype=tf.float32)

---
문제2: [A]와 [B]에 들어갈 알맞은 말을 쓰시오.\
\
logistic classifier로 계산된 값이 softmax 함수를 통과하고 나면 값이 변화하는데, 이렇게 변화된 결과 값은 [A] 사이에 있는 값이고, 합치면 [B]이 된다는 특성이 있다

현아) [A]: 0과 1   [B]: 1

동건) A= 0~1, B=1

정우)
A: 0과 1
B: 1

승렬) A = 0~1, B = 1

지원: [A]-0과 1, [B]-1

---
## 승렬
문제1.logistic classification을 사용하면 좋을 케이스의 예를 3가지 들어보시오(스팸이랑 시험 pass fail 제외).

현아) 악성 종양 vs. 양성 종양 // 지금 이 주식을 살까 vs. 팔까 // 이 고객이 돈을 갚을까 vs. 안 갚을까

동건) 보험사기, 부도심사 

정우) 
남자 여자, 키 180초과 180이하, 20세이상 20세 미만 

승렬) 경마 우승마 예측, 질병 유무 판단, 주가/환율 예측

지원: 페이스북 피드-show or hide, 신용카드 이상거래 탐지, 악성 종양 판정(..?)

---
문제2. cross entropy는 무엇이고 어떤 이유로 사용하는지 설명하시오.

현아) cross entropy는 softmax classifier의 cost function을 설계하는 방법입니다.

동건) 식: -sigma(yi*log(g(xi))), 클라스가 여러개인 분류모델의 비용을 측정하는 데 사용. 

정우)
실제 값과 예측된 값이 얼마나 차이가 있는지를 구하는 식, softmax classifier의 cost function을 구해야 하는데 cross entropy를 사용해야 맞았을때 값이 작아지고 틀렸을 때 값이 커짐

승렬) http://blog.naver.com/PostView.nhn?blogId=gyrbsdl18&logNo=221013188633&parentCategoryNo=3&categoryNo=&viewDate=&isShowPopularPosts=true&from=search
http://funmv2013.blogspot.com/2017/01/cross-entropy.html

지원: softmax classification에서 사용하는 cost function, 

## 정우

문제 1. linear Regression을 통해 classification을 하면 생기는 문제 2가지에 대해 설명해 보세요

현아) 직선으로 data를 분류하려고 하는 경우, 직선의 기울기에 따라 정확하게 분류가 안 되는 경우가 발생한다. / classification에서는 0 또는 1의 값이 나와야 하는데, H(x) = Wx + b라는 linear regression의 식의 결과값은 매우 크게 나올 수도 있다.

동건) 연속적인 값이므로 분류기준을 정하기 어렵다. 

승렬) 아웃라이어가 들어오면 모양이 바뀌기 때문에 옳게 예측할 수 없다. 

지원: 선형 모델을 활용할 때 기울기가 변화하면 제대로 분류할 수 없는 경우가 생김, 0 혹은 1이 아닌 예측값이 나올 수 있음(binary classification의 조건에 부합하지 않음)

---

문제2. cross entropy의 loss와 cost를 구하는 방법은 두가지로 코딩할 수 있습니다 두가지를 모두 

현아) [방법1] cost = tf.reduce_mean(-tf.reduce_sum(Y * tf.log(hypothesis), axis=1))  
[방법2] cost_i = tf.nn.softmax_cross_entropy_with_logits(logits=logits, labels=Y_one_hot)
cost = tf.reduce_mean(cost_i)

동건) tf.reduce_mean(-tf.reduce_sum(Y * tf.log(hypothesis), axis=1))  
cost = tf.reduce_mean(tf.nn.softmax_cross_entropy_with_logits_v2(logits=logits,labels=tf.stop_gradient([Y_one_hot])))

승렬) cost = tf.reduce_mean(-tf.reduce_sum(Y*tf.log(hypothesis), axis=1))

      cost_i = tf.nn.softmax_cross_entropy_with_logits(logits=logits, labels=Y_one_hot)
      cost = tf.reduce_mean(cost_i)

## 지원

문제 1. 
x_data=[[1,2],[2,3],[3,1],[4,3],[5,3],[6,2]]
y_data=[[0],[0],[0],[1],[1],[1]]
일 때 다음 코드가 맞으면 O를 틀리면 X를 적고 만약 틀렸을 경우 코드를 수정하시오.
X=tf.placeholder(tf.float32, shape=[2,None])	(     )
Y=tf.placeholder(tf.float32, shape=[6,1])	(     )

현아) (X) => 수정: [None, 2] or [6, 2]      /////   (X) => 수정: [None, 1]

동건) X, [6,2] / O

정우)
x: [none, 2]
x: [none, 1], o도될듯...?

--
문제 2.
one-hot encoding에 대해 설명하고 이를 구현하는 코드가 무엇인지 작성하시오.



승렬) X=tf.placeholder(tf.float32, shape=[None, 2]

지원: X [None,2] / O

---

문제 2.
one-hot encoding에 대해 설명하고 이를 구현하는 코드가 무엇인지 작성하시오.

현아) one-hot encoding이란 softmax로 만들어낸 probability 값을 비교하여, 최대의 probability 값을 가지는 class에 1을 배정하고 나머지 class에는 0을 배정하는 것이다.
Y_one_hot = tf.one_hot(Y, nb_classes)
Y_one_hot = tf.reshape(Y_one_hot, [-1, nb_classes])

동건) 실수값을 0과 1로 코딩하는 것. Y_one_hot = tf.one_hot(Y, nb_classes) ; Y_one_hot = tf.reshape(Y_one_hot, [-1, nb_classes])

승렬) 소프트맥스 함수를 거치면 값들을 0~1 사이의 확률로 바꿔주는데, 이 값을 다시 0이나 1로 바꿔주는 기법을 one-hot encoding이라 한다.
코드: a= sess.run(hypothesis, feed_dict = {X: [[?, ?, ?, ?], .....
print(a, sess.run(tf.arg_max(a, 1)))

지원: softmax 함수에 입력한 예측값이 확률로 표현될 때 one-hot encoding을 거치게 되면 max 값을 기준으로 1과 0으로 구현할 수 있음,
argmax를 사용하면 됨

정우)
n개의 레이블 중 확률이 가장 높은 것을 1로 만들고(hot하게) 나머지는 0으로 표현
with tf.Session()as sess:
   a = sess.run(hypothesis, feed_dict = {X: x_data})
   print(a, sess.run(tf.arg_max(a,1)))
