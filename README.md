# AquaSense: Machine Learning-Based Water Potability Assessment

**Author:** Odoi Stephen  
**Course:** MSC 7103 Machine Learning Practical Exam, Makerere University  
**Project:** Predict recorded potability labels from water-quality measurements.

## Overview

AquaSense compares logistic regression, random forest and gradient boosting on the Kaggle Water Quality dataset. The code reserves 20% of records for testing, compares models using five-fold training cross-validation and chooses a non-potable threshold using training out-of-fold predictions. The random forest and selected threshold are then evaluated on the held-out test set.

At the selected threshold of 0.435, the forest identified 384 of 400 records labelled non-potable in the test set. It also flagged 205 of 256 records labelled potable. These estimates refer to this dataset and split; AquaSense is a research prototype and cannot certify that water is safe to drink.

## Project files

- `AquaSense_Analysis.ipynb` — notebook that reconstructs the analysis and trains the model.
- `water_potability.csv` — dataset used by the notebook.
- `AquaSense_random_forest_v1.joblib` — fitted preprocessing and model bundle, including the selected threshold.
- `Odoi_Stephen_AquaSense_Report.pdf` — report and references; insert your GitHub repository link before submission.
- `AquaSense_*.png` — figures used in the report.
- `requirements.txt` — Python packages and versions used to verify the notebook.

The notebook was reconstructed and executed against the supplied CSV; its results match the report. The joblib file was produced by this notebook. It is compatible with scikit-learn 1.8.0; model files should only be loaded from trusted sources.

## Run the notebook in Google Colab

1. Open [Google Colab](https://colab.research.google.com/) and choose **File > Upload notebook**.
2. Upload `AquaSense_Analysis.ipynb`.
3. In Colab, open the folder icon on the left, select **Upload to session storage**, and upload `water_potability.csv`.
4. Choose **Runtime > Run all**. Colab session files are temporary, so re-upload the CSV if you start a new session. If a required library is missing, install the packages named in `requirements.txt`.
5. The notebook prints the results, displays evaluation plots and saves `AquaSense_random_forest_v1.joblib` in the current session.

## Data source and limitations

The dataset is Aditya Kadiwal's [Water Quality dataset on Kaggle](https://www.kaggle.com/datasets/adityakadiwal/water-potability). Review the dataset's applicable terms before redistribution. The dataset does not establish a verified Ugandan origin or explain how the labels were produced. Nine physicochemical features cannot rule out microbial contamination; laboratory confirmation remains necessary.
