* Asian Population ( Easy )

- Given the CITY and COUNTRY tables, query the sum of the populations of all cities where the CONTINENT is 'Asia'.

- Query Answer: 

```
SELECT 
SUM(city.population)
FROM country 
INNER JOIN city 
ON country.code = city.countrycode
WHERE country.continent = "Asia";
```


