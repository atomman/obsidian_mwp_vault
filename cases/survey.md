---
case_url: 
---
title::My First case
summary::A test case for the mwp obsidian vault
customer::[[AwsomeInc]]
lead::
stakeholder::[[John Doe]]
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
