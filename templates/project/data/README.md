# Project Data

Research datasets are stored outside the Git repository.

The default external location is:

`RESEARCH_DATA_ROOT/<PROJECT_ID>/`

Expected external structure:

raw/
intermediate/
external/
generated/

## Rules

- `raw/` contains immutable original/source data.
- `intermediate/` contains cleaned, merged, or transformed data that may be expensive to recreate.
- `external/` contains supplementary data obtained from external sources.
- `generated/` contains temporary or easily reproducible data products.

Large datasets should not be copied into this Git repository.

Project code should locate the external data directory through `RESEARCH_DATA_ROOT` rather than hard-coded Mac or Windows paths.

Confidential or restricted data may require a different storage arrangement defined by the individual project.