# Multiple Disease Prediction System

## About the Project

The Multiple Disease Prediction System is a Machine Learning project I developed as part of my hands-on learning journey to understand and implement different Machine Learning concepts.

I wanted to explore how Machine Learning works across different prediction tasks, so I brought three individual projects — Diabetes, Heart Disease, and Parkinson's Disease Prediction — together into a single interactive application using Python and Streamlit.

Although all three projects belong to the same domain, each involves a different dataset, set of input features, and prediction model. This gave me an opportunity to experiment with different classification algorithms, understand data preprocessing and feature selection, and train and evaluate multiple independent models.

The project brings these individual prediction systems together under one application, allowing me to apply and strengthen my Machine Learning knowledge through practical implementation.

## Diseases Covered

- **Diabetes Prediction:** Predicts the likelihood of diabetes using medical attributes such as glucose level, blood pressure, BMI, insulin level, and other health-related parameters.
- **Heart Disease Prediction:** Predicts the likelihood of heart disease using clinical attributes such as age, chest pain type, cholesterol, resting blood pressure, maximum heart rate, and other relevant parameters.
- **Parkinson's Disease Prediction:** Predicts the likelihood of Parkinson's disease using biomedical voice measurements and extracted voice features.

## Machine Learning Models and Performance

The project uses Supervised Learning, specifically Binary Classification, for all three prediction tasks.

| Disease             | Algorithm                              | Test Accuracy |
| ------------------- | -------------------------------------- | ------------: |
| Diabetes            | Support Vector Machine (Linear Kernel) |        77.27% |
| Heart Disease       | Logistic Regression                    |        78.69% |
| Parkinson's Disease | Support Vector Machine (Linear Kernel) |        87.18% |

All three models use StandardScaler for feature scaling before classification.

## 1. Diabetes Prediction Model

- **Dataset:** `diabetes.csv`
- **Target Variable:** `Outcome`
- **Machine Learning Type:** Supervised Learning
- **Problem Type:** Binary Classification
- **Algorithm:** Support Vector Machine (SVM) with Linear Kernel
- **Preprocessing:** StandardScaler
- **Training Accuracy:** 78.66%
- **Testing Accuracy:** 77.27%

### Features Selected

The model uses the following eight input features:

1. Pregnancies
2. Glucose
3. BloodPressure
4. SkinThickness
5. Insulin
6. BMI
7. DiabetesPedigreeFunction
8. Age

## 2. Heart Disease Prediction Model

- **Dataset:** `heart.csv`
- **Target Variable:** `target`
- **Machine Learning Type:** Supervised Learning
- **Problem Type:** Binary Classification
- **Algorithm:** Logistic Regression
- **Preprocessing:** StandardScaler
- **Training Accuracy:** 84.71%
- **Testing Accuracy:** 78.69%

### Features Selected

The model uses the following thirteen input features:

1. age
2. sex
3. cp
4. trestbps
5. chol
6. fbs
7. restecg
8. thalach
9. exang
10. oldpeak
11. slope
12. ca
13. thal

## 3. Parkinson's Disease Prediction Model

- **Dataset:** `parkinsons.csv`
- **Target Variable:** `status`
- **Machine Learning Type:** Supervised Learning
- **Problem Type:** Binary Classification
- **Algorithm:** Support Vector Machine (SVM) with Linear Kernel
- **Preprocessing:** StandardScaler
- **Training Accuracy:** 88.46%
- **Testing Accuracy:** 87.18%

### Features Selected

The model uses 22 biomedical voice measurement features:

1. MDVP\:Fo(Hz)
2. MDVP\:Fhi(Hz)
3. MDVP\:Flo(Hz)
4. MDVP\:Jitter(%)
5. MDVP\:Jitter(Abs)
6. MDVP\:RAP
7. MDVP\:PPQ
8. Jitter\:DDP
9. MDVP\:Shimmer
10. MDVP\:Shimmer(dB)
11. Shimmer\:APQ3
12. Shimmer\:APQ5
13. MDVP\:APQ
14. Shimmer\:DDA
15. NHR
16. HNR
17. RPDE
18. DFA
19. spread1
20. spread2
21. D2
22. PPE

The `name` column is excluded from model training, and `status` is used as the target variable.

## Model Training and Evaluation

The models were trained and evaluated using an 80:20 training and testing split.

- Diabetes: `train_test_split(test_size=0.2, stratify=Y, random_state=2)`
- Heart Disease: `train_test_split(test_size=0.2, stratify=Y, random_state=2)`
- Parkinson's Disease: `train_test_split(test_size=0.2, random_state=2)`

Accuracy was calculated using Scikit-learn's `accuracy_score` on both training and testing datasets.

## Technologies Used

- **Programming Language:** Python
- **Application Framework:** Streamlit
- **Machine Learning:** Scikit-learn
- **Data Processing:** NumPy, Pandas
- **Data Visualization:** Matplotlib, Seaborn
- **Model Serialization:** Pickle

## Key Features

- Three disease prediction systems in one application.
- Independently trained classification models.
- Separate datasets and feature sets for each disease.
- Feature scaling using StandardScaler.
- Saved and reusable trained models.
- Interactive user interface built with Streamlit.
