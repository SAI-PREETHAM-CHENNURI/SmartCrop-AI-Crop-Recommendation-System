SmartCrop AI — Crop Recommendation and Anomaly Detection

A notebook-based crop classification and recommendation prototype using 57 crop classes and a dataset of 57,000 rows (as recorded in the notebook's saved outputs).


Features


Preprocessing, exploratory analysis, and feature leakage investigation

Comparison of Logistic Regression, Random Forest, Extra Trees, XGBoost, and LightGBM across feature sets

K-Means clustering experiments

Isolation Forest anomaly detection, including an out-of-distribution threshold

Robustness checks using perturbed inputs

Recommendation function with input validation, anomaly-based abstention, and top-N suggestions

Model serialization with Joblib


Recorded results

The notebook's saved outputs select Random Forest with the core_without_season feature set, reporting 98.48% validation accuracy and 0.9848 validation macro F1. These results are from the included notebook; they have not been independently reproduced in this repository. Performance on independent real-world farm data has not been established.


Run in Google Colab


Open SmartCrop_AI.ipynb in Google Colab.

Upload the required dataset file named Crop recommendation dataset.csv into the notebook's working directory (or adjust DATA_PATH in cell 3).

Run the cells in order. The notebook installs packages in its first cells.

Review the validation, test, anomaly, and robustness results before using any predictions.


Dataset not included: The CSV was not supplied with this repository package. Add a source/attribution and verify permission before distributing it. Without the CSV, the notebook cannot run end-to-end.


Limitations

This is an educational/research prototype, not a validated agronomic advisory tool. Unusual inputs can be flagged by Isolation Forest, but anomaly detection is not proof that a recommendation is safe or agriculturally suitable. The notebook is not a hosted web application.


Repository contents


crop.ipynb — full experiment and recommendation workflow

requirements.txt — Python package dependencies

.gitignore — excludes generated artifacts and private/local data

