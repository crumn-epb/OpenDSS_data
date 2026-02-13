---
note_type: opendss_file
source_path: "data/OpenDSS/templates/Protection.dss"
declares_objects:
  - "fuse"
  - "recloser"
  - "relay"
included_by_master: true
include_stage: "protection_and_monitoring"
related_files:
  []
status: "draft"
---

# File - Protection.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `Protection.dss`
- Purpose: Fuses, reclosers, relays
- Declares: `fuse`, `recloser`, `relay`
- Included by master: `true`
- Include stage: `protection_and_monitoring`
- Include index: `22` of `24`


## Auto Snippets
```dss
New Fuse.<FUSE_NAME> monitoredobj=<Line.NAME> monitoredterm=<1>
~ switchedobj=<Line.NAME> switchedterm=<1> fusecurve=<TCC_NAME> ratedcurrent=<A>
```

```dss
New Recloser.<REC_NAME> monitoredobj=<Line.NAME> monitoredterm=<1>
~ switchedobj=<Line.NAME> switchedterm=<1> phasecurve=<TCC_NAME> groundcurve=<TCC_NAME>
~ phaseTrip=<A> groundTrip=<A> shots=<N>
```

```dss
New Relay.<REL_NAME> monitoredobj=<Line.NAME> monitoredterm=<1>
~ switchedobj=<Line.NAME> switchedterm=<1> type=<current|voltage|reversepower>
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Fuses, reclosers, relays

## Declared Objects
- [[Object - Fuse]]
- [[Object - Recloser]]
- [[Object - Relay]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `protection_and_monitoring`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New Fuse.<FUSE_NAME> monitoredobj=<Line.NAME> monitoredterm=<1>
~ switchedobj=<Line.NAME> switchedterm=<1> fusecurve=<TCC_NAME> ratedcurrent=<A>
```

```dss
New Recloser.<REC_NAME> monitoredobj=<Line.NAME> monitoredterm=<1>
~ switchedobj=<Line.NAME> switchedterm=<1> phasecurve=<TCC_NAME> groundcurve=<TCC_NAME>
~ phaseTrip=<A> groundTrip=<A> shots=<N>
```

```dss
New Relay.<REL_NAME> monitoredobj=<Line.NAME> monitoredterm=<1>
~ switchedobj=<Line.NAME> switchedterm=<1> type=<current|voltage|reversepower>
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/Protection.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

