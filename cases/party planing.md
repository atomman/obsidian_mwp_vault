---
case_url: 
---
 
 
title::
summary::sell candy to [[Jane Doe]]
customer::[[AwsomeInc]]
lead::
stakeholder::[[Jane Doe]]
status:: 🟩
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
