---
note_type: opendss_object
object_class: fuse
declared_in_files:
  - Master.dss
  - Protection.dss
related_objects:
  - line
  - recloser
  - relay
  - tcc_curve
related_files:
  - Master.dss
  - Protection.dss
related_commands:
  - New
source_refs:
  - data/OpenDSS/templates/Master.dss
  - data/OpenDSS/templates/Protection.dss
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=Fuse"
status: draft
---

# Object - Fuse

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `fuse`
- Declared in: `Master.dss`, `Protection.dss`
- Parsed attrs: `fusecurve`, `monitoredobj`, `monitoredterm`, `ratedcurrent`, `switchedobj`, `switchedterm`
- Description: A protection device model with current-time behavior for isolating faults.
- Grid role: Isolates faulted sections to limit outage extent and protect downstream equipment.

## Auto Snippets
```dss
New Fuse.<name> monitoredobj=<Line.name> monitoredterm=<1>
~ switchedobj=<Line.name> switchedterm=<1> fusecurve=<TCC_NAME> ratedcurrent=<A>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A protection device model with current-time behavior for isolating faults.

## Role in Grid
Isolates faulted sections to limit outage extent and protect downstream equipment.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `fusecurve` | TCC curve name used by fuse. | TCC_Curve reference | Context |
| `monitoredobj` | Element monitored by protection/control. | object reference | Required |
| `monitoredterm` | Terminal index used for monitored quantities. | integer | Context |
| `ratedcurrent` | Protection rated current value. | A | Context |
| `switchedobj` | Element operated by protection/control. | object reference | Required |
| `switchedterm` | Terminal index on switched element. | integer | Context |

## Skeleton
```dss
New Fuse.<name> monitoredobj=<Line.name> monitoredterm=<1>
~ switchedobj=<Line.name> switchedterm=<1> fusecurve=<TCC_NAME> ratedcurrent=<A>
```

## Example
```dss
New Fuse.obj1 monitoredobj=obj1 monitoredterm=1
~ switchedobj=obj1 switchedterm=1 fusecurve=obj1 ratedcurrent=1
```

## Related
**Related Objects**
- [[Object - Line]]
- [[Object - Recloser]]
- [[Object - Relay]]
- [[Object - TCC_Curve]]

**Related Files**
- [[File - Master.dss]]
- [[File - Protection.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/Master.dss`
- `data/OpenDSS/templates/Protection.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Fuse`
<!-- CURATED:END -->

