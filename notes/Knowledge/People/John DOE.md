---
First Name: John
Last Name: DOE
Company: "[[Company X]]"
Role: CEO
Hierarchy: 
tags:
  - Type/Person
---

> [!INFO] Readme
> A #Type/Person  can be created as a sort of "contact card" All projects, meetings, notes and daily notes refering to this person will show up here.

> [!success] Projects
> ```dataview
> TABLE rows.file.link as "Project" FROM #Type/Project 
> WHERE contains(file.outlinks, this.file.link)
> GROUP BY Client
> ```

> [!quote] Meetings
> ```dataview
> TABLE rows.file.link as "Meeting" FROM #Type/Meeting
> WHERE contains(file.outlinks, this.file.link)
> SORT  DATE DESC
> GROUP BY Project
> 
> ```

> [!example] Notes
> ```dataview
> TABLE rows.file.link as "Note" FROM #Type/Note/Topic  
> WHERE contains(file.outlinks, this.file.link)
> GROUP BY Project
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


*[[John DOE]] is a fictive person, working at [[Company X]]*