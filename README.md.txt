🧠 AI-Driven Digital Twin for Mutation-Based Targeted Therapy Response Prediction in Glioblastoma


🔬 Project Overview

This repository presents an interpretable Artificial Intelligence–driven Digital Twin framework designed to predict targeted therapy response in
Glioblastoma multiforme (GBM) using somatic genomic mutation signatures and pathway-informed modeling.

The framework models tumor-specific mutation landscapes to simulate therapeutic response behavior and estimate sensitivity to the MEK inhibitor
Trametinib.

This project demonstrates how mutation-driven computational modeling can contribute to real-world precision oncology systems while maintaining clinical interpretability.


🎯 Clinical Motivation

Glioblastoma is characterized by:

Extensive genomic heterogeneity

Rapid therapeutic resistance

Variable response to targeted therapies

Limited predictive reliability of single-gene biomarkers

Clinical decision-making in GBM often lacks combinatorial mutation-level predictive modeling.
This project addresses that gap through an interpretable Digital Twin approach capable of modeling multi-gene mutation signatures.


🧬 Methodological Framework

Data Processing:

Binary encoding of somatic mutation profiles

Integration of pharmacogenomic IC50 response values

Dichotomization into Sensitive vs Resistant classes


Modeling Strategy:

Sparse Logistic Regression (L1 Regularization)

Embedded feature selection

Coefficient-based interpretability

Dimensionality reduction to mitigate overfitting


Validation & Robustness:

Repeated 5-Fold Cross-Validation

Receiver Operating Characteristic (ROC) analysis

Mean Area Under the Curve (AUC) computation

Standard deviation assessment for stability

Feature selection frequency tracking across folds


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

These genes are mechanistically associated with tumor suppressor regulation and MAPK/PI3K pathway activity, supporting biological plausibility of the model outputs.


🏥 Real-World Applications

This framework is extensible to several translational contexts:


1️⃣ Clinical Decision Support Systems (CDSS)

Mutation-informed therapy prioritization

Support for molecular tumor board evaluation

Probabilistic sensitivity estimation for targeted agents


2️⃣ Precision Oncology Platforms

Integration with hospital genomic sequencing pipelines

AI-assisted stratification of patient subgroups

Personalized mutation-driven therapy modeling


3️⃣ Pharmaceutical & Drug Development Pipelines

Preclinical mutation-response modeling

Identification of genomically defined responder subpopulations

Simulation-based hypothesis generation for targeted therapy trials


4️⃣ Digital Twin Expansion

Multi-omics integration (transcriptomics, CNV, methylation)

Pathway-level perturbation modeling

Tumor evolution simulation frameworks


🧠 Why This Approach Is Clinically Relevant

✔ Interpretable modeling (non–black-box architecture)
✔ Mutation-grounded biological rationale
✔ Embedded feature selection
✔ Cross-validated performance evaluation
✔ Reproducible computational pipeline
✔ Scalable for real-world integration

Clinical adoption of AI systems requires transparency and interpretability; this framework is designed with that principle at its core.


🛠 Technology Stack

Python

NumPy

Pandas

Scikit-learn

Matplotlib

Seaborn

Jupyter Notebook

The architecture is modular and extendable for:

API deployment (FastAPI/Flask)

Docker containerization

Cloud-based inference services


📁 Repository Structure
GBM-Digital-Twin-Drug-Response/
│
├── data/                  # Processed mutation & drug response datasets
├── notebooks/             # End-to-end modeling workflow
├── src/                   # Modular machine learning scripts
├── results/               # ROC curves and performance outputs
├── requirements.txt
└── README.md


🔁 Reproducibility

Fixed random seeds

Clear train/validation separation

No data leakage

Modular preprocessing pipeline

Fully executable notebook

To reproduce:

pip install -r requirements.txt
jupyter notebook notebooks/GBM_Digital_Twin_Model.ipynb


🚀 Future Directions

External dataset validation

Multi-omics feature integration

Calibration of predicted probabilities

Prospective translational validation

Deployment-ready REST API

Regulatory-aligned interpretability enhancements



🌍 Impact Statement

This work illustrates the feasibility of constructing an interpretable AI-driven Digital Twin for mutation-based targeted therapy prediction in glioblastoma.

While predictive performance remains moderate, the framework provides a scalable and biologically grounded foundation for precision oncology modeling and clinical decision support development.


👩‍🔬 Author

Sofiya Chavarekar
School of Biosciences Engineering and Technology
VIT Bhopal University


📜 License

MIT License — Open for academic and research use.