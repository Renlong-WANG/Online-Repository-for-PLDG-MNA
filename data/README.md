# Data dictionary

## Node table

`nodes.csv` uses four columns:

| Column | Meaning |
|---|---|
| `node_type` | `agent`, `organization`, `data`, or `process` |
| `node_id` | Stable identifier used in all matrices |
| `label_en` | English node label used in the manuscript
 

## Subnetwork tables

| File | Rows × columns | Relation encoded by `1` |
|---|---:|---|
| `AA.csv` | 13 agents × 13 agents | Operational collaboration |
| `AD.csv` | 13 agents × 16 data items | Actual data access |
| `AO.csv` | 13 agents × 8 organizations | Institutional affiliation |
| `AP.csv` | 13 agents × 15 processes | Process responsibility |
| `DO.csv` | 16 data items × 8 organizations | Data ownership or maintenance responsibility |
| `DP.csv` | 16 data items × 15 processes | Data required by a process |
| `PP.csv` | 15 processes × 15 processes | Immediate process precedence |

All files are UTF-8 CSV with comma delimiters. Zeros represent relations not
identified within the scenario evidence; they should not automatically be
interpreted as proof that a relation cannot exist outside the scenario boundary.
