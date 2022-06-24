<div class="top">

# Design query Q4
### [◂](command:katapod.loadPage?step6){.steps} Step 7 of 7 [▸](command:katapod.loadPage?finish){.steps}
</div>

Find raw measurements for sensor `s1003` on `2020-07-06`; order by timestamp (desc):

<details>
  <summary>Solution</summary>

```
SELECT timestamp, value 
FROM temperatures_by_sensor
WHERE sensor = 's1003'
  AND date   = '2020-07-06';
```

</details>

[continue](command:katapod.loadPage?finish){.orange_bar}
