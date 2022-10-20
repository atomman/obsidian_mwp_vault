---
summary::
type::1-2-1, quartely status
---
<%*
   let new_titel = tp.file.creation_date("YYYY-MM-DD_HHmm"+"qrtReview")
    tp.file.rename(new_titel)
   await tp.file.move("daily/" + tp.date.now("YYYY") +  "/" + tp.date.now("MM") + "/" + new_titel)
%>

### Other reviews
```dataview
TABLE summary
FROM -"templates"
WHERE contains(type, "quartely status") AND (file.name != this.file.name)
```

## Quartely Focus

- tops
	- 
- flops
	- 

### What activities should I prioritize

#### First priority

### Competencies I want to develope

## Past quarter

## Collaborators

### Latest cases
```dataview  
TABLE  title, customer, summary, dateformat(file.mtime, "dd.MM.yyyy - HH:mm") AS "Last modified"
from "cases"
WHERE (file.mtime) >= (this.file.ctime - dur(90 d))
SORT file.mtime DESC
```


## latest traning seminars
```dataview  
TABLE  summary, dateformat(file.mtime, "dd.MM.yyyy - HH:mm") AS "Last modified"
from ""
WHERE contains(type, "learning")
SORT file.mtime DESC
```
## latest labbook
```dataview  
TABLE summary, dateformat(file.mtime, "MM.dd.yyyy - HH:mm") AS "Last modified"
from "daily"
WHERE contains(type, "labbook") AND (file.mtime) >= (this.file.ctime - dur(90 d))
SORT file.mtime DESC
```
