---
Client: "[[Company X]]"
Active: true
Team:
  - "[[John DOE]]"
Manager:
  - "[[John DOE]]"
Technologies:
  - "[[Python]]"
Summary: This is an internal project
tags:
  - Type/Project
---
# Admin

## Imputation

| Number | Description |
| ---- | ---- |
| **X** | Y |
# Description

[[Company X - Internal Activities]] is a project at [[Company X]]
# Topic

> [!task] Topics
> ```dataview
> Table Description, Started, Completed  FROM #Type/Topic 
> WHERE Project = this.file.link
> SORT Date Desc
> ```

# History

> [!quote] Meetings
> ```dataview
> TABLE Participants, Topics FROM #Type/Meeting
> WHERE Project = this.file.link
> SORT Date Desc
> ```

> [!NOTE] Notes
> ```dataview
> TABLE Date, Topics FROM #Type/Note/Topic 
> WHERE Project = this.file.link and !Archived
> Sort Date DESC
> ```
> 

> [!example] Open Tasks
> ```dataview
> TASK
> WHERE Project = this.file.link
> AND (status = " " OR status = "/")
> SORT file.Date DESC
> GROUP BY file.link 
> ```

> [!summary] Daily Activities and News
> ```dataview
> Table  rows.L.text as Notes
> from "Agenda"
> flatten file.lists as L
> where (contains(this.file.inlinks, file.link) and
> contains(L.text, this.file.name)) or contains(meta(L.section).subpath, this.file.name)
> group by file.link as Date
> sort Date desc
> ```
> 




