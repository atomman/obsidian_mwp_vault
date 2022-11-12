---
case_url: 
---
 
 
title::
summary::sell candy to [[Jane Doe]]
customer::[[AwsomeInc]]
lead::
stakeholder::[[Jane Doe]]
status:: 🟩


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
