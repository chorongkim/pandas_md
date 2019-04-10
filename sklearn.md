# Scikit-learn

- 머신러닝
![](img/ml_map.png)

1. 지도학습 : Supervised learing<br>
1) 회귀 : Regression<br>
2)  분류 : Classification <br>
3)  랭킹<br>

2. 비지도학습 : Unsupervised learning<br>

3. 강화학습 : Reinforcement learning<br>

## 1) sckit을 이용한 기본학습과정

<pre><code>from sklearn.datasets import load_iris
from sklearn.datasets import load_boston

pd_data=pd.DataFrame(iris.data, columns=iris.feature_names)
pd_target=pd.DataFrame(iris.target, columns=['target'])
pd.concat([pd_data, pd_target], axis=1)
</pre></code>
1. data를 dataframe형태로 만들어줌<br>
2. targetdata도 datafram으로 만들어줌<br>
3. concat을 이용하여 두 데이터 붙여줌<br>

<pre><code>
from sklearn.neighbors import KNeighborsClassifier
knn= KNeighborsClassifier()
knn.fit(a.iloc[:,:-1],a.target) >> data, taget넣기 
knn.predict([[3,1,2,3]])
iris.target_names

knn.predict([s.iloc[2,:-1].values])
knn.predict([s.iloc[2,:-1]]) >> 학습데이터 확인
s.iloc[2] >> 학습데이터 결과값 
</code></pre>

1. 객체화하기(해당모델을 적절하게 설정 / ex) k값)<br>
2. fit(학습)시키기<br>
3. 검증데이터로 predict해보기<br>
4. 검증데이터 정확도 확인하기<br>

## 2) HoldOut

## 3) Cross validation