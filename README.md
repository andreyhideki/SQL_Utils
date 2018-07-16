# SQL_Utils

## Link's

#### https://www.techonthenet.com/index.php
#### https://docs.microsoft.com/pt-br/sql/t-sql/functions/date-and-time-data-types-and-functions-transact-sql?view=sql-server-2017
####

## Oracle

```
SELECT SYSDATE,
       TO_CHAR(SYSDATE,'DD'),
       TO_CHAR(SYSDATE,'MM'),
       TO_CHAR(SYSDATE,'MON'),
       TO_CHAR(SYSDATE,'RRRR'),
       TO_CHAR(SYSDATE,'HH24:MI:SS'),
       TRUNC(SYSDATE,'MONTH'),
       TRUNC(LAST_DAY(SYSDATE)),
       TO_CHAR(SYSDATE,'DD/MM/RRRR HH24:MI:SS'),
       TO_CHAR(SYSDATE,'DD/MM/RRRR')
  FROM DUAL
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



