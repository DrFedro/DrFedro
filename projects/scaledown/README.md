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

It extracted DFT-tractable cells from those supercells for reference calculations supporting foundation-model fine-tuning. The resulting potentials performed better for the studied surfaces than potentials trained exclusively using existing datasets, such as OMat and OMol.

Some extracted cells also spontaneously reproduced the characteristic periodicity of the graphitic system. This result further supports ScaleDown’s ability to construct smaller periodic cells whose local atomic environments remain consistent with those of the parent structure.

[Portfolio](../../README.md) · [Code availability and release](../../README.md#availability)
