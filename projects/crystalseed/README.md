# CrystalSeed

**Atomic structures and defects for simulation and dataset preparation.**

CrystalSeed prepares starting configurations for atomistic studies and interatomic-potential development. It covers a range of structural situations, from isolated atoms and clusters to bulk crystals, surfaces and materials containing defects.

## What the package can do

- **Prepare different types of atomic systems:** isolated configurations, periodic structures, bulk supercells and surface slabs.
- **Create structural variations:** generate related configurations with changes in strain or atomic positions to broaden the starting structures available for a study.
- **Introduce point defects:** prepare vacancies, substitutions and interstitials, including configurations containing combinations of defects.
- **Build surface configurations:** create surface defects and place atoms or molecules on surfaces for adsorption-related studies.
- **Prepare cavities and gas-containing structures:** construct configurations with voids or bubbles in bulk materials or slab environments.
- **Apply geometric requirements:** control structural characteristics and check consistency with the intended geometry and periodic boundaries before subsequent calculations.

These capabilities support the preparation of collections of structures covering the configurations relevant to a particular material or physical process.

## Inputs and outputs

The starting point is a chemical composition or host structure, together with the requested structural features. The output is a collection of atomic configurations accompanied by information about their generation.

The structures can then enter simulation, reference-labeling or potential-training workflows. CrystalSeed handles their preparation; those subsequent calculations are performed with the appropriate external tools.

## Application and outcome

CrystalSeed supplied the initial structures for an active-learning workflow developing a W–H–He potential to study helium-bubble growth in tungsten in the presence of deuterium.

These configurations provided the starting point for collecting structures for potential training. The subsequent active-learning campaign produced a highly accurate potential for the intended application, with CrystalSeed contributing the initial structural basis.

[Portfolio](../../README.md) · [Code availability and release](../../README.md#availability)

<!-- project-metrics:start -->

## Development

| Metric | Value |
| --- | --- |
| Project languages | Python |
| Project code | 9,210 lines |
| Project files | 51 |
| Test code | 2,574 lines |
| Test files | 16 |
| External Python libraries | 4 detected (project + tests) |
| Commit history | 4 reachable commits on main |
| Last project-file change | 2026-05-20 (UTC) |
| Statistics collected | 2026-10-31 (UTC) |

<details>
<summary>Code breakdown & scope</summary>

| Component | Files | Code lines |
| --- | --- | --- |
| Package &amp; other source | 32 | 8,529 |
| Examples | 19 | 681 |
| Total project code | 51 | 9,210 |

Project code includes the package and other source files, scripts, examples and notebook code cells. Each file belongs to one component. Tests are counted separately.

Only tracked source files in the measured revision are counted. Documentation, repository automation, environments, caches, vendored code, configured output directories, data and other unselected formats are excluded. Notebook outputs and Markdown cells are excluded.

Code lines use cloc 2.10 and exclude blank lines and comments. Commit history includes every commit reachable from the measured default branch. The change date refers to currently included project files; comments and notebook output/Markdown changes can also change that date.

</details>

<details>
<summary>External Python libraries (4)</summary>

| Import name | Project files | Test files |
| --- | --- | --- |
| ase | 32 | 14 |
| numpy | 17 | 8 |
| pymatgen | 4 | 0 |
| pytest | 0 | 14 |

Each top-level import name counts once per file or notebook, including optional and type-checking imports. Standard-library and detected local modules are excluded. Dynamic imports, shell/magic commands and runtime changes to import paths are not resolved. This lists direct import presence, rather than installed or transitive dependencies or runtime usage.

</details>

<!-- project-metrics:end -->
