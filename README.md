# Industrial-Failure-Intelligence-System-IFIS

IFIS (Industrial Failure Intelligence System) is an end-to-end machine learning framework built to predict industrial equipment failures before breakdown, identify the core failure drivers, and prioritize maintenance actions based on risk severity.

This project transforms raw machine sensor data into actionable maintenance intelligence using advanced feature engineering, imbalance handling, explainable AI, and risk scoring.

---

Project Objective

Industrial failures often result in:

- Production downtime
- High maintenance costs
- Safety risks
- Resource inefficiency

The objective of IFIS is to build a predictive maintenance intelligence system capable of:

- Predicting machine failures
- Ranking high-risk machines
- Identifying root causes
- Supporting proactive maintenance decisions

---

Dataset Used

Dataset: AI4I 2020 Predictive Maintenance Dataset
Source: UCI Machine Learning Repository

Dataset contains:

- Air Temperature
- Process Temperature
- Rotational Speed
- Torque
- Tool Wear
- Machine Type
- Failure Labels

Total records: 10,000

---

Project Workflow

1. Data Validation Layer

- Missing value detection
- Duplicate check
- Class imbalance analysis
- Failure type distribution analysis

---

2. Feature Engineering Layer

Built custom industrial intelligence features:

Thermal Stress Index (TSI)

Measures heat differential between process and air temperature.

TSI = Process Temperature - Air Temperature

---

Mechanical Load Index (MLI)

Captures machine operational load.

MLI = Torque × Rotational Speed

---

Wear Intensity Score (WIS)

Measures wear under load.

WIS = Tool Wear × Torque

---

Speed Stress Ratio (SSR)

Captures overload behavior.

SSR = Rotational Speed / Torque

---

Composite Health Index (CHI)

Custom health degradation score.

CHI combines:

- Thermal stress
- Torque
- Tool wear
- Mechanical load

---

3. Class Imbalance Handling

Used SMOTE to balance failure and non-failure classes.

Why:

Failure records were only 3.39% of total data.

---

4. Model Training

Models tested:

- Random Forest
- XGBoost

Final selected model:

XGBoost

Reason:

Higher precision and better F1 score.

---

5. Explainable AI Layer

Used SHAP for:

- Feature importance analysis
- Root cause explainability
- Machine-level decision transparency

---

6. Risk Intelligence Layer

Built risk scoring engine:

Risk Score = Failure Probability × 100

Risk categories:

- Critical (70–100)
- High (40–69)
- Moderate (20–39)
- Low (0–19)

---

Model Performance

Random Forest

Precision: 0.60
Recall: 0.81
F1-score: 0.69

---

XGBoost (Production Model)

Precision: 0.64
Recall: 0.81
F1-score: 0.71

Accuracy: 98%

---

Key Results

- Successfully detected 81% of machine failures
- Reduced false maintenance alerts compared to baseline
- Ranked top 10 critical machines with 100% true failure precision
- Generated explainable failure root causes using SHAP

---

Feature Importance Insights

Top predictive drivers:

1. Speed Stress Ratio (SSR)
2. Rotational Speed
3. Mechanical Load Index (MLI)
4. Torque
5. Tool Wear

This validates the effectiveness of engineered industrial features.

---

Dashboard Features

ForgeSight AI Dashboard includes:

- Risk Score Distribution
- Top Critical Machines
- Failure Heatmaps
- Root Cause Frequency Analysis
- Maintenance Priority Matrix

---

Tech Stack

Programming:

- Python

Libraries:

- Pandas
- NumPy
- Scikit-learn
- XGBoost
- SHAP
- Plotly
- Matplotlib
- Imbalanced-learn

Deployment:

- Google Colab
- GitHub
- Streamlit (planned)

---

Project Structure

IFIS/
│── data/
│── notebooks/
│── app/
│── models/
│── images/
│── README.md
│── requirements.txt

---

Business Impact

IFIS helps industries:

- Predict equipment failures before breakdown
- Reduce unplanned downtime
- Improve maintenance scheduling
- Increase operational efficiency
- Reduce maintenance costs

---

Future Improvements

- Real-time IoT integration
- Live dashboard deployment
- Multi-machine streaming analytics
- Maintenance cost optimization
- Failure simulation engine

---

Author

Mayur Gaikwad

Project Management | Data Science | AI | Predictive Analytics

---

Connect

If you found this project useful or want to collaborate on industrial AI systems, feel free to connect.
