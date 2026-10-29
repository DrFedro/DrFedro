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
