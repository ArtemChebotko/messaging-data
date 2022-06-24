<div class="top">

# Design query Q2
### [◂](command:katapod.loadPage?step4){.steps} Step 5 of 7 [▸](command:katapod.loadPage?step6){.steps}
</div>

Find hourly average temperatures for every sensor in network `forest-net` and date range [`2020-07-05`,`2020-07-06`] within the week of `2020-07-05`; order by date (desc) and hour (desc):

<details>
  <summary>Solution</summary>

```
SELECT date_hour, avg_temperature, 
       latitude, longitude, sensor 
FROM temperatures_by_network
WHERE network    = 'forest-net'
  AND week       = '2020-07-05'
  AND date_hour >= '2020-07-05'
  AND date_hour  < '2020-07-07';
```

</details>

<br/>

Find hourly average temperatures for every sensor in network `forest-net` and date range [`2020-07-04`,`2020-07-06`] within the weeks of `2020-06-28` and `2020-07-05`; order by date (desc) and hour (desc):

<details>
  <summary>Solution 1</summary>

```
SELECT date_hour, avg_temperature, 
       latitude, longitude, sensor 
FROM temperatures_by_network
WHERE network    = 'forest-net'
  AND week       = '2020-07-05'
  AND date_hour >= '2020-07-04'
  AND date_hour  < '2020-07-07';
  
SELECT date_hour, avg_temperature, 
       latitude, longitude, sensor 
FROM temperatures_by_network
WHERE network    = 'forest-net'
  AND week       = '2020-06-28'
  AND date_hour >= '2020-07-04'
  AND date_hour  < '2020-07-07';  
```

</details>

<details>
  <summary>Solution 2</summary>

```
SELECT date_hour, avg_temperature, 
       latitude, longitude, sensor 
FROM temperatures_by_network
WHERE network    = 'forest-net'
  AND week      IN ('2020-07-05','2020-06-28')
  AND date_hour >= '2020-07-04'
  AND date_hour  < '2020-07-07';  
```

</details>

[continue](command:katapod.loadPage?step6){.orange_bar}