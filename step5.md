<div class="top">

# Design query Q2
### [◂](command:katapod.loadPage?step4){.steps} Step 5 of 7 [▸](command:katapod.loadPage?step6){.steps}
</div>

Find ids, subjects, senders, read/unread statuses and timestamps of all emails with label `inbox` for user `joe@datastax.com`; order by timestamp (desc):

<details>
  <summary>Solution</summary>

```
SELECT id, subject, "from", is_read, 
       toTimestamp(id) AS timestamp
FROM emails_by_user_folder
WHERE label = 'inbox' 
  AND username = 'joe@datastax.com'; 
```

</details>

[continue](command:katapod.loadPage?step6){.orange_bar}