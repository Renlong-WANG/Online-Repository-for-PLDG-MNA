# Data Dictionary

## Node table

`nodes.csv` contains 52 nodes:

| Node set | IDs | Count |
|---|---|---:|
| Process | `P1`-`P15` | 15 |
| Agent | `A1`-`A13` | 13 |
| Data | `D1`-`D16` | 16 |
| Organization | `O1`-`O8` | 8 |

The file uses three columns:

| Column | Meaning |
|---|---|
| `node_type` | Node-set heading: process, agent, data, or organization |
| `node_id` | Stable identifier used in the subnetwork matrices and optimization results |
| `label_en` | English node label used in the study |

Within each node-set block, `node_type` is shown on the first row and blank
cells inherit the most recent nonblank node type.

## Baseline subnetwork tables

| File | Dimensions | Relation encoded by `1` |
|---|---:|---|
| `AA.csv` | 13 agents x 13 agents | Operational collaboration |
| `AD.csv` | 13 agents x 16 data items | Actual data access |
| `AO.csv` | 13 agents x 8 organizations | Institutional affiliation |
| `AP.csv` | 13 agents x 15 processes | Process responsibility |
| `DO.csv` | 16 data items x 8 organizations | Data ownership or maintenance responsibility |
| `DP.csv` | 16 data items x 15 processes | Data required by a process |
| `PP.csv` | 15 processes x 15 processes | Immediate process precedence |

All subnetwork files are UTF-8, comma-delimited CSV files. Zeros represent
relations not identified within the scenario evidence; they should not be
interpreted automatically as proof that a relation cannot exist outside the
scenario boundary.

## Network optimization results

`network optimization results.xlsx` reports the changes to the agent-data
access layer (`AD`) in the selected optimized configuration. The other six
subnetworks remain fixed.

The workbook contains one worksheet, `Sheet1`, with three columns:

| Column | Meaning |
|---|---|
| `Node ID` | Agent identifier |
| `Added data` | Data IDs for which access is added |
| `Reduced data` | Data IDs for which existing access is removed |

Multiple data IDs are comma-separated. `--` indicates that no access relation
is added or removed for that entry. This workbook is an optimization result,
not an additional baseline subnetwork.
