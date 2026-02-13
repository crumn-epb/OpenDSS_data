---
note_type: opendss_index
index_scope: "objects"
status: "draft"
---

# Index - Objects

```dataview
TABLE object_class, length(declared_in_files) AS file_count, status
FROM "obsidian/opendss/01_Objects"
WHERE note_type = "opendss_object"
SORT object_class ASC
```
