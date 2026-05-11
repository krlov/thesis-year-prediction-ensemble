# Thesis Year Prediction with Ensemble Regression Methods

This project investigates thesis year prediction from short academic texts using embedding-based semantic representations and ensemble regression models.

Different text representations and ensemble learning strategies were systematically compared to analyze how semantic information quality affects regression performance.

---

# Project Overview

The study evaluates:

* Three text representations:

  * Title only
  * Abstract only
  * Combined (Title + Abstract)

* Three ensemble regression methods:

  * Bagging
  * Random Subspace
  * Random Forest

* Hyperparameter optimization effects:

  * Number of estimators
  * Feature sampling ratio
  * Sample ratio
  * Tree depth

Performance was evaluated using:

* MAE
* RMSE
* R²

---

# Key Findings

* Abstract representations produced the best semantic signal and lowest prediction error.
* Title-only representations showed the weakest performance due to limited contextual information.
* Combined representations slightly underperformed Abstract-only representations because of redundant or noisy information.
* Bagging achieved the most stable overall performance.
* Representation quality had a larger impact on performance than ensemble model selection.

---

# Technologies Used

* Python
* Scikit-learn
* Sentence Transformers
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Jupyter Notebook

---

# Repository Structure

```text id="uxd6eb"
.
├── report_outputs/
│   ├── bagging_hyperparameter_tuning_mae_abstract.png
│   ├── random_subspace_hyperparameter_tuning_mae_abstract.png
│   ├── random_forest_hyperparameter_tuning_mae_abstract.png
│   ├── mae_by_model_and_representation.png
│   ├── mae_by_representation_for_each_model.png
│   ├── r2_heatmap_representation_model.png
│   └── year_prediction_scatter_all_models_all_representations.png
│
├── Proje.ipynb
├── Proje Sunumu.pdf
├── Rapor.pdf
├── requirements.txt
├── LICENSE
└── README.md
```

---

# Visual Outputs

## Hyperparameter Analysis

* Bagging hyperparameter behavior
* Random Subspace feature sampling analysis
* Random Forest parameter sensitivity

## Representation Performance Analysis

* MAE comparison across representations
* Model-wise representation performance
* R² heatmap analysis

## Prediction Distribution Analysis

* Scatter plots comparing predicted vs real thesis years
* Error distribution behavior across all models and representations

---

# Results Summary

| Representation | Best Model | MAE   | R²    |
| -------------- | ---------- | ----- | ----- |
| Title          | Bagging    | ~5.68 | ~0.08 |
| Abstract       | Bagging    | ~5.15 | ~0.22 |
| Combined       | Bagging    | ~5.22 | ~0.19 |

---

# How to Run

Install dependencies:

```bash id="muj6of"
pip install -r requirements.txt
```

Open notebook:

```bash id="7u1z1j"
jupyter notebook Proje.ipynb
```

---

# Report and Presentation

* `Rapor.pdf` contains the full methodological analysis and experimental evaluation.
* `Proje Sunumu.pdf` contains the project presentation slides.

---

# License

This project is licensed under the MIT License.
