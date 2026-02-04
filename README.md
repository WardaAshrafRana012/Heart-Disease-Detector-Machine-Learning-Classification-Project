# Heart-Disease-Detector-Machine-Learning-Classification-Project
Heart disease prediction system using Logistic Regression and Random Forest classifiers, featuring feature selection, model comparison, and performance evaluation using accuracy, precision, recall, and specificity.
# 🩺 Heart Disease Detector: Comparative Analysis & ML Modeling
**Project By: Warda Ashraf Rana , Ammaar Mustaq , Shahzaib Khan**

## 1. Introduction
Heart disease prediction is a critical application of machine learning in healthcare. This project focuses on building a binary classification system that identifies high-risk patients. The core challenge was to balance **Accuracy** with **Recall** to ensure that potential health risks are not missed (minimizing False Negatives).

## 2. Objectives
* Perform **Exploratory Data Analysis (EDA)** on cardiovascular health data.
* Implement **Feature Engineering** to improve model performance.
* Compare **Random Forest Classifier** and **Logistic Regression**.
* Determine the optimal data split (70-30, 75-25, 80-20) for predictive reliability.

## 3. Tech Stack
* **Language:** Python
* **Environment:** Google Colab / Jupyter Notebook
* **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

## 4. Feature Selection & Preprocessing
To reduce noise and prevent model overfitting, specific features were analyzed:
* **Dropped Features:** `skin triceps` and `bp_diastolic` were removed as they showed low correlation or redundancy with other key indicators like `bp_systolic`.
* **Normalization:** Data was scaled to ensure that features like `BMI` and `Annual Income` didn't skew the model weights.
* **Correlation Analysis:** Used a Seaborn Heatmap to prioritize features most relevant to the target label.

## 5. Model Comparison (Results)
The models were tested across multiple splits. The **80-20 split** provided the most stable results.

| Metric | Random Forest (Best) | Logistic Regression (Best) |
| :--- | :--- | :--- |
| **Accuracy** | 90.65% | **90.84%** |
| **Recall (Sensitivity)** | 0.89% | **12.99%** |
| **Specificity** | **99.97%** | 98.92% |
| **Precision** | **73.68%** | 55.57% |
| **False Positive Rate** | **0.00033** | 0.01078 |

### 🏆 Conclusion: Why Logistic Regression won?
While **Random Forest** had an incredibly low False Positive Rate, its **Recall (0.89%)** was too low for a medical setting. **Logistic Regression** was chosen as the superior model because it successfully identified significantly more true positive cases (12.99% Recall) while maintaining high overall accuracy.

## 6. How to Run this Project
1. Clone the repository: `git clone https://github.com/YourUsername/Heart-Disease-Detector.git`
2. Open `Heart_Disease_Analysis.ipynb` in Google Colab or Jupyter.
3. Install dependencies: `pip install pandas scikit-learn matplotlib seaborn`
4. Run all cells to see the comparison plots and metrics.

