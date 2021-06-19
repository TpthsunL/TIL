# TIL

### 오늘 한 일

### 오늘 배운 것

#### 1. 속도측정방법
%timeit
예를 들어, df.iloc의 속도를 측정한 결과,
df.iloc[1,7] 이런 형태가 df.iloc[0]["확진일자"]보다 빨랐음을 알 수 있다. 

#### 2. 누적수 : cumsum()
#### 3. .astype(str).map(lambda x : x[-5:])
2020-01-01에서 01-01만 가져오기 

#### 4. datetime 이라는 변수에서 
dt.month
dt.dayofweek 를 사용할 경우, (월별, 요일별)을 뽑아내게 된다. 
#### 5. value_counts는 시리즈 x 
#### 6. unstack()
groupby로 두개를 묶은 인덱스를 데이터프레임으로 나누어 값을 표현한다. 

#### 7. 시리즈를 데이터프레임으로 만드는 방법 3가지
1.pd.DataFrame
2. to_frame()
3. .reset_index() <-> set_index()
#### 8. isin 함수를 쓸때 포함하는 데이터프레임을 추출한다. 
df[df["구"].isin(gu)] 
그렇지 않은 놈을 구할때는 
간단하다. 
df[~df["구"].isin(gu)] 
#### 9. 칼람을 삭제하는 방법 
del df["거주지"]

#### 10. .map(lambda x : x)에 대한 것들
df["거주지"].map(lambda x : x if x in gu else ("타지역"))
해석 : lambda는 익명을 말하는다. 익명 x 함수는 gu라는 변수 값에 없을시, x로 나타내고 아니라면, 타지역으로 나타내라. 
x : x -> input과 output
#### 11. 숫자 세는 거
시리즈는 value_counts()
데이터프레임은 count()
#### 12. merge는 데이터 프레임만 가능하다. 

#### 13. import re : 정규표현식 라이브러리
: 숫자와의 데이터는 제거하는 정규표현식 

#### 14. 역슬래시를 사용할때가 있다. 
str.replace("(퇴원)","") -> 결과값이 () 이것은 제외를 못한다. 왜냐면 정규표현식에서 이것은 제외하지 말고 남기라는 뜻

#### 15. merge에서
how="outer" : 합집합
how="inner" : 교집합

#### 16. rolling은 추세선 그릴때 사용
#### 17. 막대그래프는 가로만 신경써야하지만, 히스토그램은 가로세로 모두다 신경써야함.
#### 18. 차분과 내려쓰기 
df4['a_diff'] = df4["a"].diff() #diff는 차분값을 말한다. 
df4['a_shift'] = df4["a"].shift(1) #shift는 ()값 밑으로 내려쓰게 끔 해준다. 
df4['a_minus'] = df4["a"]-df4['a_shift']
df4[['a','a_shift','a_minus','a_diff']]

#### 19. alpha는 투명도를 의미한다. 
#### 20. 비모수적 방법 (kernel density estimate plot)
kernel density estimate plot은 비모수적 방법이다. 비모수적 방법은 모집단의 형태에 관계없이 주어진 데이터에서 직접 확률을 계산하는 통계방법
비모수적 방법 조건 : 정규분포가 아닐때, 정규뷴포로 적절히 변환되지 못할때 비모수적 방법 특징 : 많은 표본을 추출하기 어려운 경우에 적합!
####
####
####
####

