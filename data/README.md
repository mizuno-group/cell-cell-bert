# Dataset Description

This directory contains the datasets used for training (fine-tuning) and evaluating the Cell-Cell Relation Extraction models. The data is organized by source (`pubmed`, `semmed`) and split across multiple random seeds for robust experimentation.

## Directory Structure

The data is organized as follows:

```text
data/
├── pubmed/               # PubMed-based dataset (Evaluation)
│   ├── 22/               # Random Seed 22
│   │   └── test.csv
│   ├── 24/
│   ├── 42/
│   ├── 57/
│   └── 75/
└── semmed/               # SemMed-based dataset (Fine-tuning & Evaluation)
    ├── 22/
    │   ├── test.csv
    │   └── train.csv
    ├── ...
    └── 75/
```

## Dataset Usage

* SemMed/train.csv: Used for Fine-tuning the models (CPT or Supervised Fine-tuning).
* SemMed/test.csv: Used for evaluating the model on SemMed-derived samples.
* PubMed/test.csv: Used for evaluating the model on PubMed-derived samples (Generalization capability).