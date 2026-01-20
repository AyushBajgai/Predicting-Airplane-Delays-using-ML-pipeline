# Flight Delays ML Pipeline

## Overview
This repository contains all Jupyter notebooks and Python scripts used to analyze airline flight delays.  
The workflow covers:
- Data loading and cleaning  
- Exploratory Data Analysis (EDA)  
- Feature engineering  
- Model training and evaluation  

You can access the dataset from this source:  
[Airline Delay Dataset](https://ucstaff-my.sharepoint.com/personal/ibrahim_radwan_canberra_edu_au/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fibrahim%5Fradwan%5Fcanberra%5Fedu%5Fau%2FDocuments%2Fteaching%5Fjunction%2FDSTS2025%2Fdata%5Fcompressed&ga=1)  

Feature of the dataset from this source:
Bureau of Transportation Statistics (BTS), Airline On-Time Performance Data, available at the following link: [dataset attributes](https://www.transtats.bts.gov/Fields.asp?gnoyr_VQ=FGJ).

## How to Run
1. Open the Jupyter Notebook environment.
2. Make sure you have all required Python packages installed (see below).
3. Run the notebook cells step-by-step.

## Requirements
Install required libraries directly from this notebook using:
```python
!pip install -r requirements.txt
```

## Architecture
- Part A (On-Premises):
  - Data extraction from compressed files
  - Feature engineering and one-hot encoding
  - Missing value handling and dataset consolidation

- Part B (Cloud – AWS SageMaker):
  - Data upload to Amazon S3
  - Train/validation/test split (70/15/15)
  - Model training using SageMaker built-in algorithms
  - Endpoint deployment and batch inference

## Models Implemented
- Linear Learner (Binary Classification)
- XGBoost (Ensemble Model)

## Model Evaluation
Evaluation performed using SageMaker Batch Transform with the following metrics:
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix

Performance Summary:
- Linear Learner achieved ~76% accuracy with baseline performance
- XGBoost improved predictive power with ~78% accuracy and higher ROC-AUC
- Ensemble model demonstrated superior recall and overall robustness

## Technologies Used
- Python
- AWS SageMaker
- Amazon S3
- Boto3
- Scikit-learn
- XGBoost
- Pandas & NumPy

## Key Learning Outcomes
- Migrating ML workflows from on-premises to cloud infrastructure
- Building scalable ML pipelines using managed AWS services
- Comparing baseline and ensemble models in production-like environments
- Deploying and evaluating models using batch inference

## Use Cases
- Travel booking platforms
- Airline operations planning
- Weather-aware logistics systems
- Large-scale predictive analytics in cloud environments

## Future Improvements
- Incorporate real-time weather APIs
- Apply class-imbalance handling techniques
- Introduce model explainability (SHAP)
- Deploy real-time inference endpoints
- Extend to multi-class delay prediction
