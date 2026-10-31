# MLIP-ZBL

**Short-range repulsive correction for machine-learning interatomic potentials.**

MLIP-ZBL addresses close atomic encounters in simulations using learned interatomic potentials. It adds an appropriate short-range repulsive response while retaining the underlying model's behavior in the interaction regime described by density functional theory (DFT).

## What the package can do

- **Correct short-range interactions:** improve the repulsive behavior of an existing potential when atoms approach closely.
- **Preserve the established interaction regime:** retain the base model's behavior in the DFT-described range, with a smooth transition to the corrected short-range response.
- **Support different material systems:** apply the correction to supported potentials for the chemical systems of interest.
- **Work with several model families:** support MACE, NequIP, MatterSim and UPET models through the available integrations.
- **Use corrected potentials in simulations:** provide supported routes for ASE and LAMMPS workflows, with availability depending on the model backend.
- **Inspect the corrected response:** examine energy and force behavior as atoms approach and assess the connection between the short-range and ordinary interaction regimes.

These capabilities are useful when a simulation involves both ordinary material behavior and close encounters, as can occur under energetic bombardment. They allow an existing potential to be adapted for that use while retaining its role in the broader simulation workflow.

## Inputs and outputs

The starting point is an existing machine-learning interatomic potential and the chemical system in which it will be used. The result is a potential with a corrected short-range response, together with diagnostics for examining its behavior in the supported workflows.

The package focuses on this correction; training the underlying potential is a separate activity.

## Applications and outcome

MLIP-ZBL was applied to the potentials used in the [tungsten study](../crystalseed/README.md#application-and-outcome) and the [carbon-surface study](../scaledown/README.md#application-and-outcomes).

In both projects, it achieved the intended short-range correction while preserving behavior in the DFT-described regime. The corrected and preserved regions were connected through a smooth transition, meeting the modeling objectives of those applications.

[Portfolio](../../README.md) · [Code availability and release](../../README.md#availability)

<!-- project-metrics:start -->

## Development

| Metric | Value |
| --- | --- |
| Project languages | Python |
| Project code | 7,592 lines |
| Project files | 46 |
| Test code | 2,284 lines |
| Test files | 27 |
| External Python libraries | 12 detected (project + tests) |
| Commit history | 24 reachable commits on main |
| Last project-file change | 2026-07-05 (UTC) |
| Statistics collected | 2026-10-31 (UTC) |

<details>
<summary>Code breakdown & scope</summary>

| Component | Files | Code lines |
| --- | --- | --- |
| Package &amp; other source | 46 | 7,592 |
| Total project code | 46 | 7,592 |

Project code includes the package and other source files, scripts, examples and notebook code cells. Each file belongs to one component. Tests are counted separately.

Only tracked source files in the measured revision are counted. Documentation, repository automation, environments, caches, vendored code, configured output directories, data and other unselected formats are excluded. Notebook outputs and Markdown cells are excluded.

Code lines use cloc 2.10 and exclude blank lines and comments. Commit history includes every commit reachable from the measured default branch. The change date refers to currently included project files; comments and notebook output/Markdown changes can also change that date.

</details>

<details>
<summary>External Python libraries (12)</summary>

| Import name | Project files | Test files |
| --- | --- | --- |
| torch | 22 | 15 |
| ase | 11 | 6 |
| numpy | 8 | 10 |
| yaml | 5 | 0 |
| lammps | 3 | 0 |
| metatomic | 3 | 0 |
| mlip_benchmark | 2 | 1 |
| mace | 2 | 0 |
| nequip | 1 | 1 |
| mattersim | 1 | 0 |
| metatensor | 1 | 0 |
| optuna | 1 | 0 |

Each top-level import name counts once per file or notebook, including optional and type-checking imports. Standard-library and detected local modules are excluded. Dynamic imports, shell/magic commands and runtime changes to import paths are not resolved. This lists direct import presence, rather than installed or transitive dependencies or runtime usage.

</details>

<!-- project-metrics:end -->
