## INNER

Start with the most simple example.
```
SELECT *
FROM cities
  INNER JOIN countries
    ON cities.country_code = countries.code;
```

<br>

One can use the name of the tables already in the select.
```
SELECT c.code, c.name, c.region, p.year, p.fertility_rate
  FROM countries AS c
  INNER JOIN populations AS p
    ON c.code = p.country_code
```
One can simply add N different joins one after another.

<br>

You can join on multiple columns, concatenating the logic
```
[ ... ]
ON A.col1 = B.col1 AND A.col2 = B.col2
```

<br>

## USING
There's a different way of writing the condition if the tables have the same name. Note the brackets.
```
SELECT c.name AS country, l.name AS languages
FROM countries AS c
INNER JOIN languages AS l
USING (code)
```

<br>

## SELF JOIN
```
SELECT p1.country_code,
       p1.size AS size2010,
       p2.size AS size2015
FROM populations as p1
  INNER JOIN populations as p2
    ON p1.country_code = p2.country_code
```
