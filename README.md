# AquaSense: Machine Learning-Based Water Potability Assessment System

**Author:** Odoi Stephen  
**Course:** MSC 7103 Machine Learning Practical Exam, Makerere University  
**Project:** A machine- learning water potability assessment system(Aqua sense).

## Overview

AquaSense compares logistic regression, random forest and gradient boosting on the Kaggle Water Quality dataset. The code reserves 20% of records for testing, compares models using five-fold training cross-validation and chooses a non-potable threshold using training out-of-fold predictions. The random forest and selected threshold are then evaluated on the held-out test set.

At the selected threshold of 0.435, the forest identified 384 of 400 records labelled non-potable in the test set. It also flagged 205 of 256 records labelled potable. These estimates refer to this dataset and split; AquaSense is a research prototype and cannot certify that water is safe to drink.

## Project files

- `AquaSense_Analysis.ipynb` — notebook that reconstructs the analysis and trains the model.
- `water_potability.csv` — dataset used by the notebook.
- `AquaSense_random_forest_v1.joblib` — fitted preprocessing and model bundle, including the selected threshold.
- `Odoi_Stephen_AquaSense_Report.pdf` 
- `AquaSense_*.png` — figures used in the report.
- `requirements.txt` — Python packages and versions used to verify the notebook.


## Data source and limitations

The dataset is Aditya Kadiwal's [Water Quality dataset on Kaggle](https://www.kaggle.com/datasets/adityakadiwal/water-potability). 
