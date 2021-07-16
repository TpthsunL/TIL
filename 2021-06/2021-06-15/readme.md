# TIL

### 오늘 한 일


### 오늘 알았던 일

##### 1. 한글 폰트 깨질때 사용해야 하는 것!

import matplotlib.pyplot as plt

plt.rc('font', family = 'Malgun Gothic')
plt.rc('axes', unicode_minus = False)
%matplotlib inline

또는 

import matplotlib.pyplot as plt
plt.rc ('font', family='NanumGothic')
plt.rc('axes', unicode_minus=False)

그래프가 노트북 안에 보이게 하기 위해
%matplotlib inline


##### 2. df["상욱"]["와우"]
= df.loc[df["상욱"]>10,"와우"]

##### 3. nunique와 unique의 차이
nunique는 전체를 뜻하며, ex) df.nunique()
unique는 지정한 데이터들을 보여줄때 사용한다. ex) df["mpg"].unique()

##### 4. 왜도와 첨도

왜도 : 
    음수일 때는 왼쪽 부분에 긴 꼬리를 가지며, 자료가 오른쪽에 더 많이 분포했다. 
    양수일 때는 오른쪽 부분에 긴 꼬리를 가지며, 자료가 왼쪽에 더 많이 분포한다. 
    
첨도 : 3보다 크면 정규분포보다 더 완만 3보다 작으면 뾰족

##### 5. 시각화 그래프
boxplot : describe꺼 
violinplot : boxplot 보완
scatterplot : 두 개 이상의 변수를 비교하기 위해 
residplot : 중심에서 얼마나 떨어져 있는지 보기 위해 
lmplot : unique를 중심으로 3분할로 분류해서 색깔도 씌우고 보여주기 위해 사용 .
ex) sns.lmplot(data=df, x="weight", y="mpg", hue='origin', col='origin', truncate=False, ci=None)
hue는 전체적으로 똑같은 색깔입혀서 보여주고 싶은 칼럼, col은 각각 나눠서 색깔 입히고 싶은 칼럼을 말한다.
joinplot : 2개의 변수를 묶어서 표현하기 (kind 라는 옵션이 있는데, 이것은 어떤 그래프로 나타내주고 싶은지를 결정한다. hex: 밀도)
lineplot : 연속형 변수를 표현하기
relplot : ???
heatmap : 야구에서 많이 쓰이는 heatmap인데 포수쪽 앉아있을때, 타자의 타구에 대한 것을 의미한다. 
이것은 mask 옵션을 사용한다면, 삼각행령의 위쪽을 없앨수도 있다. 
mask 변수를 만들어야 하는데, 다음 만드는 코딩은 아래와 같다. 
1. np.triu: matrix를 상 삼각행렬로 만드는 numpy math
    
2. np.ones_like(x) : x와 크기만 같은 1로 이루어진 array를 생성하는일이다. 

3. mask=np.triu(np.ones_like(corr))
   mask
##### 6. 상관계수
1~0.7 사이는 강한 상관을 뜻하며, -1~-0.7 사이는 강한 부정을 뜻한다. 
#####
#####
