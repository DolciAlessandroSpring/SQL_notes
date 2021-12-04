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
