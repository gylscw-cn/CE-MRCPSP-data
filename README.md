# CE-MRCPSP benchmark instances

This is an **instance-and-parameter-only** data package for multi-mode resource-constrained project scheduling with cumulative high-load exposure.

## Contents

- `J10/`: 36 selected instances with 10 real activities.
- `J20/`: 52 selected instances with 20 real activities.
- `J30/`: 52 selected instances with 30 real activities.
- `Parameters/`: instance schema, scenario-calibration parameters and basic benchmark settings.
- `Instance_index.csv`: file identifiers, sizes of the activity sets and provenance hashes.
- `MANIFEST.csv`: file sizes and SHA-256 checksums for this distribution.

These are 140 selected inputs used in the study, not the complete original PSPLIB J10/J20/J30 libraries. Each JSON file retains all six calibrated management scenarios and the original frozen input values. No optimization or data generation was rerun during preparation.

## Input format

An instance JSON contains activity modes, durations, resource demands, precedence, physical resource capacities, scheduling horizon, and scenario-specific operating thresholds and cumulative-exposure budgets. Dummy start/end activities are retained. Activity/mode source identifiers and the original PSPLIB file/hash provide provenance. The fields in `Parameters/Instance_schema.json` describe the JSON structure.

Actual per-instance thresholds and budgets are in the instance's `scenarios` field. The calibration file describes how they were specified; it is not a replacement for those actual input vectors. Six scenario labels are lenient, balanced, strict, threshold_sensitive, budget_sensitive and heterogeneous. Nonrenewable benchmark fields are retained, but activation flags indicate whether those constraints are part of the core model.

## Not included

Algorithm source, ablation outputs, algorithm-comparison outputs, sensitivity outcomes, solver results, statistical tables, figures, road-case results and manuscript files are **not included**. This package does not claim that all experiments can be reproduced from these files alone, nor that source code or experimental results have been publicly released.

## Third-party material and release status

The instance records derive from PSPLIB; original names and source hashes are retained. Redistribution permission and required attribution for the selected derived records must be confirmed by the authors before public release. No data license is assigned on the authors' behalf by this preparation step.

This candidate has been prepared locally. No repository URL or DOI is claimed. File-content identity scanning does not establish anonymity of a future repository account or commit history; those require a separate check at upload time.
