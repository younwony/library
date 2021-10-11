# GROUP BY 절이 포함된 SQL 문의 실행 순서
 
 - SQL 문은 실행 순서가 없는 비절차적인 언어이지만 SQL 문은 내부적으로 실행 순서가 있다.

```sql
    SELECT CUSTID, COUNT(*) as 도서수량              - 5
    FROM ORDERS                                     - 1
    WHERE SALEPRICE >= 8000                         - 2
    GROUP BY CUSTID                                 - 3
    HAVING  COUNT(*) > 1                            - 4
    ORDER BY CUSTID;                                - 6
```