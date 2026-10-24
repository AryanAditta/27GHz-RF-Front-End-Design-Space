# 27 GHz RF Front-End Design Space

Design-space generation and simulation-based characterization of 27 GHz SiGe RF amplifier topologies using the IHP SG13G2 open PDK.

## Project scope

This repository documents a growing RF front-end design-space study across four circuit families:

| Circuit family | Role | Current status |
|---|---|---|
| Common-Emitter PA | Transmitter / power amplifier | Dataset generation in progress |
| Cascode PA | Transmitter / power amplifier | Initial dataset batch completed |
| Common-Emitter LNA | Receiver / low-noise amplifier | Design and dataset expansion in progress |
| Cascode LNA | Receiver / low-noise amplifier | Planned extension |

The workflow varies circuit-level design parameters such as bias, transistor sizing, RF choke values and matching-network components, then records RF performance obtained from simulation. A structured input-output dataset is being generated privately to support later analysis, surrogate modeling and design-space exploration.

## Technology and tools

- **Technology:** IHP SG13G2 130 nm SiGe BiCMOS Open PDK
- **Design frequency:** 27 GHz
- **Schematic environment:** Qucs-S
- **Small-signal / noise simulation:** ngspice
- **Large-signal / harmonic-balance simulation:** Xyce
- **Post-processing:** Python
- **Dataset tracking:** private tabular design-parameter / performance records

## Repository structure

```text
.
├── circuits/
│   ├── ce_pa/
│   │   └── figures/
│   ├── cascode_pa/
│   │   └── figures/
│   ├── ce_lna/
│   │   └── figures/
│   └── cascode_lna/
│       └── figures/
├── data/
│   └── README.md
├── scripts/
├── docs/
└── README.md
```

## Circuit families

### Common-Emitter PA
Single-HBT common-emitter power-amplifier topology with parameterized bias, device multiplier, collector RF choke and input/output matching networks.

![CE PA topology](circuits/ce_pa/figures/ce_pa_topology.png)

### Cascode PA
Stacked common-emitter/common-base SiGe HBT power-amplifier topology, allowing independent device sizing and bias exploration together with matching-network and RF-choke variation.

![Cascode PA topology](circuits/cascode_pa/figures/cascode_pa_topology.png)

### Common-Emitter LNA
Low-noise common-emitter topology with emitter degeneration and simultaneous gain/noise/stability-oriented matching. Dataset expansion is ongoing.

### Cascode LNA
Planned low-noise cascode extension for comparative front-end design-space generation.

## Dataset concept

Each private dataset sample corresponds to one circuit configuration:

```text
circuit parameters
      ↓
DC / small-signal / noise / large-signal simulation
      ↓
RF performance metrics
      ↓
structured dataset row
```

Typical input variables include bias voltages, transistor multipliers, RF-choke values and matching-network components. Typical response variables include gain, noise metrics, stability/matching quantities and output 1-dB compression behavior, depending on topology.

The underlying dataset is **not publicly released in this repository**. Public materials are limited to selected circuit schematics, workflow documentation, figures and non-sensitive analysis code where appropriate.

## Current development status

The PA branches are currently the most mature. The LNA branches are being added progressively, with CE LNA preceding the cascode-LNA extension. Public documentation and reproducible post-processing material will be added as the validation workflow is finalized.

## Notes

This repository documents simulation-based research and design-space generation. Reported circuit behavior should not be interpreted as fabricated or measured-silicon performance unless explicitly stated otherwise.

## Author

**Arian Rahman Aditta**  
B.Sc. in Electronics and Communication Engineering, KUET  
Research interests: RF/mmWave IC design, analog/RF ICs, VLSI/EDA and ML-assisted hardware design
