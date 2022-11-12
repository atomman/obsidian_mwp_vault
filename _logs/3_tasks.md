## By Case
```dataview
TASK
FROM -#TaskExclude
WHERE !completed and refnr
GROUP BY refnr
```
## misc todos
```dataview
TASK
FROM -#TaskExclude
WHERE !completed and !refnr
GROUP BY file.name
```
