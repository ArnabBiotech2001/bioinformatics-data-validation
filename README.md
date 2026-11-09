# Genomic Dataset Validation Workflow

A lightweight, automated Python pipeline designed to perform structural integrity checks and pre-processing steps on genomic expression matrices and sample metadata sheets prior to downstream NGS analytics (e.g., Differential Gene Expression analysis).

## 🧬 Overview
Before running resource-intensive NGS alignment or differential expression pipelines, ensuring the structural cleanliness of the input metadata and matrix boundaries is critical. This project serves as a diagnostic validation step utilizing NumPy and Pandas to catch empty tracks and verify phenotypic groupings.

## 🛠️ Tech Stack & Dependencies
* **Language:** Python 3.15+
* **Libraries:** NumPy (v2.5.4), Pandas (v3.1.1)
* **Environment:** Visual Studio Code (VS Code)

## 📊 Core Features Implemented
* **Zero-Expression Filter:** Uses NumPy vector filtering to isolate and count active gene expression tracks while removing dropouts.
* **Metadata Profiling:** Implements structured Pandas DataFrames to structurally view and audit sample identities alongside phenotypic categorizations (`Tumor` vs `Normal`).

## 🚀 Execution & Verification
To verify the local workspace configurations and run the validation matrix script, execute the following command in your terminal:

```bash
python dataset_validation.py
```

### Expected Diagnostic Output
```text
--- Data Science Validation Check ---
Total non-zero data tracks found: 4

Metadata structural view:
  Sample_ID Phenotype
0    SRR001     Tumor
1    SRR002    Normal
2    SRR003     Tumor

Validation Complete: Setup is ready for raw datasets!
```
