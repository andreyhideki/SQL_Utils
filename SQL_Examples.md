'''
SELECT * 
  FROM CLI;
'''

SELECT prod.id, count(*) 
  FROM products prod 
 GROUP BY prod.id;

SELECT prod.id, prod.name 
  FROM products prod
 WHERE prod.name like '%pro%';

SELECT MAX(price), MIN(price) FROM vendas;

SELECT AVG(price) FROM vendas;

SELECT SUM(price) FROM vendas;

SELECT id,
       CASE 
        WHEN categ = 1 then 'T1'
        WHEN categ = 2 then 'T2'
        WHEN categ = 3 then 'T3'
        ELSE 'TT'
       END
 FROM vendas;

SELECT id, categ, count(*) 
FROM vendas
group by categ 
HAVING COUNT(*) > 1;

WITH vend AS
(
    SELECT * FROM vendas
)
SELECT * FROM vend;

select nome, salario, AVG(salario)
OVER(PARTITION BY departamento) FROM colaboradores