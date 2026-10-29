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
