# TIL

### 오늘 배운 일

1. sort index 조심하자


2. dayofweek="월화수목금토일"
dayofweek[1]

def find_dayofweek(day_no):
    dayofweek = "월화수목금토일"
    return dayofweek[day_no]

df_hot["dayofweek"]=df_hot["dayofweek"].apply(find_dayofweek)


3.
