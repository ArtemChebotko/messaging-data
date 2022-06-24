<div class="top">

# Create tables
### [◂](command:katapod.loadPage?step1){.steps} Step 2 of 7 [▸](command:katapod.loadPage?step3){.steps}
</div>

Create table `folders_by_user`:
```
CREATE TABLE folders_by_user (
  username TEXT,
  label TEXT,
  color TEXT,
  PRIMARY KEY ((username),label)
);
```

Create table `unread_email_stats`:
```
CREATE TABLE unread_email_stats (
  username TEXT,
  label TEXT,
  num_unread COUNTER,
  PRIMARY KEY ((username),label)
);
```

Create table `emails_by_user_folder`:
```
CREATE TABLE emails_by_user_folder (
  username TEXT,
  label TEXT,
  id TIMEUUID,
  "from" TEXT,
  subject TEXT,
  is_read BOOLEAN,
  PRIMARY KEY ((username,label),id)
) WITH CLUSTERING ORDER BY (id DESC);
```

Create table `emails`:
```
CREATE TABLE emails (
  id TIMEUUID,
  "to" LIST<TEXT>,
  "from" TEXT,
  subject TEXT,
  body TEXT,
  attachments MAP<TEXT,INT>,
  PRIMARY KEY ((id))
);
```

Create table `attachments`:
```
CREATE TABLE attachments (
  email_id TIMEUUID,
  filename TEXT,
  chunk_number INT,
  type TEXT,
  value BLOB,
  PRIMARY KEY ((email_id,filename,chunk_number))
);
```

[continue](command:katapod.loadPage?step3){.orange_bar}