# Common-Emitter Power Amplifier (CE PA)

27 GHz single-HBT common-emitter power-amplifier branch using the IHP SG13G2 SiGe BiCMOS Open PDK.

## Design variables

The current design-space generation varies the transistor bias, HBT multiplier/device sizing, collector RF choke and input/output matching-network components while retaining the common-emitter topology.

## Characterization workflow

1. Verify the DC operating point.
2. Run small-signal simulation for S-parameters, gain, matching, noise quantities where recorded and stability checks.
3. Run large-signal harmonic-balance simulation.
4. Post-process the fundamental voltage/current quantities in Python to extract RF input/output power and output P1dB.
5. Record the validated parameter-performance pair in the topology dataset.

## Figures

The repository is prepared for the following validated figures:

- `figures/ce_pa_topology.png`
- `figures/ce_pa_small_signal.png`
- `figures/ce_pa_large_signal.png`

The figures are documentation views of the simulation setup rather than fabricated-silicon measurements.
