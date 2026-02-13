---
note_type: opendss_object
object_class: generator
declared_in_files:
  - Generators.dss
  - Master.dss
related_objects:
  - loadshape
  - monitor
related_files:
  - Generators.dss
  - Master.dss
related_commands:
  - New
source_refs:
  - data/OpenDSS/templates/Generators.dss
  - data/OpenDSS/templates/Master.dss
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=Generator"
status: draft
---

# Object - Generator

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `generator`
- Declared in: `Generators.dss`, `Master.dss`
- Parsed attrs: `bus1`, `enabled`, `kv`, `kvar`, `kw`, `model`, `phases`, `vpu`
- Description: A dispatchable generation element with configurable active/reactive behavior.
- Grid role: Injects controllable real/reactive power to support local demand or upstream export.

## Auto Snippets
```dss
New Generator.<GEN_NAME> bus1=<BUS> phases=<NPH> kv=<KV>
~ kw=<KW> kvar=<KVAR> model=<MODEL_ID> vpu=<VPU_SET> enabled=<True>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A dispatchable generation element with configurable active/reactive behavior.

## Role in Grid
Injects controllable real/reactive power to support local demand or upstream export.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `bus1` | Primary terminal bus connection (supports phase suffixes). | bus token | Required |
| `enabled` | Enable/disable this element. | True/False | Optional |
| `kv` | Nominal voltage level for element connection. | kV | Context |
| `kvar` | Reactive power value or rating. | kvar | Context |
| `kw` | Active power value or rating. | kW | Context |
| `model` | OpenDSS model code selecting element behavior. | integer | Context |
| `phases` | Phase count for connected element. | integer | Context |
| `vpu` | Per-unit voltage setpoint/value. | per-unit | Optional |

## Skeleton
```dss
New Generator.<GEN_NAME> bus1=<BUS> phases=<NPH> kv=<KV>
~ kw=<KW> kvar=<KVAR> model=<MODEL_ID> vpu=<VPU_SET> enabled=<True>
```

## Example
```dss
New Generator.obj1 bus1=BUS1.1.2.3 phases=3 kv=12.47
~ kw=500 kvar=12.47 model=VOLTVAR vpu=1 enabled=1
```

## Related
**Related Objects**
- [[Object - LoadShape]]
- [[Object - Monitor]]

**Related Files**
- [[File - Generators.dss]]
- [[File - Master.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/Generators.dss`
- `data/OpenDSS/templates/Master.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Generator`
<!-- CURATED:END -->

