* Weather Observation Station 13 ( Easy )

- Query the sum of Northern Latitudes (LAT_N) from STATION having values greater than n and less than n. Truncate your answer to 4 decimal places.

- Query Answer: 

```
SELECT 
TRUNCATE(SUM(station.lat_n),4)
FROM station
WHERE station.lat_n > 38.7880 AND station.lat_n < 137.2345
```


