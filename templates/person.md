<%* 
 let title = tp.file.title 
 if (title.startsWith("Untitled")) { 
     title = await tp.system.prompt("Title"); 
  } 
  await tp.file.rename(title) 
  await tp.file.move("people/" + title)
 -%>
customer:: [[]]
title::
contact::

## Stakeholder in

```dataview
TABLE refnr, summary
FROM [[]]
```
