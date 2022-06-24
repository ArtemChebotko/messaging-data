<div class="top">

# Design queries Q1.1 and Q1.2
### [◂](command:katapod.loadPage?step3){.steps} Step 4 of 7 [▸](command:katapod.loadPage?step5){.steps}
</div>

Find all folder labels and colors for user `joe@datastax.com`:

<details>
  <summary>Solution</summary>

```
SELECT label, color 
FROM folders_by_user
WHERE username = 'joe@datastax.com';   
```

</details>

<br/>

Find all folder labels and unread email quantities for user `joe@datastax.com`:

<details>
  <summary>Solution</summary>

```
SELECT label, num_unread 
FROM unread_email_stats
WHERE username = 'joe@datastax.com'; 
```

</details>

[continue](command:katapod.loadPage?step5){.orange_bar}