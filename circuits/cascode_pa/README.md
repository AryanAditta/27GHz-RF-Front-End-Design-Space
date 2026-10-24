# Cascode Power Amplifier (Cascode PA)

27 GHz SiGe HBT cascode power-amplifier branch using a stacked common-emitter/common-base device arrangement in the IHP SG13G2 Open PDK.

## Design variables

The design space includes independent lower- and upper-device bias settings, separate transistor multipliers, collector RF choke and input/output matching-network component values.

## Characterization workflow

1. Verify DC operating points for both stacked HBTs.
2. Run small-signal S-parameter, gain, matching and stability analysis.
3. Characterize noise quantities where required by the dataset.
4. Run large-signal harmonic-balance simulation and Python-based power/compression extraction.
5. Store each validated circuit configuration as a structured dataset row.

## Figures

The repository is prepared for:

- `figures/cascode_pa_topology.png`
- `figures/cascode_pa_small_signal.png`
- `figures/cascode_pa_large_signal.png`

This branch currently has the first completed baseline batch of parameterized designs.
