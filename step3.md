<div class="top">

# Populate tables
### [◂](command:katapod.loadPage?step2){.steps} Step 3 of 7 [▸](command:katapod.loadPage?step4){.steps}
</div>

Execute the CQL script to insert sample data:
```
SOURCE 'assets/sensor_data.cql'
```

Retrieve all rows from table `networks`:
```
SELECT * FROM networks;        
```

Retrieve all rows from table `temperatures_by_network`:
```
SELECT network, week, date_hour, 
       sensor, avg_temperature 
FROM temperatures_by_network;
```

Retrieve all rows from table `sensors_by_network`:
```
SELECT * FROM sensors_by_network;                    
```

Retrieve all rows from table `temperatures_by_sensor`:
```
SELECT * FROM temperatures_by_sensor; 
```

[continue](command:katapod.loadPage?step4){.orange_bar}