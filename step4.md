<div class="top">

# Design queries Q1.1 and Q1.2
### [◂](command:katapod.loadPage?step3){.steps} Step 4 of 7 [▸](command:katapod.loadPage?step5){.steps}
</div>

Find information about all networks; order by name (asc):

<details>
  <summary>Solution</summary>

```
SELECT name, description,
       region, num_sensors
FROM networks
WHERE bucket = 'all';
```

</details>

[continue](command:katapod.loadPage?step5){.orange_bar}