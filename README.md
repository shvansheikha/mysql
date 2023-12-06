# Select
```
SELECT * FROM users 
SELECT name, age FROM users
SELECT name, `age`, birthday FROM users ORDER BY `name`, age DESC
```

# Select DISTINCT
```
SELECT DISTINCT name FROM users
SELECT DISTINCT `name` FROM users ORDER BY `name`
SELECT DISTINCT `name` FROM users ORDER BY `name` DESC
```

# Select Where
```
SELECT * FROM users WHERE name = 'Shvan'
SELECT * FROM users WHERE birthday >= '2000-02-15'
SELECT * FROM users WHERE dept = value1
SELECT * FROM users WHERE dept <> value1
SELECT * FROM users WHERE dept IS NULL
SELECT * FROM users WHERE dept IS NOT NULL
SELECT * FROM users WHERE dept IS IN (value1, value2)
SELECT * FROM users WHERE dept IS NOT IN (value1, value2)
```

# Select Like
```
SELECT * FROM users WHERE dept LIKE 'd%';
SELECT * FROM users WHERE dept LIKE 'dev%';
SELECT * FROM users WHERE dept LIKE '%t';
SELECT * FROM users WHERE dept LIKE '%e%';
SELECT * FROM users WHERE dept NOT LIKE 'd%';
```

# Select Advance where
```
SELECT * FROM users WHERE age BETWEEN 20 AND 25;
SELECT * FROM users WHERE age = 17 OR points >= 7
SELECT * FROM users WHERE name = 'shvan' OR age >= 15
SELECT * FROM users WHERE birthday >= '2006-02-15' and points >= 5
SELECT * FROM users WHERE (age = 17 AND name = 'shvan') OR points >= 7
```

# Select Aggregate Functions
```sql
SELECT COUNT(id) FROM users;
SELECT MAX(age) FROM users;
SELECT MIN(age) FROM users;
SELECT SUM(age) FROM users;
SELECT UCASE(first_name), LCASE(last_name) FROM users;
```

# Group By
```
SELECT age, COUNT(age) FROM users GROUP BY age;
SELECT age, COUNT(age) FROM users WHERE age > 20 GROUP BY age;
SELECT age, COUNT(age) FROM users GROUP BY age HAVING count(age) >=2;
```

# Update
```
UPDATE film SET description = " updated description" WHERE film_id = 1;
```
