---
note_type: opendss_object
object_class: cndata
declared_in_files:
  - CableData.dss
  - Master.dss
related_objects:
  - line
  - linegeometry
related_files:
  - CableData.dss
  - Master.dss
related_commands:
  - New
source_refs:
  - data/OpenDSS/templates/CableData.dss
  - data/OpenDSS/templates/Master.dss
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=CNData"
status: draft
---

# Object - CNData

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `cndata`
- Declared in: `CableData.dss`, `Master.dss`
- Parsed attrs: `diam`, `diastrand`, `emergamps`, `epsr`, `gmrac`, `gmrstrand`, `gmrunits`, `inslayer`, `k`, `normamps`, `rac`, `radunits`, `rstrand`, `runits`
- Description: Concentric-neutral underground cable parameter data used by geometry-based line models.
- Grid role: Supplies physical cable constants so underground branch impedance is represented correctly.

## Auto Snippets
```dss
New CNData.<CN_NAME> Runits=<UNITS> Radunits=<UNITS> GMRunits=<UNITS>
~ rac=<RAC> gmrac=<GMR> diam=<DIAM> epsR=<EPS_R> inslayer=<INS_THK>
~ diastrand=<DIA_STRAND> gmrstrand=<GMR_STRAND> rstrand=<R_STRAND>
~ k=<NUM_STRANDS> normamps=<NORM_AMPS> emergamps=<EMERG_AMPS>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
Concentric-neutral underground cable parameter data used by geometry-based line models.

## Role in Grid
Supplies physical cable constants so underground branch impedance is represented correctly.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `diam` | Conductor outer diameter. | length | Context |
| `diastrand` | Neutral strand diameter for cable model. | length | Optional |
| `emergamps` | Emergency current rating. | A | Optional |
| `epsr` | Relative permittivity for cable insulation. | scalar | Optional |
| `gmrac` | Geometric mean radius at AC conditions. | length | Context |
| `gmrstrand` | Neutral strand GMR for cable model. | length | Optional |
| `gmrunits` | Units for GMR entries. | enum | Optional |
| `inslayer` | Cable insulation layer thickness. | length | Optional |
| `k` | Class-specific scalar parameter in cable/curve definitions. | scalar | Context |
| `normamps` | Normal continuous current rating. | A | Optional |
| `rac` | AC resistance at base frequency. | ohm per length | Context |
| `radunits` | Units for radius/diameter parameters. | enum | Optional |
| `rstrand` | Neutral strand AC resistance. | ohm per length | Optional |
| `runits` | Units for resistance parameters. | enum | Optional |

## Skeleton
```dss
New CNData.<CN_NAME> Runits=<UNITS> Radunits=<UNITS> GMRunits=<UNITS>
~ rac=<RAC> gmrac=<GMR> diam=<DIAM> epsR=<EPS_R> inslayer=<INS_THK>
~ diastrand=<DIA_STRAND> gmrstrand=<GMR_STRAND> rstrand=<R_STRAND>
~ k=<NUM_STRANDS> normamps=<NORM_AMPS> emergamps=<EMERG_AMPS>
```

## Example
```dss
New CNData.obj1 Runits=kft Radunits=kft GMRunits=kft
~ rac=1 gmrac=1 diam=1 epsR=1 inslayer=1
~ diastrand=1 gmrstrand=1 rstrand=1
~ k=1 normamps=1 emergamps=1
```

## Related
**Related Objects**
- [[Object - Line]]
- [[Object - LineGeometry]]

**Related Files**
- [[File - CableData.dss]]
- [[File - Master.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/CableData.dss`
- `data/OpenDSS/templates/Master.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `CNData`
<!-- CURATED:END -->

