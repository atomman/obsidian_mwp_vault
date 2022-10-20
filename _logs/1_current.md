# current cases
```dataview  
TABLE  title, customer, summary, status
from "cases"
where contains(status, "🟩")
sort file.name desc
```


## Finnished cases
```dataview  
TABLE  title, customer, summary, status
from "cases"
where contains(status, "✔")
sort file.name desc
```


# Case notes
```dataview  
LIST rows.file.link
from "daily"
where contains(type, "labbook")
GROUP BY refnr
```

