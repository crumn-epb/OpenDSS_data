---
note_type: opendss_object
object_class: "wiredata"
declared_in_files:
  - "Master.dss"
  - "WireData.dss"
related_objects:
  - "line"
  - "linegeometry"
related_files:
  - "Master.dss"
  - "WireData.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/Master.dss"
  - "data/OpenDSS/templates/WireData.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=WireData"
status: "draft"
---

# Object - WireData

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `wiredata`
- Declared in: `Master.dss`, `WireData.dss`
- Parsed attrs: `diam`, `emergamps`, `gmrac`, `normamps`, `rac`, `units`
- Description: Conductor electrical/geometric data for overhead wire modeling.
- Grid role: Defines conductor constants needed to compute realistic overhead line characteristics.

## Auto Snippets
```dss
New WireData.<WIRE_NAME> rac=<RAC> gmrac=<GMR> diam=<DIAM>
~ normamps=<NORM_AMPS> emergamps=<EMERG_AMPS> units=<UNITS>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
Conductor electrical/geometric data for overhead wire modeling.

## Role in Grid
Defines conductor constants needed to compute realistic overhead line characteristics.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `diam` | Conductor outer diameter. | length | Context |
| `emergamps` | Emergency current rating. | A | Optional |
| `gmrac` | Geometric mean radius at AC conditions. | length | Context |
| `normamps` | Normal continuous current rating. | A | Optional |
| `rac` | AC resistance at base frequency. | ohm per length | Context |
| `units` | Engineering units associated with this object. | enum | Context |

## Skeleton
```dss
New WireData.<WIRE_NAME> rac=<RAC> gmrac=<GMR> diam=<DIAM>
~ normamps=<NORM_AMPS> emergamps=<EMERG_AMPS> units=<UNITS>
```

## Example
```dss
New WireData.obj1 rac=1 gmrac=1 diam=1
~ normamps=1 emergamps=1 units=kft
```

## Related
**Related Objects**
- [[Object - Line]]
- [[Object - LineGeometry]]

**Related Files**
- [[File - Master.dss]]
- [[File - WireData.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/Master.dss`
- `data/OpenDSS/templates/WireData.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `WireData`
<!-- CURATED:END -->

