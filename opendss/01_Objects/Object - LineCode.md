---
note_type: opendss_object
object_class: "linecode"
declared_in_files:
  - "LineCodes.dss"
  - "Master.dss"
related_objects:
  - "line"
related_files:
  - "LineCodes.dss"
  - "Master.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/LineCodes.dss"
  - "data/OpenDSS/templates/Master.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=LineCode"
status: "draft"
---

# Object - LineCode

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `linecode`
- Declared in: `LineCodes.dss`, `Master.dss`
- Parsed attrs: `c0`, `c1`, `cmatrix`, `nphases`, `r0`, `r1`, `rmatrix`, `units`, `x0`, `x1`, `xmatrix`
- Description: A reusable impedance/capacitance parameter set referenced by line objects.
- Grid role: Standardizes branch electrical parameters to keep line modeling consistent across the feeder.

## Auto Snippets
```dss
New LineCode.<LC_NAME> nphases=3 units=<mi|kft|km|m|ft>
~ r1=<R1_PER_LEN> x1=<X1_PER_LEN> r0=<R0_PER_LEN> x0=<X0_PER_LEN>
~ c1=<C1_PER_LEN> c0=<C0_PER_LEN>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A reusable impedance/capacitance parameter set referenced by line objects.

## Role in Grid
Standardizes branch electrical parameters to keep line modeling consistent across the feeder.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `c0` | Zero-sequence capacitance per unit length. | nF per length | Context |
| `c1` | Positive-sequence capacitance per unit length. | nF per length | Context |
| `cmatrix` | Phase capacitance matrix entries. | nF per length matrix | Context |
| `nphases` | Number of phases represented by parameter object. | integer | Context |
| `r0` | Zero-sequence resistance per unit length. | ohm per length | Context |
| `r1` | Positive-sequence resistance per unit length. | ohm per length | Context |
| `rmatrix` | Phase resistance matrix entries. | ohm per length matrix | Context |
| `units` | Engineering units associated with this object. | enum | Context |
| `x0` | Zero-sequence reactance per unit length. | ohm per length | Context |
| `x1` | Positive-sequence reactance per unit length. | ohm per length | Context |
| `xmatrix` | Phase reactance matrix entries. | ohm per length matrix | Context |

## Skeleton
```dss
New LineCode.<LC_NAME> nphases=3 units=<mi|kft|km|m|ft>
~ r1=<R1_PER_LEN> x1=<X1_PER_LEN> r0=<R0_PER_LEN> x0=<X0_PER_LEN>
~ c1=<C1_PER_LEN> c0=<C0_PER_LEN>
```

## Example
```dss
New LineCode.obj1 nphases=3 units=mi
~ r1=1.0 x1=1.0 r0=1.0 x0=1.0
~ c1=1.0 c0=1.0
```

## Related
**Related Objects**
- [[Object - Line]]

**Related Files**
- [[File - LineCodes.dss]]
- [[File - Master.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/LineCodes.dss`
- `data/OpenDSS/templates/Master.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `LineCode`
<!-- CURATED:END -->

