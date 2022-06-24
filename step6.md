<div class="top">

# Design query Q3
### [◂](command:katapod.loadPage?step5){.steps} Step 6 of 7 [▸](command:katapod.loadPage?step7){.steps}
</div>

Find information about all sensors in network `forest-net`:

<details>
  <summary>Solution</summary>

```
SELECT * 
FROM sensors_by_network
WHERE network = 'forest-net';
```

</details>

[continue](command:katapod.loadPage?step7){.orange_bar}