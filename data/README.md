# Dataset Organization

Each RF topology has its own dataset directory. A dataset row should represent one physical circuit configuration and its validated simulation response.

```text
circuit parameters -> simulation / post-processing -> RF performance labels -> dataset row
```

## Canonical filenames

- `ce_pa/ce_pa_dataset.csv`
- `cascode_pa/cascode_pa_dataset.csv`
- `ce_lna/ce_lna_dataset.csv`
- `cascode_lna/cascode_lna_dataset.csv`

## Data-management rules

- Keep one curated canonical table per topology.
- Use stable column names and explicit units.
- Keep raw simulator exports separate from curated datasets.
- Record only simulations that pass the relevant DC, stability and extraction checks.
- Do not mix intermediate or known-invalid runs into the published dataset.
- Version schema changes explicitly as the project grows.

The public dataset will be added progressively after validation and cleanup.
