# Select
```
SELECT * FROM film 
SELECT film_id, title FROM film
```

# Select DISTINCT
```
SELECT DISTINCT id FROM film
SELECT DISTINCT `length` FROM film ORDER BY `length`
SELECT DISTINCT `length` FROM film ORDER BY `length` DESC
```

# Select Where
```
SELECT * FROM users WHERE name = 'Shvan'
SELECT * FROM users WHERE birthday >= '2000-02-15'
SELECT * FROM users WHERE age BETWEEN 20 AND 25;
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
SELECT * FROM users WHERE name = 'shvan' OR age >= 15
SELECT * FROM film WHERE last_update >= '2006-02-15' and rental_duration >= 5
SELECT * FROM film WHERE (title = 'description' AND id = 1) OR duration >= 7
```

# Select Aggregate Functions
```
SELECT COUNT(id) FROM users;
SELECT MAX(age) FROM users;
SELECT MIN(age) FROM users;
SELECT SUM(age) FROM users;
SELECT UCASE(first_name), LCASE(last_name) FROM users;
```

# Update
```
UPDATE film SET description = " updated description" WHERE film_id = 1;
```
