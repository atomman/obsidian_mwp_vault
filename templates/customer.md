<%* 
 let title = tp.file.title 
 if (title.startsWith("Untitled")) { 
     title = await tp.system.prompt("Title"); 
  } 
  await tp.file.rename(title) 
  await tp.file.move("customers/" + title)
 -%>
 
## Persons
```dataview  
TABLE  titel
from "people"
where contains(customer, this.file.link)
sort file.name desc
```
## cases

```dataview  
TABLE  titel
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

