---
tags:
  - Type/Company
---

> [!INFO] Readme
> A #Type/Company can be created to group people or projects together. This page will automatically show all projects and people related to the company

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


*This is an example `Company`, named [[Company X]]*