---
case_url: 
---
<%* 
 let title = tp.file.title 
 if (title.startsWith("Untitled")) { 
     title = await tp.system.prompt("Title"); 
  } 
  await tp.file.rename(title) 
  await tp.file.move("cases/" + title)
 -%> 
 
title::
summary::
customer::
lead::
stakeholder::
status:: 
## case notes

```dataview  
TABLE summary
from "daily"
where contains(refnr, this.file.link)
sort file.name desc
```
## TODOs

```dataview
TASK
FROM "daily"
WHERE contains(refnr, this.file.link)
```
