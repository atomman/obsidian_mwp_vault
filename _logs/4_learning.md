```dataview  
TABLE titel, kunde, summary
from "daily"
where contains(type, "training")
sort file.cday desc
```
