# PlifePred: In Silico Prediction of Peptide Half-Life in Blood

## Overview

PlifePred is a computational platform developed for predicting the half-life of natural and modified peptides in mammalian blood using machine learning and sequence/structure-based approaches.

The platform assists researchers in designing therapeutic peptides with improved stability and bioavailability.

The study developed prediction models using:

- Amino acid composition
- Dipeptide composition
- Binary profiles
- Atom composition
- PaDEL chemical descriptors

Machine learning methods were used to estimate peptide half-life directly from peptide sequences and structures.

Web Server:

http://webs.iiitd.edu.in/raghava/plifepred/

---

# Research Paper

## Title

In silico approaches for predicting the half-life of natural and modified peptides in blood

## Authors

- Deepika Mathur
- Sandeep Singh
- Ayesha Mehta
- Piyush Agrawal
- Gajendra P. S. Raghava

## Journal

PLOS ONE

## Published Date

01 June 2018

## DOI

https://doi.org/10.1371/journal.pone.0196829

## Source Paper

:contentReference[oaicite:0]{index=0}

---

# Background

Peptide therapeutics are increasingly important because of:

- High specificity
- Low toxicity
- Better tissue penetration
- Lower side effects

However, one major challenge is:

- Short half-life in blood due to enzymatic degradation

The half-life of peptides determines:

- Stability
- Bioavailability
- Dosing frequency
- Therapeutic efficacy

Experimental determination of peptide half-life is:

- Expensive
- Time-consuming
- Labor-intensive

PlifePred was developed to provide a fast computational alternative.

---

# Dataset Information

The peptide data was extracted from:

- PEPlife database

Initial collection:

- 1392 peptide entries

After filtering:

- Peptides length between 5–50 residues
- Half-life between 20 seconds and 24 hours

Final datasets:

## Modified Dataset

- 261 unique peptides
- Natural + modified residues

## Natural Dataset

- 163 natural peptides

Source: :contentReference[oaicite:1]{index=1}

---

# Feature Representation

The following input features were used:

## Amino Acid Composition

Represents frequency of amino acids in peptide sequences.

## Dipeptide Composition

Captures:

- Amino acid frequency
- Local sequence order

## Binary Profiles

Binary encoding of terminal residues:

- N-terminal residues
- C-terminal residues

## Atom Composition

Frequency of:

- C
- H
- O
- N
- S
- F
- Cl
- Br

## Chemical Descriptors

Generated using:

- PaDEL software

More than 15,000 descriptors were initially calculated.

Feature selection was performed using:

- CfsSubsetEval
- BestFirst algorithm

Source: :contentReference[oaicite:2]{index=2}

---

# Machine Learning Techniques

The following machine learning approaches were implemented:

- Support Vector Machine (SVM)
- SMOreg
- Linear Regression
- Gaussian Processes
- IBk (Instance-based learning)

Software used:

- SVM_light
- WEKA

Model evaluation was performed using:

- Leave-One-Out Cross Validation (LOOCV)

Source: :contentReference[oaicite:3]{index=3}

---

# Important Findings

The study observed that peptides with:

## Long Half-Life

Were enriched in:

- Glutamic acid (Glu)
- Alanine (Ala)
- Isoleucine (Ile)
- Leucine (Leu)

## Short Half-Life

Were enriched in:

- Tyrosine (Tyr)
- Phenylalanine (Phe)
- Glycine (Gly)
- Histidine (His)

Aromatic residues were associated with lower peptide stability.

Source: :contentReference[oaicite:4]{index=4}

---

# Performance on Natural Peptide Dataset

## Amino Acid Composition Model

| Feature | Correlation (R) |
|---|---|
| Amino Acid Composition | 0.643 |

## Dipeptide Composition Model

| Feature | Correlation (R) |
|---|---|
| Dipeptide Composition | 0.640 |

## Atom Composition Model

| Feature | Correlation (R) |
|---|---|
| Atom Composition | 0.532 |

Source: :contentReference[oaicite:5]{index=5}

---

# Best Structure-Based Model

Using:

- 45 selected PaDEL descriptors

## Best Performance

| Method | Correlation (R) |
|---|---|
| SMOreg | 0.743 |

Additional metrics:

- MAE: 1.369
- RMSE: 1.932

Source: :contentReference[oaicite:6]{index=6}

---

# Performance on Modified Dataset

Using:

- 43 selected PaDEL descriptors

## Best Model

| Method | Correlation (R) |
|---|---|
| SVM | 0.692 |

Additional metrics:

- MAE: 1.564
- RMSE: 2.075

Source: :contentReference[oaicite:7]{index=7}

---

# Workflow

The workflow included:

1. Dataset extraction from PEPlife
2. Dataset filtering
3. Feature extraction
4. Machine learning model development
5. LOOCV validation
6. Web server implementation

The workflow diagram is shown on page 3 of the paper. :contentReference[oaicite:8]{index=8}

---

# Web Server Features

PlifePred contains two major modules:

## Natural Peptide Module

### Sequence-Based Prediction

- Analog Generation
- Batch Submission
- Protein Scan

### Structure-Based Prediction

- Draw Module
- File Upload Module

## Modified Peptide Module

Allows prediction for:

- Modified residues
- Chemically modified peptides
- Non-natural amino acids

Users can:

- Predict peptide half-life
- Generate mutants
- Design stable analogs
- Analyze physicochemical properties

Web Server:

http://webs.iiitd.edu.in/raghava/plifepred/

Source: :contentReference[oaicite:9]{index=9}

---

# Technologies Used

- SVM_light
- WEKA
- PaDEL Descriptor
- PHP
- Perl
- HTML
- Machine Learning Algorithms

---

# Applications

PlifePred can be used for:

- Therapeutic peptide design
- Peptide engineering
- Drug discovery
- Stability prediction
- Rational peptide modification
- Pharmacokinetics research

---

# Conclusion

The study demonstrated that:

- Chemical descriptors significantly improve prediction accuracy
- Structure-based models outperform sequence-only models
- Peptide composition strongly influences stability
- Machine learning can effectively predict peptide half-life

PlifePred provides a useful platform for rational design of stable therapeutic peptides.

---

# Contact

## Dr. G. P. S. Raghava

Email: raghava@iiitd.ac.in

Address:  
Indraprastha Institute of Information Technology Delhi

---

# License

Creative Commons Attribution License (CC BY)

---
