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
3. .reset_index()
#### 8. isin 함수를 쓸때 포함하는 데이터프레임을 추출한다. 
df[df["구"].isin(gu)] 
그렇지 않은 놈을 구할때는 
간단하다. 
df[~df["구"].isin(gu)] 
#### 9. 칼람을 삭제하는 방법 
del df["거주지"]

#### .map(lambda x : x)에 대한 것들
df["거주지"].map(lambda x : x if x in gu else ("타지역"))
해석 : lambda는 익명을 말하는다. 익명 x 함수는 gu라는 변수 값에 없을시, x로 나타내고 아니라면, 타지역으로 나타내라. 
x : x -> input과 output
####
####
####
####
