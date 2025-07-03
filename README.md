🩺 Diabetes Prediction System
This project builds a machine learning system to predict whether a person(women) has diabetes, based on key health parameters. 

🚀 Overview
Goal: Predict diabetes (binary outcome: diabetic / non-diabetic) using features such as glucose level, BMI, age, etc.

Tech stack: Python, Pandas, scikit-learn, Seaborn, Matplotlib.

Models used:

K-Nearest Neighbors (KNN)

Support Vector Machine (SVM) with linear kernel

🗂 Dataset
The dataset is loaded from diabetes.csv.

It contains features like:

Pregnancies

Glucose

BloodPressure

SkinThickness

Insulin

BMI

DiabetesPedigreeFunction

Age

Target variable: Outcome (0: no diabetes, 1: diabetes).

🔍 Exploratory Data Analysis (EDA)
Checked for missing values and duplicates (none found).

Plotted a heatmap of correlations, which showed:

Glucose and BMI are most strongly correlated with diabetes outcome.

Used bar plots to visualize how glucose varies across diabetic and non-diabetic groups.

⚙️ Model Training
✅ Data preparation
Split features (X) and target (Y).

Standardized features using StandardScaler to ensure fair distance calculations for KNN and better SVM convergence.

Performed an 80-20 train-test split, stratified on outcome to keep class balance.

🔎 Models tried
🔵 K-Nearest Neighbors (KNN)
Used K=5.

Achieved moderate precision and recall.

🔴 Support Vector Machine (SVM)
Used SVC with linear kernel and C=1.0.

Outperformed KNN in both precision and recall on test set.

🏆 Final Model
Selected SVM (linear kernel) as the production model due to higher precision and recall.

🧪 Prediction Function
Created a Diabetes_prediction function that:

Accepts an 8-element tuple of features.

Transforms data using the fitted StandardScaler.

Predicts diabetes outcome using the trained SVM model.

📝 Requirements
Python 3.8+

pandas

numpy

scikit-learn

matplotlib

seaborn

jupyter

