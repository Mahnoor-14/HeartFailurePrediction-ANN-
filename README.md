# HeartFailurePrediction-ANN-
This project leverages machine learning techniques to predict the likelihood of death in patients suffering from cardiovascular diseases using a clinical dataset. Specifically, it employs an Artificial Neural Network (ANN) model to classify patients based on their health indicators.
![image](https://github.com/user-attachments/assets/71eefef6-cbd0-42c5-96a2-faa47f50fc01)

📁 Dataset
Name: Heart Failure Clinical Records Dataset

Source: [Kaggle or UCI Repository (based on actual source)]

Records: 299 patients

Attributes: 13

Target Variable: DEATH_EVENT (1 = Deceased, 0 = Survived during follow-up)

💉 Features Description:
Feature	Description
age	Age of the patient
anaemia	Haemoglobin level (0 = No, 1 = Yes)
creatinine_phosphokinase	CPK enzyme level in blood (mcg/L)
diabetes	Diabetes (0 = No, 1 = Yes)
ejection_fraction	% of blood leaving the heart per contraction
high_blood_pressure	Hypertension (0 = No, 1 = Yes)
platelets	Platelet count (kiloplatelets/mL)
serum_creatinine	Level of serum creatinine (mg/dL)
serum_sodium	Level of serum sodium (mEq/L)
sex	Sex (0 = Female, 1 = Male)
smoking	Smoking status (0 = No, 1 = Yes)
time	Follow-up duration (in days)
DEATH_EVENT	Target variable (0 = Alive, 1 = Deceased)

🧠 Objective
To build and evaluate a neural network that can predict the likelihood of heart failure, helping in early diagnosis and potential prevention.

🧪 Dependencies
Install dependencies using:

bash
Copy
Edit
pip install numpy pandas matplotlib seaborn scikit-learn keras
📌 Steps Performed
1. Data Loading
Data is loaded from a CSV file stored in Google Drive via Google Colab.

2. Exploratory Data Analysis (EDA)
Checked for missing values (none found).

Investigated data balance (imbalance: 203 alive vs 96 deceased).
![image](https://github.com/user-attachments/assets/233dc30f-4741-45a1-aa08-c3a9905f4b54)

Analyzed correlation using heatmaps.

Examined how age and other factors relate to mortality.

3. Data Preprocessing
Split into features X and label y.

Applied StandardScaler for feature scaling.

Split data into training and test sets (70/30).

4. Model Building
Designed an ANN using Keras with the following architecture:

Input Layer: 12 features

Hidden Layers: Dense(16) → Dense(8, Dropout) → Dense(8, Dropout)

Output Layer: Sigmoid Activation

Used Adam optimizer and binary_crossentropy loss.

Implemented early stopping to prevent overfitting.

5. Model Training & Evaluation
Trained over 50 epochs with batch size 25.

Tracked training and validation accuracy and loss.

Evaluated predictions using:

Confusion matrix

Classification report (Precision, Recall, F1-score)

📈 Performance Visualization
Training vs Validation Accuracy/Loss:
Plotted to check convergence and overfitting.

Confusion Matrix:
Helps assess model precision and recall.
![2](https://github.com/user-attachments/assets/ce05c1c4-e2b3-4b69-8882-fb8beacaebfd)

📌 Results (Sample)
Validation Accuracy: ~82%
![1](https://github.com/user-attachments/assets/9ed26413-67a8-45e2-9493-25e568acbfbb)

Precision / Recall / F1-score: Depend on classification threshold (default used: 0.4)

💡 Future Improvements
Use SMOTE or Class weights to handle class imbalance.

Try advanced models (e.g., Random Forest, XGBoost).

Tune hyperparameters more thoroughly.

Add cross-validation for robust evaluation.
