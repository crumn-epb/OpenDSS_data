---
note_type: opendss_object
object_class: "sensor"
declared_in_files:
  - "Master.dss"
  - "MetersMonitors.dss"
related_objects:
  - "line"
  - "monitor"
  - "transformer"
related_files:
  - "Master.dss"
  - "MetersMonitors.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/Master.dss"
  - "data/OpenDSS/templates/MetersMonitors.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=Sensor"
status: "draft"
---

# Object - Sensor

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `sensor`
- Declared in: `Master.dss`, `MetersMonitors.dss`
- Parsed attrs: `clear`, `element`, `kvars`, `kvbase`, `kws`, `terminal`
- Description: A measurement element for injecting observed values into monitoring/state-estimation workflows.
- Grid role: Supplies measured observables that improve situational awareness and model-data alignment.

## Auto Snippets
```dss
New Sensor.<name> element=<Line|Transformer.name> terminal=<TERM>
~ kVbase=<KV_BASE> clear=<Yes|No> kWs=[...] kvars=[...]
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A measurement element for injecting observed values into monitoring/state-estimation workflows.

## Role in Grid
Supplies measured observables that improve situational awareness and model-data alignment.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `clear` | Reset/clear sensor stored values at solve start. | Yes/No | Optional |
| `element` | Target element reference used by monitor/meter/control. | object reference | Context |
| `kvars` | Reactive measurement list (e.g., Sensor). | array<kvar> | Optional |
| `kvbase` | Base voltage for sensor/measurement scaling. | kV | Optional |
| `kws` | Active measurement list (e.g., Sensor). | array<kW> | Optional |
| `terminal` | Terminal index for monitor/meter/sensor/control. | integer | Context |

## Skeleton
```dss
New Sensor.<name> element=<Line|Transformer.name> terminal=<TERM>
~ kVbase=<KV_BASE> clear=<Yes|No> kWs=[...] kvars=[...]
```

## Example
```dss
New Sensor.obj1 element=Line terminal=1
~ kVbase=12.47 clear=Yes kWs=[...] kvars=[...]
```

## Related
**Related Objects**
- [[Object - Line]]
- [[Object - Monitor]]
- [[Object - Transformer]]

**Related Files**
- [[File - Master.dss]]
- [[File - MetersMonitors.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/Master.dss`
- `data/OpenDSS/templates/MetersMonitors.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Sensor`
<!-- CURATED:END -->

