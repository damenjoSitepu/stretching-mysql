* Weather Observation Station 17 ( Easy )

- Query the Western Longitude (LONG_W)where the smallest Northern Latitude (LAT_N) in STATION is greater than 38.7780. Round your answer to 4 decimal places.

- Query Answer: 

```
SELECT 
ROUND(station.long_w,4)
FROM station
WHERE station.lat_n IN (
    SELECT MIN(station.lat_n) FROM station
    WHERE station.lat_n > 38.7780
);
```


