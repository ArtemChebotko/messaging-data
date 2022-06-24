<div class="top">

# Populate tables
### [◂](command:katapod.loadPage?step2){.steps} Step 3 of 7 [▸](command:katapod.loadPage?step4){.steps}
</div>

Execute the CQL script to insert sample data:
```
SOURCE 'assets/messaging_data.cql'
```

Retrieve all rows from table `folders_by_user`:
```
SELECT * FROM folders_by_user;        
```

Retrieve all rows from table `unread_email_stats`:
```
SELECT * FROM unread_email_stats;
```

Retrieve all rows from table `emails_by_user_folder`:
```
SELECT * FROM emails_by_user_folder;                    
```

Retrieve all rows from table `emails`:
```
SELECT id, "to", "from" FROM emails; 
SELECT id, subject, body FROM emails; 
SELECT id, attachments FROM emails;
```

Retrieve all rows from table `attachments`:
```
SELECT * FROM attachments;       
```

[continue](command:katapod.loadPage?step4){.orange_bar}