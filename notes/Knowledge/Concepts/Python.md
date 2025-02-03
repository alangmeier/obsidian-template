---
Provider: 
tags: Type/Concept
aliases: 
Related:
---

> [!INFO] Readme
> A #Type/Concept  can be created to document a technology or concept.
> 
> The concept page will automatically show other types of pages referring it


# Projects
```dataview
LIST FROM #Type/Project 
WHERE contains(file.outlinks, this.file.link)
```
# Notes
```dataview
TABLE Project FROM #Type/Note/Topic
WHERE contains(file.outlinks, this.file.link)
SORT Date DESC
```
# Meetings
```dataview
TABLE Project FROM #Type/Meeting
WHERE contains(file.outlinks, this.file.link)
SORT Date DESC
```
# Documentation

*[[Python]] is a concept.*

# References

*See [python.org](https://python.org)*
