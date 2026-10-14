# CE-MRCPSP benchmark instances

This repository contains benchmark instances and parameter settings for multi-mode resource-constrained project scheduling with cumulative high-load exposure (CE-MRCPSP).

## Contents

- `J10/`: 36 selected instances with 10 real activities.
- `J20/`: 52 selected instances with 20 real activities.
- `J30/`: 52 selected instances with 30 real activities.
- `Parameters/`: instance schema, scenario-calibration parameters and basic benchmark settings.
- `Instance_index.csv`: file identifiers, activity-set sizes and provenance hashes.
- `MANIFEST.csv`: file sizes and SHA-256 checksums for the files in this distribution, excluding the manifest itself.

The 140 instances are selected study inputs, not the complete original PSPLIB J10/J20/J30 libraries. Each JSON file retains all six calibrated management scenarios and the frozen input values used in the study.

## Input format

Each instance JSON contains activity modes, durations, resource demands, precedence relations, physical resource capacities, a scheduling horizon, and scenario-specific operating thresholds and cumulative-exposure budgets. Dummy start and finish activities are retained. Field definitions are provided in `Parameters/Instance_schema.json`.

Actual per-instance thresholds and budgets are stored in the instance's `scenarios` field. `Parameters/Scenario_calibration.json` describes their calibration and is not a substitute for these instance-specific values. The six scenario labels are `lenient`, `balanced`, `strict`, `threshold_sensitive`, `budget_sensitive`, and `heterogeneous`. Nonrenewable-resource fields are retained; activation flags indicate whether those constraints are included in the core model.

## Scope

The repository file tree contains benchmark instances and parameter settings. The complete reproducibility package, including source code, experiment and analysis scripts, additional inputs, and archived numerical results, is available in release v1.0. Download the attached Supplementary.Material.zip and follow the README inside the archive. GitHub’s automatically generated “Source code” archives do not contain this complete package.

## Provenance and third-party rights

The benchmark instance records derive from PSPLIB. Original instance identifiers and source hashes are retained in the records and in `Instance_index.csv`.

PSPLIB source reference: Kolisch, R., & Sprecher, A. (1997). PSPLIB - A project scheduling problem library. European Journal of Operational Research, 96(1), 205-216. https://doi.org/10.1016/S0377-2217(96)00170-1

Original benchmark provider: https://www.om-db.wi.tum.de/psplib/

Third-party benchmark material remains subject to the rights and terms of its original provider. This repository does not grant an additional licence for that material.
