---
note_type: opendss_object
object_class: "loadshape"
declared_in_files:
  - "LoadShape.dss"
  - "Master.dss"
related_objects:
  - "generator"
  - "load"
  - "pvsystem"
  - "storage"
related_files:
  - "LoadShape.dss"
  - "Master.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/LoadShape.dss"
  - "data/OpenDSS/templates/Master.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=LoadShape"
status: "draft"
---

# Object - LoadShape

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `loadshape`
- Declared in: `LoadShape.dss`, `Master.dss`
- Parsed attrs: `file`, `interval`, `mult`, `npts`, `qmult`
- Description: A time-series multiplier profile used by loads/DER for sequential simulations.
- Grid role: Drives temporal variation in consumption/generation for daily/yearly/duty simulations.

## Auto Snippets
```dss
New LoadShape.<LS_NAME> npts=<NPTS> interval=<HOURS>
~ mult=(file=<P_MULT_CSV_PATH>) qmult=(file=<Q_MULT_CSV_PATH>)
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A time-series multiplier profile used by loads/DER for sequential simulations.

## Role in Grid
Drives temporal variation in consumption/generation for daily/yearly/duty simulations.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `file` | External file path for profile/curve values. | path | Context |
| `interval` | Time step between profile points. | hours (or class-specific) | Context |
| `mult` | Multiplier vector for profile/shape values. | array | Context |
| `npts` | Number of points in profile/curve. | integer | Required |
| `qmult` | Reactive multiplier vector for profile/shape. | array | Optional |

## Skeleton
```dss
New LoadShape.<LS_NAME> npts=<NPTS> interval=<HOURS>
~ mult=(file=<P_MULT_CSV_PATH>) qmult=(file=<Q_MULT_CSV_PATH>)
```

## Example
```dss
New LoadShape.obj1 npts=24 interval=1
~ mult=(file=./shape.csv) qmult=(file=./shape.csv)
```

## Related
**Related Objects**
- [[Object - Generator]]
- [[Object - Load]]
- [[Object - PVSystem]]
- [[Object - Storage]]

**Related Files**
- [[File - LoadShape.dss]]
- [[File - Master.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/LoadShape.dss`
- `data/OpenDSS/templates/Master.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `LoadShape`
<!-- CURATED:END -->

