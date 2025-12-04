# This directory contains processed data generated for validation and high-throughput screening (HTS) tasks, specifically for the JaCVAM tests listed below.

The data is provided in two tab-separated (.tsv) files that contain Chemical Abstracts Service (CAS) numbers, toxicity severity information, and chemical descriptors.

| JaCVAM Test Number | JaCVAM Test Name | Number of Compounds (Validation Test) | Number of Compounds (HTS Test) |
| ---- | ---- | ---- | ---- |
| 07_acute toxicity | 01_Cytotoxicity Testing | 72 | 7111 |
| 07_acute toxicity | 02_Cytotoxicity Testing |	56 | 7099 |
| 09_endocrine_disruptors | 01_VM7 Luc ER TA assay | 42 (agonist) 25 (antagonist) | 6779 (agonist) 6778 (antagonist) |
| 09_endocrine_disruptors	| 02_ER-STTA assay | 86 (agonist) 21 (antagonist) | 6810 (agonist) 6781 (antagonist) |
| 09_endocrine_disruptors	| 04_AR-Ecoscreen |	10 (agonist) 10 (antagonist) | 6782 (agonist) 6780 (antagonist) |
| 09_endocrine_disruptors	| 05_AR-CALUX	| 11 (agonist) 9 (antagonist) | 6777 (agonist) 6777 (antagonist) |
| 09_endocrine_disruptors	| 07_hrER in vitro study |	36 | 6782 |
| 10_Developmental Toxicity Prediction Test | 01_Embryonic Stem Cell Technology (EST) | 18 | 456 |
| 10_Developmental Toxicity Prediction Test |	02_Hand1-Luc EST | 16 | 451 |

## Data Files

- `all_data.tsv`: Contains CAS numbers, severity information, and chemical descriptors (CanonicalSmiles, xlogp, tpsa) for all compounds in both the HTS and validation sets. If descriptor data is unavailable, placeholder values (`###`) are used.
- `validation_data.tsv`: Contains CAS numbers, severity, and chemical descriptors for compounds in the validation set. If descriptor data is unavailable, original validation values are retained.

All files are tab-separated and include the following columns:
- `CAS`: Chemical Abstracts Service Registry Number
- `severity`: Toxicity severity information
- `CanonicalSmiles`: Canonical SMILES string (if available)
- `xlogp`: Predicted logP value (if available)
- `tpsa`: Topological Polar Surface Area (if available)

These files support downstream data validation and HTS analyses.
