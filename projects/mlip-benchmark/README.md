# MLIP-Benchmark

**Comparison of interatomic potentials for their intended physical applications.**

MLIP-Benchmark evaluates candidate potentials across model architectures, connecting reference-data agreement, material properties and computational cost. It helps determine which models are suitable for a simulation task through checks that extend beyond performance on training and validation datasets.

## What the package can do

- **Compare predictions with reference data:** assess energy, force and stress agreement across the datasets relevant to the study.
- **Examine interactions over changing atomic separation:** inspect dimer behavior, including short-distance interactions that may matter in demanding simulations.
- **Evaluate structural and defect energetics:** compare relative structure energies and supported formation-energy, surface and point-defect calculations.
- **Assess material properties:** evaluate supported thermal, elastic and vibrational properties, alongside equilibrium structural behavior.
- **Compare computational cost:** examine inference time and simulation throughput, helping place prediction quality in the context of the intended workload.
- **Evaluate multiple candidates consistently:** organize comparisons across supported learned and classical potentials, with the inputs and results of each evaluation retained for inspection.
- **Revisit model selection:** analyze saved results as evaluation priorities change, without repeating the underlying calculations solely to produce a different comparison.

The package supports comparisons across several aspects of model behavior. The relevant properties and acceptable trade-offs depend on the application being considered.

## Inputs and outputs

Inputs are the candidate models, reference data and properties to evaluate. Outputs include comparable evaluation results, model rankings and diagnostic figures that support a reasoned choice of potential.

The package evaluates existing models; model training remains a separate activity.

## Applications and outcome

MLIP-Benchmark compared models from different architectures in the [tungsten study](../crystalseed/README.md#application-and-outcome) and the [carbon-surface study](../scaledown/README.md#application-and-outcomes).

In these projects, application-focused evaluations identified the models best suited to the intended simulations. Considering behavior beyond the training and validation datasets provided a stronger basis for model selection in the two physical settings.

[Portfolio](../../README.md) · [Code availability and release](../../README.md#availability)

<!-- project-metrics:start -->

## Development

| Metric | Value |
| --- | --- |
| Project languages | Python |
| Project code | 18,225 lines |
| Project files | 38 |
| Test code | 5,431 lines |
| Test files | 17 |
| External Python libraries | 20 detected (project + tests) |
| Commit history | 45 reachable commits on main |
| Last project-file change | 2026-07-19 (UTC) |
| Statistics collected | 2026-10-31 (UTC) |

<details>
<summary>Code breakdown & scope</summary>

| Component | Files | Code lines |
| --- | --- | --- |
| Package &amp; other source | 37 | 18,009 |
| Examples | 1 | 216 |
| Total project code | 38 | 18,225 |

Project code includes the package and other source files, scripts, examples and notebook code cells. Each file belongs to one component. Tests are counted separately.

Only tracked source files in the measured revision are counted. Documentation, repository automation, environments, caches, vendored code, configured output directories, data and other unselected formats are excluded. Notebook outputs and Markdown cells are excluded.

Code lines use cloc 2.10 and exclude blank lines and comments. Commit history includes every commit reachable from the measured default branch. The change date refers to currently included project files; comments and notebook output/Markdown changes can also change that date.

</details>

<details>
<summary>External Python libraries (20)</summary>

| Import name | Project files | Test files |
| --- | --- | --- |
| numpy | 15 | 8 |
| ase | 14 | 2 |
| matplotlib | 12 | 1 |
| scipy | 3 | 0 |
| yaml | 2 | 4 |
| lammps | 2 | 0 |
| tqdm | 2 | 0 |
| dftd3 | 1 | 0 |
| mace | 1 | 0 |
| mattersim | 1 | 0 |
| metatomic | 1 | 0 |
| mlip_zbl | 1 | 0 |
| nequip | 1 | 0 |
| pandas | 1 | 0 |
| pet_mad | 1 | 0 |
| phonopy | 1 | 0 |
| pymatgen | 1 | 0 |
| torch | 1 | 0 |
| upet | 1 | 0 |
| pytest | 0 | 11 |

Each top-level import name counts once per file or notebook, including optional and type-checking imports. Standard-library and detected local modules are excluded. Dynamic imports, shell/magic commands and runtime changes to import paths are not resolved. This lists direct import presence, rather than installed or transitive dependencies or runtime usage.

</details>

<!-- project-metrics:end -->
