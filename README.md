## Select
```SQL
SELECT * FROM users 
SELECT name, age FROM users
SELECT name, age, birthday FROM users ORDER BY name, age DESC
```

## Select DISTINCT
```SQL
SELECT DISTINCT state FROM customers;
SELECT DISTINCT state FROM customers ORDER BY state DESC
SELECT DISTINCT state, city FROM customers WHERE state IS NOT NULL
```

## Select Where
```SQL
SELECT * FROM users WHERE name = 'Shvan'
SELECT * FROM users WHERE birthday >= '2000-02-15'
SELECT * FROM users WHERE dept = value1
SELECT * FROM users WHERE dept <> value1
SELECT * FROM users WHERE dept IS NULL
SELECT * FROM users WHERE dept IS NOT NULL
SELECT * FROM users WHERE dept IS IN (value1, value2)
SELECT * FROM users WHERE dept IS NOT IN (value1, value2)
```

## Select Like
```SQL
SELECT * FROM users WHERE dept LIKE 'd%';
SELECT * FROM users WHERE dept LIKE 'dev%';
SELECT * FROM users WHERE dept LIKE '%t';
SELECT * FROM users WHERE dept LIKE '%e%';
SELECT * FROM users WHERE dept NOT LIKE 'd%';
```

## Select Advance where
```SQL
SELECT * FROM users WHERE age BETWEEN 20 AND 25;
SELECT * FROM users WHERE age = 17 OR points >= 7
SELECT * FROM users WHERE name = 'shvan' OR age >= 15
SELECT * FROM users WHERE birthday >= '2006-02-15' and points >= 5
SELECT * FROM users WHERE (age = 17 AND name = 'shvan') OR points >= 7

SELECT * FROM orders WHERE requireddate 
    BETWEEN CAST('2003-01-01' AS DATE) AND CAST('2003-01-31' AS DATE);
```

## Select Aggregate Functions
```SQL
SELECT COUNT(id) FROM users;
SELECT MAX(age) FROM users;
SELECT MIN(age) FROM users;
SELECT SUM(age) FROM users;
SELECT UCASE(first_name), LCASE(last_name) FROM users;
```

## Group By
```SQL
SELECT city,COUNT(*) as count FROM customers GROUP BY city ORDER BY count DESC;
SELECT city, COUNT(*) as count FROM customers WHERE age > 25 GROUP BY city ORDER BY count DESC;
SELECT age, COUNT(*) as total FROM customers GROUP BY age HAVING total >=4 ORDER BY total DESC;
```

## Having
```SQL
SELECT customerNumber, COUNT(*) as total FROM orders 
GROUP BY customerNumber
HAVING total BETWEEN 3 AND 17 ORDER BY total DESC
```

## Sub Query
```SQL
SELECT * FROM payments WHERE amount > (SELECT AVG(amount) FROM payments) ORDER BY amount DESC  

SELECT * FROM address WHERE city_id IN 
    (SELECT city_id FROM city WHERE country_id IN(1,2,3,4,5));

SELECT * FROM customers WHERE customerNumber NOT IN 
    (SELECT DISTINCT customerNumber FROM payments); 

SELECT MAX(items), MIN(items), FLOOR(AVG(items)) FROM (SELECT 
    customerNumber, COUNT(customerNumber) AS items FROM payments GROUP BY customerNumber) AS lineitems;
```

## Update
```SQL
UPDATE film SET description = " updated description" WHERE film_id = 1;
```
