---
note_type: opendss_object
object_class: capcontrol
declared_in_files:
  - CapControls.dss
  - Master.dss
related_objects:
  - capacitor
  - line
  - transformer
related_files:
  - CapControls.dss
  - Master.dss
related_commands:
  - New
source_refs:
  - data/OpenDSS/templates/CapControls.dss
  - data/OpenDSS/templates/Master.dss
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=CapControl"
status: draft
---

# Object - CapControl

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `capcontrol`
- Declared in: `CapControls.dss`, `Master.dss`
- Parsed attrs: `capacitor`, `delay`, `element`, `offsetting`, `onsetting`, `terminal`, `type`
- Description: A control element that operates capacitor steps using voltage/current/kvar/time logic.
- Grid role: Automates reactive compensation timing/location so voltage and power-factor targets are maintained.

## Auto Snippets
```dss
New CapControl.<CAPCTRL_NAME> capacitor=<CAP_NAME>
~ element=<Line|Transformer.NAME> terminal=<TERM> type=<current>
~ onsetting=<ON_VALUE> offsetting=<OFF_VALUE> delay=<SEC>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A control element that operates capacitor steps using voltage/current/kvar/time logic.

## Role in Grid
Automates reactive compensation timing/location so voltage and power-factor targets are maintained.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `capacitor` | Capacitor object name controlled by this controller. | object reference | Required |
| `delay` | Intentional control/protection action delay. | seconds | Optional |
| `element` | Target element reference used by monitor/meter/control. | object reference | Context |
| `offsetting` | Turn-off threshold for selected control type. | class-dependent | Context |
| `onsetting` | Turn-on threshold for selected control type. | class-dependent | Context |
| `terminal` | Terminal index for monitor/meter/sensor/control. | integer | Context |
| `type` | Capacitor control algorithm type. | current|voltage|kvar|pf|time | Context |

## Skeleton
```dss
New CapControl.<CAPCTRL_NAME> capacitor=<CAP_NAME>
~ element=<Line|Transformer.NAME> terminal=<TERM> type=<current>
~ onsetting=<ON_VALUE> offsetting=<OFF_VALUE> delay=<SEC>
```

## Example
```dss
New CapControl.obj1 capacitor=obj1
~ element=Line terminal=1 type=1
~ onsetting=1 offsetting=1 delay=1
```

## Related
**Related Objects**
- [[Object - Capacitor]]
- [[Object - Line]]
- [[Object - Transformer]]

**Related Files**
- [[File - CapControls.dss]]
- [[File - Master.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/CapControls.dss`
- `data/OpenDSS/templates/Master.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `CapControl`
<!-- CURATED:END -->

