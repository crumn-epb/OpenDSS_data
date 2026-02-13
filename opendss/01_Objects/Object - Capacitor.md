---
note_type: opendss_object
object_class: capacitor
declared_in_files:
  - Capacitors.dss
  - Master.dss
related_objects:
  - capcontrol
related_files:
  - Capacitors.dss
  - Master.dss
related_commands:
  - New
source_refs:
  - data/OpenDSS/templates/Capacitors.dss
  - data/OpenDSS/templates/Master.dss
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=Capacitor"
status: draft
---

# Object - Capacitor

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `capacitor`
- Declared in: `Capacitors.dss`, `Master.dss`
- Parsed attrs: `bus1`, `conn`, `enabled`, `kv`, `kvar`, `numsteps`, `phases`
- Description: A switched or fixed shunt reactive-power device connected to a bus.
- Grid role: Provides local reactive support to improve voltage profile and reduce feeder reactive flow.

## Auto Snippets
```dss
New Capacitor.<CAP_NAME> bus1=<BUS> phases=<NPH> conn=<wye|delta>
~ kv=<KV> kvar=<KVAR> numsteps=<NSTEPS> enabled=<True>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A switched or fixed shunt reactive-power device connected to a bus.

## Role in Grid
Provides local reactive support to improve voltage profile and reduce feeder reactive flow.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `bus1` | Primary terminal bus connection (supports phase suffixes). | bus token | Required |
| `conn` | Connection type for element terminals. | wye|delta | Context |
| `enabled` | Enable/disable this element. | True/False | Optional |
| `kv` | Nominal voltage level for element connection. | kV | Context |
| `kvar` | Reactive power value or rating. | kvar | Context |
| `numsteps` | Number of discrete capacitor steps. | integer | Optional |
| `phases` | Phase count for connected element. | integer | Context |

## Skeleton
```dss
New Capacitor.<CAP_NAME> bus1=<BUS> phases=<NPH> conn=<wye|delta>
~ kv=<KV> kvar=<KVAR> numsteps=<NSTEPS> enabled=<True>
```

## Example
```dss
New Capacitor.obj1 bus1=BUS1.1.2.3 phases=3 conn=wye
~ kv=12.47 kvar=12.47 numsteps=1 enabled=1
```

## Related
**Related Objects**
- [[Object - CapControl]]

**Related Files**
- [[File - Capacitors.dss]]
- [[File - Master.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/Capacitors.dss`
- `data/OpenDSS/templates/Master.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Capacitor`
<!-- CURATED:END -->

