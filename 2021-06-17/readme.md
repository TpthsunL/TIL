# TIL

### 오늘 한 일

### 오늘 배웠던 일

#### 1. 판다스 안에서는 datatypes Object인 경우는 str을 함수 앞에 쓰는 경우가 교과서적이다. 그냥 써라.

#### 2. sql에서 replace함수는 많이 쓰이므로 알아두자. 
select replace(phone_number, '.','-') 
from employees; 

#### 3. pivot_table 
pdf1 = pd.pivot_table(df,                # 피벗할 데이터프레임
                     index = 'class',    # 행 위치에 들어갈 열
                     columns = 'sex',    # 열 위치에 들어갈 열
                     values = 'age',     # 데이터로 사용할 열
                     aggfunc = 'mean')   # 데이터 집계함수
pdf1

#### 4. groupby를 활용해서 agg를 이용하다면, 여러 개의 함수를 사용해 연산이 포함된 데이터프레임을 얻을 수 있다.
df.groupby(["deck"])["fare"].agg(["count", "mean", "sum"])

#### 5. 결측치를 삭제할때는 drop.na() 함수를 사용한다. 중요한 점은 안에 들어가는 옶션이다. 
시프트 탭키로 안에 있는 매개변수들을 본다. axis=0으로 행으로 고정되어 있다. 따라서 how='any'를 쓰게 되면, 행 또는 열에 대하여 결측치가 하나라도 있으면 삭제할때 사용한다. 
모든 값이 결측치여야 삭제할 것인지를 how= "all"로 결정한다. 
#### 6. korea_data.dropna(subset=['행정구역']) 
다음 매개변수를 사용해서 쓰게 된다면, 행정구역 칼럼에서 결측치들을 제거하는 역할을 한다. 

####
####
####
####
####
####
