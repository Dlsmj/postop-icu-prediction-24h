# postop-icu-prediction-24h

# Postoperative ICU Admission Risk Prediction Using INSPIRE and MOVER
This project is based on two electronic health record (EHR) datasets—INSPIRE and MOVER—and uses EHR data from the 7 days prior to surgery to predict the risk of ICU admission within 24 hours after surgery. The goal is to build a high-performance machine learning algorithm to provide early warning support for perioperative management.

# Reproducibility Note
The code used in this project includes steps where certain features had to be generated via Large Language Model (LLM) inference, as diagnoses and surgical procedures in MOVER are stored as free-text narratives. Although we set temperature=0 and performed inference three times to minimize randomness, due to the inherent non-deterministic behavior of LLMs, the final inferred results may exhibit minor fluctuations. Therefore, 100% perfect reproducibility of all intermediate features cannot be guaranteed.

# Technical Workflow
Data extraction was first performed using PostgreSQL, followed by Python-based data preprocessing, model training, data analysis, and model evaluation. We provide the corresponding SQL scripts and Python code used in this project.

💡 Note on Chinese identifiers: We extensively used Chinese variable names and Chinese-language output during development. As a result, you may encounter a small number of directories or variables with Chinese names. Please rest assured—this does not affect code execution or the validity of the final conclusions.

# Data Access
Both INSPIRE and MOVER are controlled-access datasets. Access requires completion of required training and signing of a Data Use Agreement (DUA).

INSPIRE: https://physionet.org/content/inspire/1.3/
MOVER: https://mover.ics.uci.edu/index.html

⚠️ Important: This repository does not include any raw patient data—only the associated code is provided.

```
Project Structure
.
├── python/          # All Python code used in this project
├── sql/             # All SQL code used for data extraction
└── requirements.txt # Python dependencies (note: no raw data is included)
```
