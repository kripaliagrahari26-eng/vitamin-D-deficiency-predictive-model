# vitamin-D-deficiency-predictive-model
End-to-end machine learning pipeline for Vitamin D deficiency prediction and actionable customer risk segmentation.
# Vitamin D Deficiency Prediction

A machine learning project that predicts vitamin D deficiency risk using patient lifestyle and dietary data.

## Files

| File | Description |
|---|---|
| `Dataset_vitamin_deficiency_disease.csv` | Dataset with 34 features per patient |
| `vitamin_D_predictive_modelling.ipynb` | End-to-end ML pipeline (Google Colab) |

## Dataset

**Features include:**
- Demographics: age, gender, BMI
- Lifestyle: smoking status, alcohol consumption, exercise level, diet type, sun exposure
- Nutritional intake: % RDA for vitamins A, C, D, E, B12, folate, calcium, iron
- Lab values: serum vitamin D, B12, folate, hemoglobin
- Clinical: symptoms list, disease diagnosis, multiple deficiency flag

**Target variable:** `vitamin_d_status` — binary (1 = deficient if vitamin D % RDA < 100, else 0)

**Disease classes:** Healthy, Anemia, Rickets/Osteomalacia, Night Blindness

## Methodology

1. **EDA** — Correlation heatmap, deficiency rates by sun exposure, income, and diet type
2. **Feature Engineering** — Binary target creation, one-hot encoding, standard scaling
3. **Models Trained:**
   - Logistic Regression
   - Decision Tree (max_depth = 4)
4. **Evaluation** — Accuracy, Precision, Recall, F1, ROC-AUC, 5-fold cross-validation
5. **Risk Segmentation** — Patients classified as Low / Medium / High risk using predicted probabilities
6. **Interactive Predictor** — Widget-based form to predict deficiency risk for new patients

## Requirements
```
pandas
numpy
scikit-learn
matplotlib
seaborn
ipywidgets
```

Run in **Google Colab** with the dataset uploaded to Google Drive.

## Usage

1. Upload the CSV to Google Drive
2. Open the notebook in Google Colab
3. Run all cells
4. Use the interactive widget at the end to predict risk for individual patients
