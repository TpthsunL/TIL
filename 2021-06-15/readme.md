# TIL

### 오늘 한 일


### 오늘 알았던 일

1. 한글 폰트 깨질때 사용해야 하는 것!

import matplotlib.pyplot as plt

plt.rc('font', family = 'Malgun Gothic')
plt.rc('axes', unicode_minus = False)
%matplotlib inline

또는 

import matplotlib.pyplot as plt
### Window 의 한글 폰트 설정 > 차트에서 깨짐 방지
plt.rc ('font', family='NanumGothic')
plt.rc('axes', unicode_minus=False)

### 그래프가 노트북 안에 보이게 하기 위해
%matplotlib inline


2. df["상욱"]["와우"]
= df.loc[df["상욱"]>10,"와우"]
