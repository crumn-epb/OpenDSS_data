---
note_type: opendss_object
object_class: "pvsystem"
declared_in_files:
  - "Master.dss"
  - "PVSystems.dss"
related_objects:
  - "invcontrol"
  - "loadshape"
  - "monitor"
  - "xycurve"
related_files:
  - "Master.dss"
  - "PVSystems.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/Master.dss"
  - "data/OpenDSS/templates/PVSystems.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=PVSystem"
status: "draft"
---

# Object - PVSystem

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `pvsystem`
- Declared in: `Master.dss`, `PVSystems.dss`
- Parsed attrs: `bus1`, `conn`, `daily`, `enabled`, `irradiance`, `kv`, `kva`, `phases`, `pmpp`, `temperature`, `yearly`
- Description: A photovoltaic DER element with inverter rating and irradiance-driven output behavior.
- Grid role: Injects variable solar generation at distribution buses and interacts with voltage controls.

## Auto Snippets
```dss
New PVSystem.<name> bus1=<BUS> phases=<NPH> conn=<wye> kv=<KV>
~ pmpp=<PMPP_KW> kva=<KVA_RATING> irradiance=<PU_IRRAD>
~ temperature=<DEGC> daily=<IRR_SHAPE> yearly=<IRR_SHAPE>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A photovoltaic DER element with inverter rating and irradiance-driven output behavior.

## Role in Grid
Injects variable solar generation at distribution buses and interacts with voltage controls.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `bus1` | Primary terminal bus connection (supports phase suffixes). | bus token | Required |
| `conn` | Connection type for element terminals. | wye|delta | Context |
| `daily` | Daily profile object applied to element. | LoadShape name | Optional |
| `enabled` | Enable/disable this element. | True/False | Optional |
| `irradiance` | Current irradiance multiplier used for output scaling. | per-unit | Context |
| `kv` | Nominal voltage level for element connection. | kV | Context |
| `kva` | Apparent power rating. | kVA | Context |
| `phases` | Phase count for connected element. | integer | Context |
| `pmpp` | PV array maximum power point at reference conditions. | kW | Context |
| `temperature` | PV cell/module temperature input. | degC | Optional |
| `yearly` | Yearly profile object applied to element. | LoadShape name | Optional |

## Skeleton
```dss
New PVSystem.<name> bus1=<BUS> phases=<NPH> conn=<wye> kv=<KV>
~ pmpp=<PMPP_KW> kva=<KVA_RATING> irradiance=<PU_IRRAD>
~ temperature=<DEGC> daily=<IRR_SHAPE> yearly=<IRR_SHAPE>
```

## Example
```dss
New PVSystem.obj1 bus1=BUS1.1.2.3 phases=3 conn=1 kv=12.47
~ pmpp=500 kva=12.47 irradiance=1
~ temperature=1 daily=1 yearly=1
```

## Related
**Related Objects**
- [[Object - InvControl]]
- [[Object - LoadShape]]
- [[Object - Monitor]]
- [[Object - XYCurve]]

**Related Files**
- [[File - Master.dss]]
- [[File - PVSystems.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/Master.dss`
- `data/OpenDSS/templates/PVSystems.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `PVSystem`
<!-- CURATED:END -->

