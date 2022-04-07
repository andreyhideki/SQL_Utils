# SQL_Utils :panda_face::bike:

## Link's

#### [Markdown Mastering](https://guides.github.com/features/mastering-markdown/)
#### [Tech On The Net](https://www.techonthenet.com/index.php)
#### [OracleTutorial](https://www.oracletutorial.com)
#### [SQL Server Docs Date Time](https://docs.microsoft.com/pt-br/sql/t-sql/functions/date-and-time-data-types-and-functions-transact-sql?view=sql-server-2017)
####

## Oracle

```
SELECT SYSDATE,
       TO_CHAR(SYSDATE,'DD'),
       TO_CHAR(SYSDATE,'MM'),
       TO_CHAR(SYSDATE,'MON'),
       TO_CHAR(SYSDATE,'RRRR'),
       TO_CHAR(SYSDATE,'HH24:MI:SS'),
       TO_CHAR(TO_DATE(SYSDATE),'MM/RRRR'),
       TRUNC(SYSDATE,'MONTH'),
       TRUNC(SYSDATE, 'MONTH')-1,
       TRUNC(SYSDATE, 'YEAR'),
       TRUNC(LAST_DAY(SYSDATE)),
       TO_CHAR(SYSDATE,'DD/MM/RRRR HH24:MI:SS'),
       TO_CHAR(SYSDATE,'DD/MM/RRRR'),
       LAST_DAY(ADD_MONTHS(SYSDATE,-2))+1,
       LAST_DAY(ADD_MONTHS(SYSDATE,-1)),
       TO_DATE(TRUNC(LAST_DAY(ADD_MONTHS(SYSDATE,-2)))+1,'DD/MM/RRRR'),
       floor(MONTHS_BETWEEN(SYSdate,SYSDATE-60) /12) + 1 AS MONTHS_BETWEEN,
       MONTHS_BETWEEN(SYSdate,SYSDATE-60) AS MONTHS_BETWEEN,
       ADD_MONTHS(SYSDATE,-12)
  FROM DUAL
```

Exemplo Rank:
```
SELECT PRODUTO, CATEGORIA, RANK () OVER ( ORDER BY PRODUTO) RANKINGPROD, DENSE_RANK () OVER ( ORDER BY CATEGORIA) RANKINGCAT
  FROM (
SELECT 'p1' AS PRODUTO, 'c1' AS CATEGORIA FROM DUAL
UNION ALL
SELECT 'p2' AS PRODUTO, 'c1' AS CATEGORIA FROM DUAL
UNION ALL
SELECT 'p3' AS PRODUTO, 'c1' AS CATEGORIA FROM DUAL
UNION ALL
SELECT 'p4' AS PRODUTO, 'c2' AS CATEGORIA FROM DUAL
UNION ALL
SELECT 'p5' AS PRODUTO, 'c2' AS CATEGORIA FROM DUAL) AX
```

## SQL Server

```
select convert(datetimeoffset,'01/01/2018') --2018-01-01 00:00:00.0000000 +00:00
```

```
select SYSDATETIMEOFFSET() --2018-07-16 11:17:07.0469589 -03:00
```

``` 
select convert(int,CONVERT(CHAR(10), GETDATE(),112))  --20180716
```



