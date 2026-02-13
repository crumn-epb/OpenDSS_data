---
note_type: opendss_file
source_path: "data/OpenDSS/templates/CableData.dss"
declares_objects:
  - "cndata"
  - "tsdata"
included_by_master: true
include_stage: "parameter_libraries"
related_files:
  []
status: "draft"
---

# File - CableData.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `CableData.dss`
- Purpose: Underground cable data (CNData/TSData)
- Declares: `cndata`, `tsdata`
- Included by master: `true`
- Include stage: `parameter_libraries`
- Include index: `3` of `24`


## Auto Snippets
```dss
New CNData.<CN_NAME> Runits=<UNITS> Radunits=<UNITS> GMRunits=<UNITS>
~ rac=<RAC> gmrac=<GMR> diam=<DIAM> epsR=<EPS_R> inslayer=<INS_THK>
~ diastrand=<DIA_STRAND> gmrstrand=<GMR_STRAND> rstrand=<R_STRAND>
~ k=<NUM_STRANDS> normamps=<NORM_AMPS> emergamps=<EMERG_AMPS>
```

```dss
New TSData.<TS_NAME> Runits=<UNITS> Radunits=<UNITS> GMRunits=<UNITS>
~ rac=<RAC> gmrac=<GMR> diam=<DIAM> epsR=<EPS_R> inslayer=<INS_THK>
~ diaShield=<DIA_SHIELD> tapeLayer=<TAPE_THK> tapeLap=<TAPE_LAP_PCT>
~ normamps=<NORM_AMPS> emergamps=<EMERG_AMPS>
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Underground cable data (CNData/TSData)

## Declared Objects
- [[Object - CNData]]
- [[Object - TSData]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `parameter_libraries`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New CNData.<CN_NAME> Runits=<UNITS> Radunits=<UNITS> GMRunits=<UNITS>
~ rac=<RAC> gmrac=<GMR> diam=<DIAM> epsR=<EPS_R> inslayer=<INS_THK>
~ diastrand=<DIA_STRAND> gmrstrand=<GMR_STRAND> rstrand=<R_STRAND>
~ k=<NUM_STRANDS> normamps=<NORM_AMPS> emergamps=<EMERG_AMPS>
```

```dss
New TSData.<TS_NAME> Runits=<UNITS> Radunits=<UNITS> GMRunits=<UNITS>
~ rac=<RAC> gmrac=<GMR> diam=<DIAM> epsR=<EPS_R> inslayer=<INS_THK>
~ diaShield=<DIA_SHIELD> tapeLayer=<TAPE_THK> tapeLap=<TAPE_LAP_PCT>
~ normamps=<NORM_AMPS> emergamps=<EMERG_AMPS>
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/CableData.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

