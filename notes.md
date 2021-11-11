## SELECT 
```
SELECT title
FROM films;
```
<br/>

## DISTINCT
```
SELECT DISTINCT country
FROM films;
```

<br/>

## COUNT
```
SELECT COUNT(country)
FROM films;
```
```
SELECT COUNT(DISTINCT country)
FROM films;
```
[*you can use SELECT COUNT(\*) to count rows*]


<br/>

## WHERE
You can use `=`, `<>`, `<`, `>`, `<=`, `>=`, `AND`, `OR`, `BETWEEN` (inclusive), `IN` (define a list with parenthesis), `IS NULL`, `IS NOT NULL`, `LIKE`, `NOT LIKE`. \
Comes always after a `FROM`.
```
SELECT *
FROM films
WHERE title = 'Metropolis';
```
```
SELECT name
FROM kids
WHERE age IN (2, 4, 6, 8, 10);
```