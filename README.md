# PLDG-MNA Data Repository

Data accompanying the Port R scenario presented in:

> *Assessing and Optimizing Operational Data Governance Capacity in Port
> Logistics: A Collaboration-Based Meta-Network Approach*

The repository contains the baseline meta-network data and the reported
agent-data access changes from the selected optimized configuration. Port R is
an anonymized, reference-informed illustrative scenario abstracted from a
real-port workflow; it is not an observed empirical network.

## Repository contents

```text
data/
|-- nodes.csv
|-- network optimization results.xlsx
|-- README.md
`-- subnetworks/
    |-- AA.csv
    |-- AD.csv
    |-- AO.csv
    |-- AP.csv
    |-- DO.csv
    |-- DP.csv
    `-- PP.csv
```

- `nodes.csv` provides the English labels and stable IDs for 13 agents,
  8 organizations, 16 data items, and 15 processes.
- `subnetworks/` contains the seven binary matrices used as the baseline
  PLDG meta-network.
- `network optimization results.xlsx` lists the data-access additions and
  removals associated with the selected optimized agent-data configuration.

## Data conventions

- Each subnetwork CSV uses node IDs in its first row and first column.
- Matrix entries are binary: `1` means that the relation was identified in the
  scenario, and `0` means that it was not identified.
- `AA` is symmetric. `PP` is directed from an immediately preceding process to
  its successor.
- Diagonal ones in `AA` and `PP` are ORA identity markers retained from the
  source network. They should be excluded from substantive interpretation.
- In `network optimization results.xlsx`, comma-separated data IDs denote
  access relations to add or remove, while `--` denotes no change.

See [data/README.md](data/README.md) for the detailed data dictionary.
