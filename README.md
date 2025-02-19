# Related Knowledge Perturbation Matters

This repository includes the data and python implementation for the paper "Related Knowledge Perturbation Matters: Rethinking Multiple Pieces of Knowledge Editing in Same-Subject." (Accepted by NAACL 2025 Main Conference).

[![arXiv](https://img.shields.io/badge/arXiv-paper-b31b1b.svg)](https://arxiv.org/abs/2502.06868)

<div align="center">
    <img src="./pic/demo.png" alt="Pipeline Diagram" width=50%; height=50%;">
</div>
## DataSet
Our dataset is located in `S2RKE.json`. Compared to the dataset COUTERFACT, the knowledge density surrounding the same topic is higher.

| Item | S2RKE| COUNTERFACT |
|------|---------|---------|
| Records | 22064 | 21919 |
| Subjects | 4503 | 20391 |
| Relations | 43 | 32 |
| Maximum records per subject | 13 | 4 |
| Minimum records per subject | 3 | 1 |
| Average records per subject | 4.9 | 1.1 |
## Model Preparation
