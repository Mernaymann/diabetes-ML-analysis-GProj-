Diabetes is a growing global health challenge, often undiagnosed until advanced stages.
This project applies machine learning techniques for early prediction of diabetes, focusing on:

Data preprocessing
Feature engineering
Model evaluation
Explainable AI (XAI)

The goal is to improve early detection and support better decision-making through data-driven insights.
Preview
<img width="1582" height="907" alt="Screenshot 2026-05-08 235733" src="https://github.com/user-attachments/assets/7fc7be92-8d38-483a-b2fa-9fa9d61c99f6" />
The application is deployed using Lovable and includes advanced model interpretability techniques such as SHAP and Permutation Importance to explain predictions clearly.
# Live Demo
Try the app here: Diabetes Prediction App
https://diabetes-predictor-mer.lovable.app/dashboard
Table of Contents
Overview
Dataset
Model
Features
Installation
How It Works
Project Structure
Explainability Methods
Model Performance
Project Motivation
Contributing
License
Contact
🧠 Overview
This project uses machine learning to estimate the risk of diabetes based on patient health indicators.

The focus is not only on prediction accuracy, but also on model interpretability, making it easier to understand why a prediction was made.

⚠️ Disclaimer: This model is not medically validated and is intended for educational and experimental purposes only.

💡 Why this project?
Real-world application of ML in healthcare
Focus on model interpretability (SHAP, permutation importance)
End-to-end deployment using Streamlit
Experimentation with threshold tuning for recall optimization
📊 Dataset

Source: National Institute of Diabetes and Digestive and Kidney Diseases

Dataset Overview
Rows: 768
Columns: 9
Features:
Pregnancies
Glucose
BloodPressure
SkinThickness
Insulin
BMI
DiabetesPedigreeFunction
Age
Outcome (0/1)
⚠️ Note

Some features contain zero values that may represent missing data and require preprocessing.

🤖 Model
Algorithm: RandomForestClassifier
Hyperparameter tuning: Optuna
Feature pipeline includes:
Feature Engineering
WoE Encoding
Column Selection
📌 Why Random Forest?

Chosen due to strong performance on non-linear tabular medical data and robustness against overfitting.

📈 Evaluation Strategy
Cross-validation used due to limited dataset size
Metric focus: ROC AUC + Recall (medical priority)
⚙️ Features
Interactive health input form (Streamlit UI)
Real-time diabetes risk prediction
Probability output
Explainability:
SHAP Waterfall Plot
SHAP Force Plot
Feature importance analysis
Performance dashboard:
Accuracy
Precision
Recall
F1 Score
ROC AUC
🛠 Installation
1. Clone repo
git clone https://github.com/UznetDev/Diabetes-Prediction.git
cd Diabetes-Prediction
2. Install dependencies
pip install -r requirements.txt
3. Run app
streamlit run main.py
🔄 How It Works
User enters health data
Model processes input through preprocessing pipeline
Random Forest predicts diabetes risk
SHAP explains feature contribution
Results + probability displayed in UI
📁 Project Structure
Diabetes-Prediction/
│── main.py
│── training.py
│── loader.py
│── requirements.txt
│
├── datasets/
├── models/
├── functions/
├── app/
├── data/
├── images/
🧾 Explainability Methods
🔍 SHAP (Explainable AI)
Waterfall Plot → local prediction breakdown
Force Plot → feature influence per prediction
📊 Permutation Importance

Measures how much each feature affects model performance globally.

📈 Model Performance
Accuracy: 0.7857
Precision: 0.6296
Recall: 0.9444
F1 Score: 0.7556
ROC AUC: 0.8367
🎯 Project Motivation
Learn ML in healthcare context
Understand model interpretability
Deploy real-world AI system
Improve recall for medical sensitivity use-case

📬 Contact
Email: mernaay01@gmail.com
GitHub: Mernaymann
LinkedIn: www.linkedin.com/in/merna-ayman-005578364 -- Merna ayman
