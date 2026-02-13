---
note_type: opendss_object
object_class: "tsdata"
declared_in_files:
  - "CableData.dss"
related_objects:
  - "line"
  - "linegeometry"
related_files:
  - "CableData.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/CableData.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=TSData"
status: "draft"
---

# Object - TSData

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `tsdata`
- Declared in: `CableData.dss`
- Parsed attrs: `diam`, `diashield`, `emergamps`, `epsr`, `gmrac`, `gmrunits`, `inslayer`, `normamps`, `rac`, `radunits`, `runits`, `tapelap`, `tapelayer`
- Description: Tape-shield underground cable parameter data used by geometry-based line models.
- Grid role: Provides cable shield properties needed for realistic underground feeder representation.

## Auto Snippets
```dss
New TSData.<TS_NAME> Runits=<UNITS> Radunits=<UNITS> GMRunits=<UNITS>
~ rac=<RAC> gmrac=<GMR> diam=<DIAM> epsR=<EPS_R> inslayer=<INS_THK>
~ diaShield=<DIA_SHIELD> tapeLayer=<TAPE_THK> tapeLap=<TAPE_LAP_PCT>
~ normamps=<NORM_AMPS> emergamps=<EMERG_AMPS>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
Tape-shield underground cable parameter data used by geometry-based line models.

## Role in Grid
Provides cable shield properties needed for realistic underground feeder representation.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `diam` | Conductor outer diameter. | length | Context |
| `diashield` | Tape shield diameter for cable model. | length | Optional |
| `emergamps` | Emergency current rating. | A | Optional |
| `epsr` | Relative permittivity for cable insulation. | scalar | Optional |
| `gmrac` | Geometric mean radius at AC conditions. | length | Context |
| `gmrunits` | Units for GMR entries. | enum | Optional |
| `inslayer` | Cable insulation layer thickness. | length | Optional |
| `normamps` | Normal continuous current rating. | A | Optional |
| `rac` | AC resistance at base frequency. | ohm per length | Context |
| `radunits` | Units for radius/diameter parameters. | enum | Optional |
| `runits` | Units for resistance parameters. | enum | Optional |
| `tapelap` | Tape shield overlap percentage. | percent | Optional |
| `tapelayer` | Tape shield thickness. | length | Optional |

## Skeleton
```dss
New TSData.<TS_NAME> Runits=<UNITS> Radunits=<UNITS> GMRunits=<UNITS>
~ rac=<RAC> gmrac=<GMR> diam=<DIAM> epsR=<EPS_R> inslayer=<INS_THK>
~ diaShield=<DIA_SHIELD> tapeLayer=<TAPE_THK> tapeLap=<TAPE_LAP_PCT>
~ normamps=<NORM_AMPS> emergamps=<EMERG_AMPS>
```

## Example
```dss
New TSData.obj1 Runits=kft Radunits=kft GMRunits=kft
~ rac=1 gmrac=1 diam=1 epsR=1 inslayer=1
~ diaShield=1 tapeLayer=1 tapeLap=1
~ normamps=1 emergamps=1
```

## Related
**Related Objects**
- [[Object - Line]]
- [[Object - LineGeometry]]

**Related Files**
- [[File - CableData.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/CableData.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `TSData`
<!-- CURATED:END -->

