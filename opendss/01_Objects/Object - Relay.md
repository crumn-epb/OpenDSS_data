---
note_type: opendss_object
object_class: "relay"
declared_in_files:
  - "Master.dss"
  - "Protection.dss"
related_objects:
  - "fuse"
  - "line"
  - "recloser"
  - "tcc_curve"
  - "transformer"
related_files:
  - "Master.dss"
  - "Protection.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/Master.dss"
  - "data/OpenDSS/templates/Protection.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=Relay"
status: "draft"
---

# Object - Relay

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `relay`
- Declared in: `Master.dss`, `Protection.dss`
- Parsed attrs: `monitoredobj`, `monitoredterm`, `switchedobj`, `switchedterm`, `type`
- Description: A configurable protection relay model that supervises and trips assigned elements.
- Grid role: Implements selective protection logic to detect abnormal conditions and trigger tripping.

## Auto Snippets
```dss
New Relay.<name> monitoredobj=<Line.name> monitoredterm=<1>
~ switchedobj=<Line.name> switchedterm=<1> type=<current|voltage|reversepower>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A configurable protection relay model that supervises and trips assigned elements.

## Role in Grid
Implements selective protection logic to detect abnormal conditions and trigger tripping.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `monitoredobj` | Element monitored by protection/control. | object reference | Required |
| `monitoredterm` | Terminal index used for monitored quantities. | integer | Context |
| `switchedobj` | Element operated by protection/control. | object reference | Required |
| `switchedterm` | Terminal index on switched element. | integer | Context |
| `type` | Controller/protection type selection. | enum | Context |

## Skeleton
```dss
New Relay.<name> monitoredobj=<Line.name> monitoredterm=<1>
~ switchedobj=<Line.name> switchedterm=<1> type=<current|voltage|reversepower>
```

## Example
```dss
New Relay.obj1 monitoredobj=obj1 monitoredterm=1
~ switchedobj=obj1 switchedterm=1 type=current
```

## Related
**Related Objects**
- [[Object - Fuse]]
- [[Object - Line]]
- [[Object - Recloser]]
- [[Object - TCC_Curve]]
- [[Object - Transformer]]

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
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Relay`
<!-- CURATED:END -->

