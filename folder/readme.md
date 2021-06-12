# TIL
### 오늘 한 것 

- sql 복습과 과제

Sql – 2주차
-	모르는 거 정리 
: end와 end as 의 차이를 궁금함. 값은 똑같이만 나옴
Ex) select employee_id first_name, last_name, salary, job_id
        ,case when salary between 1 and 5000 then '낮음'
              when salary between 5001 and 10000 then '높음'
              else '최상위'
        end as salary_rank
from employees;
: case when A와 case A when의 차이 


select country_id
    ,country_name
    ,case region_id when 1 then '유럽'
                    when 2 then '아메리카'
    end region_name
from countries;

-	SQL 이번주차 해결했던거
"" (x) '' (o)
1.	Case when then 구문에서 then3 (x) then 3(o) 
when salary between 10000 and 15000 then 3 
else 9
2.	where phone_number like ‘%124%’
-	과제 (6번) 
  select * from employees
where first_name = 'David'
and salary>=6000;

select * from departments
where department_id=80;

select * from locations
where location_id=2500;

3.	Case when 구절에서 두가지가 있다. 
SELECT에서 언급을 안했다면, Case A when then (with else!!!!)
 # else는 생략도 가능하지만 기억할것!
언급을 했다면, SELECT A CASE WHEN 이렇게 바로 직역으로 쓴다.  
4.	붙이기 방법 
select first_name ||' '|| last_name as full_name from employees;
5.	where postal_code='1730'; where구문을 쓸 때 데이터값들은 항상 ‘ ‘ 적용할것!


