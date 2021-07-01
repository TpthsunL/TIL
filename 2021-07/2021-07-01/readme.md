# TIL 


### 오늘 한 일
kaggle code 따라하면 데이터분석 실력 급등 


### 오늘 배운 일

#### 1. 마케팅 분야 분석내용
LTV : 고객 평생 가치 분석
시장 세분화
최근 성, 빈도, 통화 모델
A / B 테스트
Churn : 고객 이탈 예측
코호트 분석 : 이번달에 구매한 사람들이 다음달에 구매하는 것을 분석함.


#### 2. 결측치 히트맵
sns.heatmap(df.isnull(), cmap='Greys_r' )  
없는 거만 하얗게는 greys_r
없는 거는 거멓게 greys 

#### 3. 중복 제거
drop_duplicates로 중복을 제거.
print(df.shape)
df = df.drop_duplicates()
df.shape

#### 4. 히트맵
sns.heatmap(cohort_counts, cmap='Blues', annot=True, fmt='.0f')
fmt ='.0f' : 소수점은 체크하지 않는다. ex).1f : 소수점 한자리까지
annot = True : 숫자가 체크되게끔


#### 5. 나누기의 다른 형식 
div를 쓰게 되면 행을 지정할 수 있어서 나눌때는 이렇게 이용한다. 
