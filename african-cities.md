* African Cities ( Easy )

- Given the CITY and COUNTRY tables, query the names of all cities where the CONTINENT is 'Africa'.

- Query Answer: 

```
SELECT 
city.name
FROM country
INNER JOIN city 
ON country.code = city.countrycode
WHERE country.continent = "Africa";
```


