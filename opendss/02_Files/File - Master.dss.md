---
note_type: opendss_file
source_path: data/OpenDSS/templates/Master.dss
declares_objects:
  - capacitor
  - capcontrol
  - circuit
  - cndata
  - energymeter
  - fuse
  - generator
  - invcontrol
  - line
  - linecode
  - linegeometry
  - load
  - loadshape
  - monitor
  - pvsystem
  - recloser
  - regcontrol
  - relay
  - sensor
  - storage
  - transformer
  - wiredata
included_by_master: false
include_stage: "master_entrypoint"
related_files: []
status: draft
---

# File - Master.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `Master.dss`
- Purpose: OpenDSS template file.
- Declares: `capacitor`, `capcontrol`, `circuit`, `cndata`, `energymeter`, `fuse`, `generator`, `invcontrol`, `line`, `linecode`, `linegeometry`, `load`, `loadshape`, `monitor`, `pvsystem`, `recloser`, `regcontrol`, `relay`, `sensor`, `storage`, `transformer`, `wiredata`
- Included by master: `false`
- Include stage: `master_entrypoint`

- This file is the canonical master entrypoint.

## Auto Snippets
```dss
New Circuit.<name> fields:
```

```dss
New Circuit.<CIRCUIT_NAME> basekV=<SOURCE_KV_LL> pu=<SOURCE_PU> phases=<NPH>
~ bus1=<SOURCE_BUS> angle=<SOURCE_ANGLE_DEG> frequency=<FREQ_HZ>
~ mvasc3=<MVASC_3PH> mvasc1=<MVASC_1PH>
```

```dss
New LineCode.<name> fields:
```

## Auto Include Order
1. [[File - LineCodes.dss]]
2. [[File - WireData.dss]]
3. [[File - CableData.dss]]
4. [[File - LineGeometry.dss]]
5. [[File - LoadShape.dss]]
6. [[File - TShape.dss]]
7. [[File - PriceShape.dss]]
8. [[File - GrowthShape.dss]]
9. [[File - XYCurve.dss]]
10. [[File - TCC_Curve.dss]]
11. [[File - Lines.dss]]
12. [[File - Switches.dss]]
13. [[File - Transformers.dss]]
14. [[File - Regulators.dss]]
15. [[File - Loads.dss]]
16. [[File - Capacitors.dss]]
17. [[File - CapControls.dss]]
18. [[File - Generators.dss]]
19. [[File - PVSystems.dss]]
20. [[File - Storage.dss]]
21. [[File - InvControls.dss]]
22. [[File - Protection.dss]]
23. [[File - MetersMonitors.dss]]
24. [[File - BusCoords.dss]]
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
OpenDSS template file.

## Declared Objects
- [[Object - Capacitor]]
- [[Object - CapControl]]
- [[Object - Circuit]]
- [[Object - CNData]]
- [[Object - EnergyMeter]]
- [[Object - Fuse]]
- [[Object - Generator]]
- [[Object - InvControl]]
- [[Object - Line]]
- [[Object - LineCode]]
- [[Object - LineGeometry]]
- [[Object - Load]]
- [[Object - LoadShape]]
- [[Object - Monitor]]
- [[Object - PVSystem]]
- [[Object - Recloser]]
- [[Object - RegControl]]
- [[Object - Relay]]
- [[Object - Sensor]]
- [[Object - Storage]]
- [[Object - Transformer]]
- [[Object - WireData]]

## Include and Ordering Role
- Included by `Master.dss`: `false`
- Include stage: `master_entrypoint`
- This note is the source of include ordering for the template set.

## Skeleton Snippets
```dss
New Circuit.<name> fields:
```

```dss
New Circuit.<CIRCUIT_NAME> basekV=<SOURCE_KV_LL> pu=<SOURCE_PU> phases=<NPH>
~ bus1=<SOURCE_BUS> angle=<SOURCE_ANGLE_DEG> frequency=<FREQ_HZ>
~ mvasc3=<MVASC_3PH> mvasc1=<MVASC_1PH>
```

```dss
New LineCode.<name> fields:
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]


## Source Refs
- `data/OpenDSS/templates/Master.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->
