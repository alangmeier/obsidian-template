---
Name: "[[Important Topic]]"
Project: "[[Company X - Internal Activities]]"
Started: false
Completed: false
Description: 
tags:
  - Type/Topic
---

> [!INFO] Readme
> A #Type/Topic  can be created to further divide a project in multiple topics. These topics can be referred to from the meetings and notes


> [!quote] Meetings
> ```dataview
> TABLE Participants FROM #Type/Meeting
> WHERE  contains(file.outlinks, this.file.link)
> SORT Date Desc
> ```

> [!NOTE] Notes
> ```dataview
> TABLE Date FROM #Type/Note/Topic 
> WHERE  contains(file.outlinks, this.file.link)
> Sort Date DESC
> ```
> 

------------------------------


