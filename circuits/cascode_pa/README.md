# Cascode Power Amplifier (Cascode PA)

27 GHz SiGe HBT cascode power-amplifier branch using a stacked common-emitter/common-base device arrangement in the **IHP SG13G2 Open PDK**.

This branch extends the PA design space beyond the single-transistor common-emitter case by introducing independent bias and sizing choices for the lower and upper HBTs. The public repository documents the topology and analysis workflow while the numerical dataset remains private.

## Design variables

The design space includes lower- and upper-device bias settings, separate transistor multipliers, collector RF choke and input/output matching-network component values.

## Characterization workflow

1. Verify the DC operating points of both stacked HBTs.
2. Run small-signal analysis for S-parameters, forward gain, input/output matching, noise quantities where required and stability.
3. Re-check the effect of the matching networks at the 27 GHz design frequency.
4. Run large-signal harmonic-balance simulation over the RF drive sweep.
5. Post-process fundamental voltage/current quantities in Python to determine RF power and compression behavior.
6. Retain only validated parameter-response pairs in the private topology dataset.

## Circuit topology

The schematic below shows the stacked common-emitter/common-base cascode skeleton used for the parameterized PA designs.

![Cascode PA skeleton](figures/Cascode%20PA%20Skeleton.png)

## Small-signal analysis setup

The small-signal testbench is used for gain, S-parameter, matching, noise and stability characterization around the design frequency.

![Cascode PA small-signal analysis](figures/Small%20Signal%20Analysis.png)

## Large-signal analysis setup

The large-signal testbench supports harmonic-balance drive sweeps and subsequent Python-based power/compression extraction.

![Cascode PA large-signal analysis](figures/Large%20Signal%20Analysis.png)

## Current status

An initial baseline batch of parameterized cascode-PA designs has been completed and is being used as part of the wider RF front-end design-space study.

## Data policy

The corresponding parameter-performance table is **private research data** and is not publicly released in this repository.

> All material shown here is simulation-based and should not be interpreted as fabricated- or measured-silicon performance.
