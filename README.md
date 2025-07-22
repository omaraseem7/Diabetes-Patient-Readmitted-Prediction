# Diabetes-Patient-Readmitted-Prediction
This project aims to predict hospital readmission outcomes for diabetic patients using machine learning models trained on the **"Diabetes 130-US hospitals for years 1999–2008"** dataset. The project includes preprocessing, exploratory analysis, model building, and performance evaluation.
# Dataset
- **Source**: UCI Machine Learning Repository
- **Link**:"https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008"
- **Records**: 100,000+ patient encounters  
- **Target**: `readmitted` (categorized as):
  - `0` → Not readmitted (`NO`)
  - `1` → Readmitted within 30 days (`<30`)
  - `2` → Readmitted after 30 days (`>30`)
 # Preprocessing Steps
 - Dropped unnecessary columns (`encounter_id`, `patient_nbr`, etc.)
- Handled missing values and placeholder `'?'` values
- Categorical encoding using One-Hot Encoding
- Mapped ICD-9 diagnosis codes to clinical categories
- Winsorized outliers for several numerical columns
- Standard scaled numerical features
- Converted target to binaryclass format (`0`, `1`)
# 📊 Models Used
- Logistic Regression
- Random Forest Classifier
- XGBoost Classifier
- Linear SVM
- K-Nearest Neighbors (KNN - Multiclass)
# Evaluation Metrics
- Accuracy
- Precision / Recall / F1-score
- ROC AUC Score
- Confusion Matrix
## Final Comparison Table
| Model              | Accuracy | Precision | Recall | F1-Score | ROC AUC |
|--------------------|----------|-----------|--------|----------|---------|
| **Logistic Regression** | 0.6228   | 0.62      | 0.61   | 0.61     | 0.6570  |
| **Random Forest**       | 0.6326   | 0.63      | 0.62   | 0.62     | 0.6771  |
| **Linear SVM**          | 0.6230   | 0.62      | 0.61   | 0.61     | 0.6571  |
| **XGBoost**             | **0.6376**   | **0.64**      | **0.63**   | **0.63**     | **0.6876**  |

> ✅ **XGBoost** performed the best overall, achieving the highest accuracy and ROC AUC score among all models.

## 📁 Project Structure
- Patient_readmission_Project.ipynb - Main Jupyter notebook
- diabetic_data.csv - Dataset
- README.md - Project overview
