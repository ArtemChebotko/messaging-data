<div class="top">

# Design query Q4
### [◂](command:katapod.loadPage?step6){.steps} Step 7 of 7 [▸](command:katapod.loadPage?finish){.steps}
</div>

Find an attachment file with name `Budget.xlsx` for an email with id `8ae31dd0-d361-11ea-a40e-5dd6331dfc45`, assuming that the complete file is stored in one partition with chunk number `1`:

<details>
  <summary>Solution</summary>

```
SELECT filename, type, value,
       blobAsText(value)
FROM attachments
WHERE email_id = 8ae31dd0-d361-11ea-a40e-5dd6331dfc45
  AND filename = 'Budget.xlsx'
  AND chunk_number = 1;
```

</details>

<br/>

Find an attachment file with name `Presentation.pptx` for an email with id `8ae31dd0-d361-11ea-a40e-5dd6331dfc45`, assuming that the three file chunks are stored across three partitions with chunk numbers `1`, `2` and `3`:

<details>
  <summary>Solution</summary>

```
SELECT filename, type, value,
       blobAsText(value)
FROM attachments
WHERE email_id = 8ae31dd0-d361-11ea-a40e-5dd6331dfc45
  AND filename = 'Presentation.pptx'
  AND chunk_number IN (1,2,3);
```

</details>

[continue](command:katapod.loadPage?finish){.orange_bar}
