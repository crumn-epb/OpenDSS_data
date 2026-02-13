---
note_type: opendss_object
object_class: "tshape"
declared_in_files:
  - "TShape.dss"
related_objects:
  - "priceshape"
  - "storage"
related_files:
  - "TShape.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/TShape.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=TShape"
status: "draft"
---

# Object - TShape

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `tshape`
- Declared in: `TShape.dss`
- Parsed attrs: `file`, `interval`, `npts`, `temp`
- Description: A temperature time-series profile used by temperature-sensitive models and controls.
- Grid role: Represents ambient/asset temperature evolution impacting temperature-dependent behavior.

## Auto Snippets
```dss
New TShape.<TSHAPE_NAME> npts=<NPTS> interval=<HOURS>
~ temp=(file=<TEMP_CSV_PATH>)
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A temperature time-series profile used by temperature-sensitive models and controls.

## Role in Grid
Represents ambient/asset temperature evolution impacting temperature-dependent behavior.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `file` | External file path for profile/curve values. | path | Context |
| `interval` | Time step between profile points. | hours (or class-specific) | Context |
| `npts` | Number of points in profile/curve. | integer | Required |
| `temp` | Temperature profile or scalar assignment. | TShape name or scalar | Optional |

## Skeleton
```dss
New TShape.<TSHAPE_NAME> npts=<NPTS> interval=<HOURS>
~ temp=(file=<TEMP_CSV_PATH>)
```

## Example
```dss
New TShape.obj1 npts=24 interval=1
~ temp=(file=./shape.csv)
```

## Related
**Related Objects**
- [[Object - PriceShape]]
- [[Object - Storage]]

**Related Files**
- [[File - TShape.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/TShape.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `TShape`
<!-- CURATED:END -->

