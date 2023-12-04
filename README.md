# Select
```
SELECT * FROM film 
SELECT film_id, title FROM film
```

# Select DISTINCT
```
SELECT DISTINCT id FROM film
SELECT DISTINCT `length` FROM film ORDER BY `length` DESC
SELECT DISTINCT `length` FROM film ORDER BY `length`
```

# Select Where
```
SELECT * FROM film WHERE title = 'ACE GOLDFINGER'
SELECT * FROM film WHERE last_update >= '2006-02-15'
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
SELECT * FROM film WHERE last_update >= '2006-02-15' and rental_duration >= 5
SELECT * FROM film WHERE title = 'description' OR duration >= 5
SELECT * FROM film WHERE (title = 'description' AND id = 1) OR duration >= 7
```

# Update
```
UPDATE film SET description = " updated description" WHERE film_id = 1;
```
