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

> [!summary] Summary of notes
> ```dataview  
TABLE type, summary
from "daily"
where contains(refnr, this.file.link)
sort file.name desc


>[!todo]
>```dataview
TASK
FROM "daily"
WHERE contains(refnr, this.file.link)
