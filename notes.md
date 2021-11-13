## SELECT 
```
SELECT title
FROM films;
```
This not only works with columns, but also with basic math
```
SELECT (10 / 3);
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

<br/>

## AGGREGATION
You can use `AVG`, `MAX`, `MIN`, `SUM`.
```
SELECT AVG(budget)
FROM films;
```
You can obviously add a `WHERE` after this.
```
SELECT SUM(budget)
FROM films
WHERE release_year >= 2010;
```

<br/>

## AS
Use it for renaming.
```
SELECT MAX(budget) AS max_budget,
       MAX(duration) AS max_duration
FROM films;
```

<br/>

## ORDER BY
