---
note_type: opendss_object
object_class: "linegeometry"
declared_in_files:
  - "LineGeometry.dss"
  - "Master.dss"
related_objects:
  - "cndata"
  - "line"
  - "tsdata"
  - "wiredata"
related_files:
  - "LineGeometry.dss"
  - "Master.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/LineGeometry.dss"
  - "data/OpenDSS/templates/Master.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=LineGeometry"
status: "draft"
---

# Object - LineGeometry

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `linegeometry`
- Declared in: `LineGeometry.dss`, `Master.dss`
- Parsed attrs: `cond`, `h`, `nconds`, `nphases`, `units`, `wire`, `x`
- Description: A geometric conductor arrangement definition used to derive phase impedance/admittance.
- Grid role: Captures conductor placement effects that influence impedance coupling and unbalanced behavior.

## Auto Snippets
```dss
New LineGeometry.<GEO_NAME> nconds=<NCONDS> nphases=<NPH> units=<UNITS>
~ cond=1 wire=<WIRE_OR_CABLE_A> x=<X1> h=<H1>
~ cond=2 wire=<WIRE_OR_CABLE_B> x=<X2> h=<H2>
~ cond=3 wire=<WIRE_OR_CABLE_C> x=<X3> h=<H3>
~ cond=4 wire=<NEUTRAL> x=<X4> h=<H4>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A geometric conductor arrangement definition used to derive phase impedance/admittance.

## Role in Grid
Captures conductor placement effects that influence impedance coupling and unbalanced behavior.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `cond` | Conductor index in LineGeometry definition. | integer | Required |
| `h` | Conductor height coordinate in geometry. | length | Context |
| `nconds` | Total conductors in geometry. | integer | Required |
| `nphases` | Number of phases represented by parameter object. | integer | Context |
| `units` | Engineering units associated with this object. | enum | Context |
| `wire` | Wire/CN/TS data object name in geometry entry. | object reference | Required |
| `x` | Reactance-like setting (class-dependent). | ohm or class-dependent | Context |

## Skeleton
```dss
New LineGeometry.<GEO_NAME> nconds=<NCONDS> nphases=<NPH> units=<UNITS>
~ cond=1 wire=<WIRE_OR_CABLE_A> x=<X1> h=<H1>
~ cond=2 wire=<WIRE_OR_CABLE_B> x=<X2> h=<H2>
~ cond=3 wire=<WIRE_OR_CABLE_C> x=<X3> h=<H3>
~ cond=4 wire=<NEUTRAL> x=<X4> h=<H4>
```

## Example
```dss
New LineGeometry.obj1 nconds=1 nphases=3 units=kft
~ cond=1 wire=1 x=1 h=1
~ cond=2 wire=1 x=1 h=1
~ cond=3 wire=1 x=1 h=1
~ cond=4 wire=1 x=1 h=1
```

## Related
**Related Objects**
- [[Object - CNData]]
- [[Object - Line]]
- [[Object - TSData]]
- [[Object - WireData]]

**Related Files**
- [[File - LineGeometry.dss]]
- [[File - Master.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/LineGeometry.dss`
- `data/OpenDSS/templates/Master.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `LineGeometry`
<!-- CURATED:END -->

