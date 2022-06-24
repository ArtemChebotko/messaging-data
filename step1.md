<div class="top">

# Create a keyspace
### [◂](command:katapod.loadPage?intro){.steps} Step 1 of 7 [▸](command:katapod.loadPage?step2){.steps}
</div>

Start the CQL shell:
```
cqlsh
```

Create the `messaging_data` keyspace:
```
CREATE KEYSPACE messaging_data
WITH replication = {
  'class': 'NetworkTopologyStrategy', 
  'DC-Houston': 1 };
```

Set the current working keyspace:
```
USE messaging_data;
```

[continue](command:katapod.loadPage?step2){.orange_bar}