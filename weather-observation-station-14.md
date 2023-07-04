* Weather Observation Station 14 ( Easy )

- Query the greatest value of the Northern Latitudes (LAT_N) from STATION that is less than 137.2345. Truncate your answer to  decimal places.

- Query Answer: 

```
SELECT
TRUNCATE(MAX(station.lat_n),4)
FROM station
WHERE station.lat_n < 137.2345;
```