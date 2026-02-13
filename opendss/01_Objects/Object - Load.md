---
note_type: opendss_object
object_class: "load"
declared_in_files:
  - "Loads.dss"
  - "Master.dss"
related_objects:
  - "growthshape"
  - "loadshape"
  - "monitor"
related_files:
  - "Loads.dss"
  - "Master.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/Loads.dss"
  - "data/OpenDSS/templates/Master.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=Load"
status: "draft"
---

# Object - Load

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `load`
- Declared in: `Loads.dss`, `Master.dss`
- Parsed attrs: `bus1`, `conn`, `daily`, `enabled`, `kv`, `kvar`, `kw`, `model`, `phases`, `status`, `yearly`
- Description: A demand element representing customer consumption with selectable load models.
- Grid role: Represents end-use demand that drives power flow, losses, and voltage drop.

## Auto Snippets
```dss
New Load.<LOAD_NAME> bus1=<BUS> phases=<NPH> conn=<wye|delta>
~ kv=<KV> kw=<KW> kvar=<KVAR> model=<MODEL_ID>
~ daily=<LS_NAME> yearly=<LS_NAME> status=<variable|fixed> enabled=<True>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A demand element representing customer consumption with selectable load models.

## Role in Grid
Represents end-use demand that drives power flow, losses, and voltage drop.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `bus1` | Primary terminal bus connection (supports phase suffixes). | bus token | Required |
| `conn` | Connection type for element terminals. | wye|delta | Context |
| `daily` | Daily profile object applied to element. | LoadShape name | Optional |
| `enabled` | Enable/disable this element. | True/False | Optional |
| `kv` | Nominal voltage level for element connection. | kV | Context |
| `kvar` | Reactive power value or rating. | kvar | Context |
| `kw` | Active power value or rating. | kW | Context |
| `model` | Load model code controlling voltage-dependence behavior. | integer code | Context |
| `phases` | Phase count for connected element. | integer | Context |
| `status` | Load variability mode (e.g., variable/fixed). | enum | Optional |
| `yearly` | Yearly profile object applied to element. | LoadShape name | Optional |

## Skeleton
```dss
New Load.<LOAD_NAME> bus1=<BUS> phases=<NPH> conn=<wye|delta>
~ kv=<KV> kw=<KW> kvar=<KVAR> model=<MODEL_ID>
~ daily=<LS_NAME> yearly=<LS_NAME> status=<variable|fixed> enabled=<True>
```

## Example
```dss
New Load.obj1 bus1=BUS1.1.2.3 phases=3 conn=wye
~ kv=12.47 kw=500 kvar=12.47 model=VOLTVAR
~ daily=obj1 yearly=obj1 status=variable enabled=1
```

## Related
**Related Objects**
- [[Object - GrowthShape]]
- [[Object - LoadShape]]
- [[Object - Monitor]]

**Related Files**
- [[File - Loads.dss]]
- [[File - Master.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/Loads.dss`
- `data/OpenDSS/templates/Master.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Load`
<!-- CURATED:END -->

