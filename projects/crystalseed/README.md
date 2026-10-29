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
