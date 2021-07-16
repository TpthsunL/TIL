# TIL

### 오늘 한 일

### 오늘 알게 된 것

#### 1. 짠짠한 것. 
- CI=NONE은 데이터가 많을수록 써야한다

- lineplot은 연속형, barplot은 범주형

- df["연번"].nunique()

- 인덱스를 지정하는 방법
  df=df.set_index("연번")

#### 2. pivot_table로도 계산이 가능하다. 
마치 groupby써서, mean()구하는거랑 똑같다.
pd.pivot_table(data=df, index="origin", values="mpg")

#### 3. unstack() 
df.groupby(["cylinders, "origin"])["mpg"].mean().unstack()


#### 4. 함수정의
def find_dayofweek(day_no):
    dayofweek = "월화수목금토일"
    return dayofweek[day_no]

df["요일명"]=df["요일"].map(find_dayofweek)
* 여기서 map은 시리즈만 사용할 수 있는데 이것으로 시리즈에게 덮어쓰일때 사용된다는 것이다. 

#### 5. oc와 iloc에 대한 차이점 명확히 이해함. 
####
####
####
####
####
####
