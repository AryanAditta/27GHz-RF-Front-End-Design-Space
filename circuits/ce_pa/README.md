# Common-Emitter Power Amplifier (CE PA)

27 GHz single-HBT common-emitter power-amplifier branch implemented with the **IHP SG13G2 SiGe BiCMOS Open PDK**.

This branch is used for systematic circuit-level design-space generation rather than presentation of one optimized operating point. The public repository shows the topology and simulation workflow; the numerical dataset remains private.

## Design variables

The design space varies the HBT bias condition, device multiplier, collector RF choke and input/output matching-network components while retaining the common-emitter topology.

## Characterization workflow

1. Verify the DC operating point and active-device bias condition.
2. Run small-signal analysis for S-parameters, forward gain, input/output matching, noise quantities where required and stability.
3. Verify the matching networks around the 27 GHz design frequency.
4. Run large-signal harmonic-balance simulation over the RF drive sweep.
5. Post-process the fundamental voltage/current quantities in Python to determine RF input/output power and compression behavior.
6. Retain only validated parameter-response pairs in the private topology dataset.

## Circuit topology

The schematic below shows the common-emitter PA skeleton used as the basis for parameterized designs.

![Common-Emitter PA skeleton](figures/Common%20Emitter%20Skeleton.png)

## Small-signal analysis setup

The small-signal environment is used for RF gain, S-parameter, matching, noise and stability characterization around the design frequency.

![Common-Emitter PA small-signal analysis](figures/Common%20Emitter%20Small%20Signal%20Analysis.png)

## Large-signal analysis setup

The large-signal testbench drives the PA through harmonic-balance simulation. Fundamental voltage/current quantities are subsequently processed in Python for power and compression extraction.

![Common-Emitter PA large-signal analysis](figures/CE%20Large%20Signal%20Analysis.png)

## Data policy

The corresponding design-space table contains circuit parameters and validated RF responses, but the numerical dataset is **not publicly released** in this repository.

> All material shown here is simulation-based and should not be interpreted as fabricated- or measured-silicon performance.
