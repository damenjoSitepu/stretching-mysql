* Weather Observation Station 16 ( Easy )

- Query the smallest Northern Latitude (LAT_N) from STATION that is greater than 33.7780. Round your answer to 4 decimal places.

- Query Answer: 

```
SELECT 
ROUND(MIN(station.lat_n),4)
FROM station
WHERE station.lat_n > 38.7780;
```