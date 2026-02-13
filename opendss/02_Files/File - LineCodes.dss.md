---
note_type: opendss_file
source_path: "data/OpenDSS/templates/LineCodes.dss"
declares_objects:
  - "linecode"
included_by_master: true
include_stage: "parameter_libraries"
related_files:
  []
status: "draft"
---

# File - LineCodes.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `LineCodes.dss`
- Purpose: Sequence/matrix line impedance models
- Declares: `linecode`
- Included by master: `true`
- Include stage: `parameter_libraries`
- Include index: `1` of `24`


## Auto Snippets
```dss
New LineCode.<LC_NAME> nphases=3 units=<mi|kft|km|m|ft>
~ r1=<R1_PER_LEN> x1=<X1_PER_LEN> r0=<R0_PER_LEN> x0=<X0_PER_LEN>
~ c1=<C1_PER_LEN> c0=<C0_PER_LEN>
```

```dss
New LineCode.<LC_MATRIX_NAME> nphases=3 units=<UNITS>
~ rmatrix=[<r11> | <r21> <r22> | <r31> <r32> <r33>]
~ xmatrix=[<x11> | <x21> <x22> | <x31> <x32> <x33>]
~ cmatrix=[<c11> | <c21> <c22> | <c31> <c32> <c33>]
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Sequence/matrix line impedance models

## Declared Objects
- [[Object - LineCode]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `parameter_libraries`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New LineCode.<LC_NAME> nphases=3 units=<mi|kft|km|m|ft>
~ r1=<R1_PER_LEN> x1=<X1_PER_LEN> r0=<R0_PER_LEN> x0=<X0_PER_LEN>
~ c1=<C1_PER_LEN> c0=<C0_PER_LEN>
```

```dss
New LineCode.<LC_MATRIX_NAME> nphases=3 units=<UNITS>
~ rmatrix=[<r11> | <r21> <r22> | <r31> <r32> <r33>]
~ xmatrix=[<x11> | <x21> <x22> | <x31> <x32> <x33>]
~ cmatrix=[<c11> | <c21> <c22> | <c31> <c32> <c33>]
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/LineCodes.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

