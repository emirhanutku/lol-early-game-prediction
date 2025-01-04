# 🏆 League of Legends Early Game Prediction: A Data Mining Project

## 📚 Project Overview
This project aims to predict early-game outcomes in **Challenger-ranked League of Legends matches** using a snapshot of in-game statistics at the **15-minute mark**. The project consists of two primary goals:

1. **Classification Task:** Predict which team (Blue or Red) will win the game based on in-game statistics.
2. **Regression Task:** Predict the total gold earned by the Blue team at the 15-minute mark.

---

## 📊 Dataset
- **Dataset Source:** [League of Legends Challenger Rank Game Data](https://www.kaggle.com/datasets/gyejr95/league-of-legends-challenger-rank-game10min15min)
- **Dataset File:** `Challenger_Ranked_Games_15minute.csv`
- **Details:**
   - 51 features, including gold, kills, assists, objectives, and wards.
   - Snapshot from 15-minute mark for both Blue and Red teams.

---

## ⚙️ Methodology

### 1️⃣ **Data Preprocessing**
- Handled missing values and inconsistencies.
- Feature scaling using **Min-Max Scaling**.
- Removed non-relevant columns (e.g., string/object attributes).

### 2️⃣ **Exploratory Data Analysis (EDA)**
- Distribution analysis of numerical features (e.g., gold, kills, assists).
- Correlation heatmaps for identifying influential features.
- Feature engineering:
   - **Objective Control Score**
   - **Gold Efficiency**
   - **Gold per Minute**
   - **K/D Ratio**
   - **Ward Efficiency**

### 3️⃣ **Classification Models**
- **Random Forest Classifier**
- **XGBoost Classifier**
- **K-Nearest Neighbors**
- **Logistic Regression**
- **Decision Tree**
- **Support Vector Machine (SVM)**
- **Stacking Classifier (Ensemble Method)**

**Evaluation Metrics:**  
- Accuracy  
- Precision  
- Recall  
- F1-Score  

### 4️⃣ **Regression Models**
- **Linear Regression**
- **Random Forest Regressor**
- **XGBoost Regressor**

**Evaluation Metrics:**  
- Mean Squared Error (MSE)  
- Mean Absolute Error (MAE)  
- R² Score  

### 5️⃣ **SHAP Analysis**
- SHAP (SHapley Additive exPlanations) was used to interpret and validate the model's predictions.
- Insights on feature contributions to predictions.

---

## 📈 Results

### 🥇 **Classification Performance**
| Model             | Accuracy | Precision | Recall | F1-Score |
|--------------------|---------:|---------:|-------:|---------:|
| KNN               | 76.8%    | 78.1%    | 75.5% | 76.7%   |
| LogisticRegression| 78.0%    | 81.2%    | 73.9% | 77.4%   |
| DecisionTree      | 78.7%    | 78.4%    | 80.2% | 79.3%   |
| RandomForest      | 79.8%    | 80.2%    | 79.7% | 80.0%   |
| XGBClassifier     | 79.7%    | 80.2%    | 79.8% | 80.0%   |
| Stacking          | 80.0%    | 80.4%    | 79.5% | 80.0%   |

### 📊 **Regression Performance**
| Model               | MSE       | MAE   | R²    |
|----------------------|---------:|------:|------:|
| Linear Regression   | 2.34M    | 1059  | 96.2% |
| Random Forest       | 743,927  | 603   | 98.8% |
| XGBoost Regressor   | 773,095  | 604   | 98.7% |

**Key Takeaways:**
- Random Forest and Stacking classifiers achieved the best classification results.
- Regression models like Random Forest and XGBoost demonstrated high predictive power with minimal error.

---

## 📊 SHAP Analysis
- Key Features for Prediction:
   - **K/D Ratio**
   - **Gold Efficiency**
   - **Gold per Minute**
   - **Objective Control Score**
   - **Ward Efficiency**

**SHAP Insights:**
- High kill counts positively impact both classification and regression predictions.
- Early objective control (e.g., First Tower, Dragons) significantly influences match outcomes.

---

## 📝 Detailed Report
For a thorough explanation of the methodology, analysis, and findings, refer to the **[Final Report](./Final%20Report.pdf)**.

---

## 🚀 How to Run the Project

1. **Clone the Repository:**
   ```bash
   git clone <repo-link>
   cd lol-early-game-prediction
