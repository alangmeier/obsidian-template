<%*  
const clientNames = [... new Set(app.vault.getMarkdownFiles().map(f => f.path).filter(path => path.startsWith("Knowledge/Companies")).map(path => path.split("/")[2].split(".")[0]))];
const clientName = (await tp.system.suggester((item) => item, clientNames, true, "Select Company Name")); 
const firstName = await tp.system.prompt("First Name", ""); 
const lastName = await tp.system.prompt("Last Name", ""); 
const fileName = firstName + " " + lastName.toUpperCase()
%>---
First Name: <% firstName %>
Last Name: <% lastName %>
Company: '[[<% clientName %>]]'
Role: 
Hierarchy:
tags:
  - Type/Person
---

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


<% await tp.file.move("/Knowledge/People/" + fileName) %>