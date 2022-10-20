# customer meetings
```dataview  
TABLE title, customer, summary
from "daily"
where contains(type, "customer meeting")
sort file.cday desc
```

# 1-2-1 meetings

```dataview  
TABLE summary
from "daily"
where contains(type, "1-2-1")
sort file.name desc
```


## All meetings
```dataview  
TABLE title, type, summary
from "daily"
where regexmatch(".+meeting", type)
sort file.cday desc
```
