```tasks
not done
path does not include MyKanBan
```
```dataview
TASK 
FROM "daily"
WHERE !completed and refnr
GROUP BY refnr
```
