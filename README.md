# BWB Control Surface Sizing

Conceptual MATLAB/CasADi sizing demo for control-surface placement on a
100 ft span blended-wing-body aircraft. The planform data are generated from
the NASA/Boeing X-48 outline and scaled to the demo span.

## What is included

- `+DynamicsPkg`: BWB control-surface sizing, CasADi optimization,
  feasibility checks, and plotting.
- `+MissionSegsPkg`: minimal atmosphere/flight-condition helpers used by the
  demo.
- `+DynamicsPkg/outputs`: current generated plots and X-48-derived chord
  tables.
- `docs/dynamics_workflow.md`: workflow chart.

## Requirements

- MATLAB
- CasADi for MATLAB on the MATLAB path. The demo is set up for
  `C:\Program Files\MATLAB\casadi-3.7.2-windows64-matlab2018b` via
  `DynamicsPkg.SetupCasadi`.

## Run

From the repository root:

```matlab
DynamicsPkg.BWB_Dynamics_Demo(true, true)
```

The first argument enables the full report plots. The second argument
re-optimizes pitch-required elevon area across the CG envelope.

## Scope

This is a conceptual sizing workflow, not a validated 6DOF aircraft model. The
BWB aero/stability derivatives in `BWB_Dynamics_Demo.m` are placeholder demo
values and should be replaced with project-specific aerodynamic data before
design use.
