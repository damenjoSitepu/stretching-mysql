* Weather Observation Station 2 ( Easy )

- Query the following two values from the STATION table:

- The sum of all values in LAT_N rounded to a scale of  decimal places.
- The sum of all values in LONG_W rounded to a scale of  decimal places.

- Query Answer: 

```
SELECT 
ROUND(SUM(station.lat_n),2), 
ROUND(SUM(station.long_w),2)
FROM station;
```