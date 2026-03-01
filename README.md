🧠 AI-Driven Digital Twin for Mutation-Based Targeted Therapy Response Prediction in Glioblastoma

🔬 Project Overview

This repository presents an interpretable Artificial Intelligence–driven Digital Twin framework for predicting targeted therapy response in Glioblastoma (GBM) using somatic genomic mutation signatures and pathway-informed modeling.
The framework models tumor-specific mutation landscapes to simulate therapeutic response behavior and estimate sensitivity to the MEK inhibitor Trametinib.
This project demonstrates how mutation-driven computational modeling can contribute to clinically interpretable precision oncology systems.


🎯 Clinical Motivation

. Glioblastoma is characterized by:
. Extensive genomic heterogeneity
. Rapid therapeutic resistance
. Variable response to targeted therapies
. Limited predictive reliability of single-gene biomarkers

Clinical decision-making in GBM often lacks combinatorial mutation-level predictive modeling.
This project addresses that gap using a sparse, interpretable Digital Twin approach capable of modeling multi-gene mutation signatures.


🗂 Data

This study integrates publicly available genomic and pharmacogenomic datasets:
. Somatic mutation profiles from The Cancer Genome Atlas (TCGA)
. GBM cohort: PanCancer Atlas (cBioPortal release)
. Drug response data (IC50 values) aligned to Trametinib sensitivity
. Due to GitHub file size limitations, raw molecular datasets are not included in this repository.


🔗 Dataset Access

TCGA GBM PanCancer Atlas dataset can be accessed via:

https://www.cbioportal.org/study/summary?id=gbm_tcga_pan_can_atlas_2018

All preprocessing steps are documented and reproducible using the provided notebook.


🧬 Methodological Framework

1. Data Processing
. Binary encoding of somatic mutation profiles
. Integration of pharmacogenomic IC50 response values
. Dichotomization into Sensitive vs Resistant classes

2. Modeling Strategy
. Sparse Logistic Regression (L1 Regularization)
. Embedded feature selection
. Coefficient-based interpretability
. Dimensionality control to mitigate overfitting

3.Validation & Robustness
. Repeated 5-Fold Cross-Validation
. Receiver Operating Characteristic (ROC) analysis
. Mean Area Under the Curve (AUC) computation
. Standard deviation assessment for stability
. Feature selection frequency tracking across folds


📊 Model Performance

Metric	Value
Mean Cross-Validated AUC	0.76
AUC Standard Deviation	± 0.18
Model Type	Sparse Logistic Regression
Validation Strategy	Repeated 5-Fold Cross-Validation

Interpretation

. Demonstrates moderate discriminative capability using mutation-only features
. Captures biologically meaningful predictive signal
. Variability reflects tumor heterogeneity and dataset scale
. Sparse regularization enhances generalizability and interpretability


🧪 Stable Genomic Determinants Identified

Consistently selected predictors across validation folds:
TP53
PTEN
RB1
NF1
These genes are mechanistically associated with tumor suppressor regulation and MAPK/PI3K pathway activity, supporting biological plausibility of model outputs.


🏥 Translational Applications

1️⃣ Clinical Decision Support Systems (CDSS)
. Mutation-informed therapy prioritization
. Molecular tumor board support
. Probabilistic sensitivity estimation

2️⃣ Precision Oncology Platforms
. Integration with hospital genomic sequencing workflows
. AI-assisted stratification of patient subgroups
. Mutation-driven therapy modeling

3️⃣ Pharmaceutical & Drug Development
. Preclinical mutation-response modeling
. Identification of genomically defined responder subpopulations
. Simulation-based hypothesis generation

4️⃣ Digital Twin Expansion
. Multi-omics integration (transcriptomics, CNV, methylation)
. Pathway-level perturbation modeling
. Tumor evolution simulation frameworks


🧠 Clinical Relevance
✔ Interpretable non–black-box architecture
✔ Mutation-grounded biological rationale
✔ Embedded feature selection
✔ Cross-validated evaluation
✔ Reproducible computational workflow
✔ Scalable for translational integration

Transparent modeling is essential for clinical AI adoption; this framework prioritizes interpretability and biological plausibility.


🛠 Technology Stack

1. Python
2. NumPy
3. Pandas
4. Scikit-learn
5. Matplotlib
6. Seaborn
7. Jupyter Notebook

Extensible for:

FastAPI / Flask deployment

Docker containerization

Cloud-based inference services


📁 Repository Structure

GBM-Digital-Twin-Drug-Response/
│
├── data/                  # Processed mutation & response datasets
├── notebooks/             # End-to-end modeling workflow
├── src/                   # Modular ML scripts
├── results/               # ROC curves and outputs
├── requirements.txt
└── README.md


🔁 Reproducibility

. Fixed random seeds

. No data leakage

. Clear train/validation separation

. Modular preprocessing

. Fully executable notebook

To Reproduce:
pip install -r requirements.txt
jupyter notebook notebooks/GBM_Digital_Twin_Model.ipynb


🚀 Future Directions

. External validation cohorts

. Multi-omics feature integration

. Probability calibration

. Prospective translational evaluation

. REST API deployment

. Regulatory-aligned explainability frameworks


🌍 Impact Statement

This work demonstrates the feasibility of constructing an interpretable AI-driven Digital Twin for mutation-based targeted therapy response prediction in glioblastoma.

While predictive performance remains moderate, the framework provides a biologically grounded and scalable foundation for precision oncology modeling and clinical decision support research.


👩‍🔬 Author

Sofiya Chavarekar
School of Biosciences Engineering and Technology
VIT Bhopal University


📜 License

MIT License — Open for academic and research use.
