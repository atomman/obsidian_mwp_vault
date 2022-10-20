## Persons
```dataview  
TABLE  title
from "people"
where contains(customer, this.file.link)
sort file.name desc
```
## cases

```dataview  
TABLE  summary
from "cases"
where contains(customer, this.file.link)
sort file.name desc
```

## Everything else
```dataview  
TABLE  titel, refnr
from -"cases" AND -"people" AND [[]]
sort file.name desc
```

