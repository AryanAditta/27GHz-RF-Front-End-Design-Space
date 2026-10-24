# Project Workflow

The repository is organized around a common characterization loop for each 27 GHz RF amplifier topology.

1. Select a topology and parameter configuration.
2. Set bias voltages, device sizing, RF choke and matching-network values.
3. Verify the DC operating point.
4. Run small-signal RF characterization.
5. Check matching and stability; for LNAs also evaluate noise-optimum behavior.
6. Perform or refine input/output matching.
7. Run large-signal harmonic-balance characterization where required.
8. Post-process exported quantities in Python for metrics such as output P1dB.
9. Record the validated input/output pair in the canonical topology dataset.
10. Repeat systematically across the design space.

The long-term objective is to use the resulting validated dataset for quantitative design-space analysis, surrogate modeling and eventually software-assisted RF design exploration.
