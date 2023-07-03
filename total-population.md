* Total Populations ( Easy )

- Query the total population of all cities in CITY where District is California

- Query Answer: 

```
SELECT SUM(city.population) FROM city
WHERE city.district = "california";
```