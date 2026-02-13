---
note_type: opendss_file
source_path: "data/OpenDSS/templates/LineGeometry.dss"
declares_objects:
  - "linegeometry"
included_by_master: true
include_stage: "parameter_libraries"
related_files:
  []
status: "draft"
---

# File - LineGeometry.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `LineGeometry.dss`
- Purpose: Conductor arrangement definitions
- Declares: `linegeometry`
- Included by master: `true`
- Include stage: `parameter_libraries`
- Include index: `4` of `24`


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
## Purpose
Conductor arrangement definitions

## Declared Objects
- [[Object - LineGeometry]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `parameter_libraries`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New LineGeometry.<GEO_NAME> nconds=<NCONDS> nphases=<NPH> units=<UNITS>
~ cond=1 wire=<WIRE_OR_CABLE_A> x=<X1> h=<H1>
~ cond=2 wire=<WIRE_OR_CABLE_B> x=<X2> h=<H2>
~ cond=3 wire=<WIRE_OR_CABLE_C> x=<X3> h=<H3>
~ cond=4 wire=<NEUTRAL> x=<X4> h=<H4>
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/LineGeometry.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

