---
tags:
  - Type/Company
---
# Projects
```dataview
TABLE Summary
FROM #Type/Project
WHERE Client = this.file.link

```

# People
```dataview
TABLE Role
FROM #Type/Person
WHERE Company = this.file.link
```


<% await tp.file.move("/Knowledge/Companies/" + tp.file.title) %>