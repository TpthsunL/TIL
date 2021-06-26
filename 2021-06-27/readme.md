# TIL

### 오늘 한 일
- 파이썬 과제 모두 제출
- 피자 먹기
- 미팅 가기
- 그래프 모두 마스터하기 (예정)
- sql 지금까지 한거 한번 복습하기 (예정)
- 공공데이터 자료 수집 인프런 강의 모두 듣기 (예정)

### 오늘 배운 일

#### 1. sort_values 여러개 열 같이 나오게 하는 방법과 순위 매기기 
- df.sort_values(by='total', ascending=False).groupby('name', sort=False).head(3)
- df.groupby('name').apply(lambda x: x.nlargest(3, 'total'))

-> 가장 빠른 방법은 두번째이다. 

#### 2. 혼합 정렬
df.sort_values(by=['carat', 'depth'], ascending=[False, True]).head(5)

#### 3. 조심하자. 
df.loc[(df['cut']=='Ideal')&(df['color']=='G')

#### 4. 파이썬 질문 
df['category']=df['price'].copy()
df.loc[df['category']<900,'category']='low'
df.loc[df['category']>2000,'category']='high'

#### 5. 이것을 포함하는 여부 
isin(values)
 * 구성된 애들이 있는 놈들만 데이터프레임화 시키기 : df[df['clarity'].isin(top_index)]
####
####
####
####
