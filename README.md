#  Cellphone Price Classification Project

A supervised machine learning project that predicts the **price range of a cellphone** (0 to 3) using features such as RAM, battery power, camera specs, screen dimensions, and more. The goal is to build an accurate, interpretable, and production-ready model using Logistic Regression.

---

##  Project Overview

- **Problem Type:** Multiclass Classification
- **Target Variable:** `price_range` (0 = low cost, 3 = high cost)
- **Algorithm Used:** Logistic Regression (tuned with GridSearchCV)
- **Explainability:** SHAP (SHapley Additive exPlanations)

##  Target Labels Explained

The `price_range` column contains:
- **0** → Low cost
- **1** → Medium cost
- **2** → High cost
- **3** → Very high cost

##  Key Features Used

- `battery_mAh`: Battery capacity
- `clock_speed_GHz`: Processor speed
- `has_4G`: 4G capability
- `internal_storage_GB`: Built-in storage
- `RAM_MB`: RAM size
- `talk_time_hr`: Talk time in hours
- `average_camera_MP`: Average megapixels of front and rear cameras
- `total_pixel_resolution`: Product of height × width in pixels
- `screen_area_cm2`: Approximate screen area


---

##  Model Results

| Metric            | Value     |
|-------------------|-----------|
| Accuracy          | **95.0%** |
| F1 Macro Score    | **0.9287** |
| CV F1 Score (5-fold) | **0.9287** |

- ROC AUC Scores per class (Logistic Regression):
  - Class 0: **1.00**
  - Class 1: **0.65**
  - Class 2: **0.66**
  - Class 3: **1.00**

---

##  Why Logistic Regression?

- Performs consistently across classes.
- Outperformed other models in **generalization and interpretability**.
- Simpler and more efficient for deployment.
- Excellent compatibility with SHAP explainability tools.



##  Explainability with SHAP

- **Top impactful features**: `RAM_MB`, `battery_mAh`, `total_pixel_resolution`
- SHAP force plots and waterfall plots illustrate how individual features affect predictions.
- Helps in communicating results with business teams.




