# TIL

### 오늘 한 일
입금 완료


SQL 복습(서브쿼리, 기본실습)


### 오늘 배운 일

#### 1. 
INSERT INTO EMP  ( emp_no,  salary, hire_date)
VALUES (5,  1000, SYSDATE);

오류가 남. 이유는 not_null 값을 넣어야 하는데, 안함. 

#### 2. 

INSERT INTO EMP  
VALUES (4, '신사임당', 1000, SYSDATE);

오류가 남. 왜냐면 emp_no는 기본키로 설정하였기 때문에, 중복적으로 못들어감


####
