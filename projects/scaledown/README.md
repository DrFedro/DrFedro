# ScaleDown

**Small periodic cells for DFT calculations from large atomistic structures and trajectories.**

ScaleDown takes large atomic structures or trajectory frames and constructs smaller periodic cells that are tractable for density functional theory (DFT) calculations.

Its purpose is to make selected atomic environments available for reference calculations and potential development when evaluating the complete source structure would be too expensive.

## What the package can do

- **Identify useful atomic environments:** select atomic surroundings of interest from the input structures for subsequent reference evaluation.
- **Preserve environments in a smaller periodic cell:** construct compact cells designed to reproduce selected local atomic environments from the original structure as closely as possible, accounting for periodic boundary conditions and the environments near the cell boundaries.
- **Work with structures and trajectories:** process individual configurations or collections of frames.
- **Control the size of the reference workload:** adapt cell sizes and the final collection to the available computational budget.
- **Check candidate geometry:** assess geometric consistency before committing resources to expensive reference calculations.
- **Prepare targeted additions to training data:** provide cells representing environments encountered in the intended application, for subsequent reference labeling and model adaptation.

## Inputs and outputs

**Input:** atomistic structures or trajectories compatible with the Atomic Simulation Environment (ASE), including individual supercells and collections of frames.

**Output:** a set of smaller periodic cells suitable for DFT reference calculations. DFT evaluation and model fine-tuning are subsequent steps; ScaleDown provides the configurations they require.

## Application and outcomes

In the carbon-surface project, ScaleDown operated on large molecular-dynamics (MD) supercells describing C–N–H surfaces grown on graphite through bombardment with carbon, nitrogen and deuterium, with thermalization at different temperatures.

It extracted DFT-tractable cells from those supercells for reference calculations supporting foundation-model fine-tuning. The resulting potentials performed better for the studied surfaces than potentials trained exclusively using existing datasets, such as OMat24 and OMol25.

Some extracted cells also spontaneously reproduced the characteristic periodicity of the graphitic system. This result further supports ScaleDown’s ability to construct smaller periodic cells whose local atomic environments remain consistent with those of the parent structure.

[Portfolio](../../README.md) · [Code availability and release](../../README.md#availability)


<!-- project-metrics:start -->

## Development

| Metric | Value |
| --- | --- |
| Project languages | Python |
| Project code | 26,718 lines |
| Project files | 85 (including 12 notebooks) |
| Test code | 7,830 lines |
| Test files | 40 |
| External Python libraries | 17 detected (project + tests) |
| Commit history | 71 reachable commits on main |
| Last project-file change | 2026-06-23 (UTC) |
| Statistics collected | 2026-10-31 (UTC) |

<details>
<summary>Code breakdown & scope</summary>

| Component | Files | Code lines |
| --- | --- | --- |
| Package &amp; other source | 62 | 18,073 |
| Scripts &amp; benchmarks | 10 | 3,261 |
| Examples | 1 | 118 |
| Notebook code | 12 | 5,266 |
| Total project code | 85 | 26,718 |

Project code includes the package and other source files, scripts, examples and notebook code cells. Each file belongs to one component. Tests are counted separately.

Only tracked source files in the measured revision are counted. Documentation, repository automation, environments, caches, vendored code, configured output directories, data and other unselected formats are excluded. Notebook outputs and Markdown cells are excluded.

Code lines use cloc 2.10 and exclude blank lines and comments. Commit history includes every commit reachable from the measured default branch. The change date refers to currently included project files; comments and notebook output/Markdown changes can also change that date.

</details>

<details>
<summary>External Python libraries (17)</summary>

| Import name | Project files | Test files |
| --- | --- | --- |
| numpy | 54 | 35 |
| ase | 31 | 8 |
| matplotlib | 15 | 0 |
| joblib | 10 | 0 |
| pandas | 9 | 2 |
| scipy | 6 | 0 |
| threadpoolctl | 5 | 0 |
| skmatter | 4 | 0 |
| tqdm | 3 | 0 |
| sklearn | 2 | 2 |
| chemiscope | 2 | 0 |
| IPython | 2 | 0 |
| chgnet | 1 | 0 |
| featomic | 1 | 0 |
| mace | 1 | 0 |
| metatensor | 1 | 0 |
| pytest | 0 | 21 |

Each top-level import name counts once per file or notebook, including optional and type-checking imports. Standard-library and detected local modules are excluded. Dynamic imports, shell/magic commands and runtime changes to import paths are not resolved. This lists direct import presence, rather than installed or transitive dependencies or runtime usage.

</details>

*Test-code volume does not indicate test results or coverage.*

<!-- project-metrics:end -->
