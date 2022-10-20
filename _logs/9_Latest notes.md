## latest daily notes
```dataview  
table summary

from ""

where date(split(file.name, "_")[0]) > (date(now) - dur(28 days))

sort file.name desc
```

## latest edited notes
```dataview 
TABLE summary, dateformat(file.mtime, "dd.MM.yyyy - HH:mm") AS "Last modified" 
FROM -"_Logs" 
WHERE file.mtime> (date(now) - dur(4 days))
SORT file.mtime DESC LIMIT 25
```
