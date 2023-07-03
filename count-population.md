* Count Populations ( Easy )

- Query a count of the number of cities in CITY having a Population larger than 100000

- Query Answer: 

```
SELECT COUNT(city.population) FROM city 
WHERE city.population > 100000;
```