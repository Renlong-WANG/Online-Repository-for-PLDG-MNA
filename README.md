# PLDG-MNA Input Data

Input data for the Port R scenario used in:

> *Assessing and Optimizing Operational Data Governance Capacity in Port
> Logistics: A Collaboration-Based Meta-Network Approach*

This repository contains only the input node dictionary and the seven binary
subnetwork matrices. Port R is an anonymized, reference-informed illustrative
scenario abstracted from a real-port workflow; it is not an observed empirical
network.

## Contents

```text
data/
├── nodes.csv
└── subnetworks/
    ├── AA.csv
    ├── AD.csv
    ├── AO.csv
    ├── AP.csv
    ├── DO.csv
    ├── DP.csv
    └── PP.csv
```

- `nodes.csv` lists 13 agents, 8 organizations, 16 data items, and 15
  processes.
- Each subnetwork CSV has node IDs in the first row and first column.
- Matrix entries are binary: `1` means that the relation was identified in the
  scenario; `0` means that it was not identified.
- `AA` is symmetric. `PP` is directed from an immediately preceding process to
  its successor.
- The diagonal ones in `AA` and `PP` are ORA identity markers. They are retained
  to preserve the original input and should be excluded from substantive
  interpretation.

See [data/README.md](data/README.md) for matrix meanings and dimensions.

