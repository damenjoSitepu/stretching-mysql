* Weather Observation Station 15 ( Easy )

- Query the Western Longitude (LONG_W) for the largest Northern Latitude (LAT_N) in STATION that is less than 137.2345. Round your answer to 4 decimal places.

- Query Answer: 

```
SELECT
ROUND(station.long_w,4)
FROM station
WHERE station.lat_n = (SELECT MAX(station.lat_n) FROM station WHERE station.lat_n < 137.2345);
```