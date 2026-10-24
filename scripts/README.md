# Reproducible Scripts

Post-processing and dataset-generation utilities will be organized here as the workflow is consolidated.

Suggested structure:

```text
scripts/
├── power/       # Fourier-domain Pin/Pout and OP1dB extraction
├── noise/       # NF/NFmin and noise/gain-circle processing
├── validation/  # schema, missing-value and engineering sanity checks
└── plots/       # dataset / repository figures
```

Scripts added here should operate on documented inputs and produce reproducible outputs rather than relying on manually edited intermediate files.
