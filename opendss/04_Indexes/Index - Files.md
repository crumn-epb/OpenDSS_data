---
note_type: opendss_index
index_scope: "files"
status: "draft"
---

# Index - Files

```dataview
TABLE source_path, include_stage, included_by_master, status
FROM "obsidian/opendss/02_Files"
WHERE note_type = "opendss_file"
SORT source_path ASC
```
