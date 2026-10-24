# Dataset Schema Principles

This project treats circuit parameters as model/design inputs and simulated RF performance as outputs.

## Typical input variables

- bias voltage(s)
- HBT multiplier / effective device sizing
- RF choke inductance
- input matching inductance/capacitance
- output matching inductance/capacitance
- emitter degeneration inductance for relevant LNA topologies

## Typical response variables

Depending on topology and simulation stage:

- forward gain
- input/output matching quantities
- stability quantities
- noise figure and minimum noise figure
- output 1-dB compression point

Column names, units and extraction definitions should be frozen before a dataset version is published. Raw simulator quantities and intermediate files should not be treated as canonical labels until their extraction has been validated.
