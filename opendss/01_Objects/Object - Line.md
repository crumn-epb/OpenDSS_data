---
note_type: opendss_object
object_class: "line"
declared_in_files:
  - "Lines.dss"
  - "Master.dss"
  - "Switches.dss"
related_objects:
  - "cndata"
  - "linecode"
  - "linegeometry"
  - "tsdata"
  - "wiredata"
related_files:
  - "Lines.dss"
  - "Master.dss"
  - "Switches.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/Lines.dss"
  - "data/OpenDSS/templates/Master.dss"
  - "data/OpenDSS/templates/Switches.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=Line"
status: "draft"
---

# Object - Line

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `line`
- Declared in: `Lines.dss`, `Master.dss`, `Switches.dss`
- Parsed attrs: `bus1`, `bus2`, `emergamps`, `enabled`, `geometry`, `length`, `linecode`, `normamps`, `phases`, `r0`, `r1`, `switch`, `units`, `x0`, `x1`
- Description: A branch element connecting two buses, representing overhead/underground segments or switch lines.
- Grid role: Carries power between network nodes and defines feeder topology and electrical paths.

## Auto Snippets
```dss
New Line.<LINE_NAME> bus1=<FROM_BUS> bus2=<TO_BUS> phases=<NPH>
~ length=<LEN> units=<UNITS> linecode=<LC_NAME>
~ normamps=<NORM_AMPS> emergamps=<EMERG_AMPS> enabled=<True>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A branch element connecting two buses, representing overhead/underground segments or switch lines.

## Role in Grid
Carries power between network nodes and defines feeder topology and electrical paths.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `bus1` | Primary terminal bus connection (supports phase suffixes). | bus token | Required |
| `bus2` | Secondary terminal bus connection (supports phase suffixes). | bus token | Required |
| `emergamps` | Emergency current rating. | A | Optional |
| `enabled` | Initial line availability in the solved topology. | True/False | Optional |
| `geometry` | LineGeometry used for geometry-based line modeling. | LineGeometry reference | Context |
| `length` | Branch physical/electrical length. | length | Required |
| `linecode` | LineCode used for electrical parameter lookup. | LineCode reference | Context |
| `normamps` | Normal continuous current rating. | A | Optional |
| `phases` | Phase count for connected element. | integer | Context |
| `r0` | Zero-sequence resistance per unit length. | ohm per length | Context |
| `r1` | Positive-sequence resistance per unit length. | ohm per length | Context |
| `switch` | Marks this line object as a switch-like branch for topology operations. | Yes/No | Optional |
| `units` | Engineering units associated with this object. | enum | Context |
| `x0` | Zero-sequence reactance per unit length. | ohm per length | Context |
| `x1` | Positive-sequence reactance per unit length. | ohm per length | Context |

## Skeleton
```dss
New Line.<LINE_NAME> bus1=<FROM_BUS> bus2=<TO_BUS> phases=<NPH>
~ length=<LEN> units=<UNITS> linecode=<LC_NAME>
~ normamps=<NORM_AMPS> emergamps=<EMERG_AMPS> enabled=<True>
```

## Example
```dss
New Line.obj1 bus1=BUS1.1.2.3 bus2=BUS1.1.2.3 phases=3
~ length=1.0 units=kft linecode=obj1
~ normamps=1 emergamps=1 enabled=1
```

## Related
**Related Objects**
- [[Object - CNData]]
- [[Object - LineCode]]
- [[Object - LineGeometry]]
- [[Object - TSData]]
- [[Object - WireData]]

**Related Files**
- [[File - Lines.dss]]
- [[File - Master.dss]]
- [[File - Switches.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/Lines.dss`
- `data/OpenDSS/templates/Master.dss`
- `data/OpenDSS/templates/Switches.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Line`
<!-- CURATED:END -->

