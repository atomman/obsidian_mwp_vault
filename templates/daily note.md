<%*
   let new_titel = tp.file.creation_date("YYYY-MM-DD")
    tp.file.rename(new_titel)
   await tp.file.move("daily/" + tp.date.now("YYYY") +  "/" + tp.date.now("MM") + "/" + new_titel)
%>
summary::
## Quick Captures

## Notes from today
```dataview
TABLE summary, refnr
FROM "daily"
WHERE file.day = date({{date:YYYY-MM-DD}}) and file.name != "{{date:YYYY-MM-DD}}"
```
