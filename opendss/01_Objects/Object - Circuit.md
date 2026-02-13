---
note_type: opendss_object
object_class: "circuit"
declared_in_files:
  - "Master.dss"
related_objects:
  - "capacitor"
  - "generator"
  - "line"
  - "load"
  - "pvsystem"
  - "storage"
  - "transformer"
related_files:
  - "Master.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/Master.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=Circuit"
status: "draft"
---

# Object - Circuit

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `circuit`
- Declared in: `Master.dss`
- Parsed attrs: `angle`, `basekv`, `bus1`, `frequency`, `mvasc1`, `mvasc3`, `phases`, `pu`
- Description: The top-level OpenDSS model container that defines source, bases, and simulation context.
- Grid role: Defines the feeder boundary and source equivalent, anchoring all downstream device behavior.

## Auto Snippets
```dss
New Circuit.<CIRCUIT_NAME> basekV=<SOURCE_KV_LL> pu=<SOURCE_PU> phases=<NPH>
~ bus1=<SOURCE_BUS> angle=<SOURCE_ANGLE_DEG> frequency=<FREQ_HZ>
~ mvasc3=<MVASC_3PH> mvasc1=<MVASC_1PH>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
The top-level OpenDSS model container that defines source, bases, and simulation context.

## Role in Grid
Defines the feeder boundary and source equivalent, anchoring all downstream device behavior.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `angle` | Source voltage phase angle at the source bus. | degrees | Optional |
| `basekv` | Source nominal line-line voltage for the circuit. | kV | Required |
| `bus1` | Primary terminal bus connection (supports phase suffixes). | bus token | Required |
| `frequency` | Nominal circuit frequency. | Hz | Optional |
| `mvasc1` | Single-phase short-circuit level for source stiffness. | MVA | Optional |
| `mvasc3` | Three-phase short-circuit level for source stiffness. | MVA | Optional |
| `phases` | Phase count for connected element. | integer | Context |
| `pu` | Source voltage magnitude at initialization. | per-unit | Context |

## Skeleton
```dss
New Circuit.<CIRCUIT_NAME> basekV=<SOURCE_KV_LL> pu=<SOURCE_PU> phases=<NPH>
~ bus1=<SOURCE_BUS> angle=<SOURCE_ANGLE_DEG> frequency=<FREQ_HZ>
~ mvasc3=<MVASC_3PH> mvasc1=<MVASC_1PH>
```

## Example
```dss
New Circuit.obj1 basekV=12.47 pu=1 phases=3
~ bus1=BUS1.1.2.3 angle=1 frequency=1
~ mvasc3=1 mvasc1=1
```

## Related
**Related Objects**
- [[Object - Capacitor]]
- [[Object - Generator]]
- [[Object - Line]]
- [[Object - Load]]
- [[Object - PVSystem]]
- [[Object - Storage]]
- [[Object - Transformer]]

**Related Files**
- [[File - Master.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/Master.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Circuit`
<!-- CURATED:END -->

