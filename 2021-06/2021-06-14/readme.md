# TIL

### 오늘 한 것 
빡셌다...


### 오늘 몰라서 적었던 것!

!!!중요한 점은 df.loc[0]은 index를 지정하지 않을때 불가능하다.
index를 dates로 지정하게 된다면 df.loc[dates[0]]이 가능하다.

loc와 iloc의 차이는 loc는 인덱스를 말하며, iloc는 인덱스가 필요없으며, 위치를 뜻한다.

필터링 함수는 isin을 사용한다! ex)df2[df2['E'].isin(['two','four'])]

결측치를 가지고 있는 행들을 지울때 다음과 같이 한다. ex)df1.dropna(how='any')
결측치를 채울때 ex) df1.fillna(value=5)

h : 다양한 주피터 노트북의 단축키를 확인
앞뒤 공백 제거하기 : strip
startswtith을 사용하면, 특정문자가 포함되는지 알 수 있습니다.
" ".join(리스트)를 사용하면 리스트를 공백 문자열을 연결할 수 있습니다.

### 그냥 오늘 학교 시험봄!

import random

for i in range(5):
    time=random.randint(1,24)
    x=int(input("몇 명이 타십니까?"))
    y=int(input("몇 킬로를 갑니까?"))
    fare=500
    if y>10:
          y=y-10
          y=y//2
          fare=fare+100*y
    elif y>=100:
          print("운행할 수 없음")
    else: 
          fare=fare
    
    if time>=22:
          fare=fare*1.2
    elif time>=1 and time<4:
          fare=fare*1.5
    elif time>=4 and time<7:
          print("운행할 수 없음")
    else: 
          fare=fare
    
    if x<5:
          fare1=fare+500+400*(x-1)
    else:
          print("운행할 수 없음")
          
    print("======================")
    print(i+1, "번 고객")
    print("사람수:",x)
    print("시간:",time)
    print("킬로:",y)
    print("금액:",fare)
    print("=====================")
    print("최종금액:",fare1)
