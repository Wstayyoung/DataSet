**SELECT**  
SELECT column1, column2, ...  
FROM table_name;  

**AND OR NOT**  

**NULL**  
It is not possible to test for NULL values with comparison operators, such as =, <, or <>.  

We will have to use the IS NULL and IS NOT NULL operators instead.  

MySQL 使用三值逻辑 —— TRUE, FALSE 和 UNKNOWN。任何与 NULL 值进行的比较都会与第三种值 UNKNOWN 做比较。这个“任何值”包括 NULL 本身！这就是为什么 MySQL 提供 IS NULL 和 IS NOT NULL 两种操作来对 NULL 特殊判断。  

**IN**  
The IN operator allows you to specify multiple values in a WHERE clause.  

The IN operator is a shorthand for multiple OR conditions.  

SELECT *column_name(s)*  
FROM *table_name*  
WHERE *column_name* IN (*value1*, *value2*, ...);  

or:  

SELECT *column_name(s)*  
FROM *table_name*  
WHERE *column_name* IN (*SELECT STATEMENT*);  

**CASE**  
The CASE expression goes through conditions and returns a value when the first condition is met (like an if-then-else statement). So, once a condition is true, it will stop reading and return the result. If no conditions are true, it returns the value in the ELSE clause.  

If there is no ELSE part and no conditions are true, it returns NULL.  

CASE  
    WHEN *condition1* THEN *result1*  
    WHEN *condition2* THEN *result2*  
    WHEN *conditionN* THEN *resultN*  
    ELSE *result*  
END;  

**AS**  
The AS command is used to rename a column or table with an alias.  

An alias only exists for the duration of the query.  

**GROUP_CONCAT**  
GROUP_CONCAT(DISTINCT expression  
    ORDER BY expression  
    SEPARATOR sep);  
类似于把SELECT v FROM t GROUP BY v;语句的结果串接起来。  
![](https://github.com/Wstayyoung/DataSet/blob/main/img/GROUP_CONCAT.png)


