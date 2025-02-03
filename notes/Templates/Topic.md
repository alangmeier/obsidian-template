<%*  
const projectNames = [... new Set(app.vault.getMarkdownFiles().map(f => f.path).filter(path => path.startsWith("Projects")).map(path => path.split("/")[1].split(".")[0]))];
const projectName = (await tp.system.suggester((item) => item, projectNames, true, "Select Project Name")); 
const fileTitle = await tp.system.prompt("Task Name", ""); 
const fileName = fileTitle
%>---
Name: '[[<% fileTitle %>]]'
Project: '[[<% projectName %>]]'
Started: false
Completed: false
Description: 
tags:
  - Type/Topic
---

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


<% await tp.file.move("/Projects/" + projectName + "/Topics/" + fileName) %>