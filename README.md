# Hotel Booking Cancellation Prediction — Classification & Hypothesis Testing  

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/ML-ScikitLearn-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## Objective  
Developed a machine learning–based solution for **INN Hotels Group** (Portugal) to predict hotel booking cancellations, enabling proactive policy design to reduce revenue loss, operational inefficiencies, and last-minute price cuts.  

---

## Key Highlights  

### **Exploratory Data Analysis (EDA)**  
- Analyzed **36,275 bookings** across **19 features**, identifying key drivers of cancellations such as **lead time**, **average price per room**, **market segment**, and **number of special requests**.  
- Detected anomalies (e.g., zero-price bookings linked to “Complementary” segment) and corrected unlikely values (e.g., unrealistic children counts).  
- Visualized correlations, booking patterns by month, and customer segments most prone to canceling.  

### **Data Preparation**  
- Encoded categorical variables, handled outliers via **IQR capping**, and used **stratified train-test splits** to preserve class distribution (**32.8% cancellations**).  
- Scaled features for SVM models and engineered derived metrics like **total stay duration**.  

### **Model Development**  
- Implemented and evaluated multiple classifiers:  
  - **Logistic Regression**  
  - **Support Vector Machine (Linear & RBF kernels)**  
  - **Decision Tree** (with hyperparameter tuning via GridSearchCV)  
  - **Random Forest**  
- Optimized thresholds using **Precision-Recall curves** to balance false positives and false negatives.  
- Reduced overfitting in tree-based models with tuned hyperparameters.  

---

## Model Performance  

| Model                         | Accuracy | Precision (Cancel) | Recall (Cancel) | F1-Score (Cancel) |
|--------------------------------|----------|--------------------|-----------------|-------------------|
| Logistic Regression            | 0.80     | 0.72               | 0.62            | 0.67              |
| SVM (Linear)                   | 0.80     | 0.74               | 0.61            | 0.67              |
| SVM (RBF)                      | 0.82     | 0.78               | 0.63            | 0.70              |
| Decision Tree (Tuned)          | 0.87     | 0.82               | 0.78            | 0.80              |
| **Random Forest** (Best Model) | **0.90** | **0.88**           | **0.80**        | **0.84**          |

---

## Business Recommendations  
1. **Incentivize long lead-time bookings** with perks to reduce cancellation risk.  
2. **Adjust pricing strategies** for high-risk segments to improve retention.  
3. **Use special requests as a retention indicator** — customers with more requests cancel less.  
4. Implement **targeted follow-ups** for online bookings, especially during peak months (**Aug–Oct**).  

---

## Tech Stack  
`Python` • `Pandas` • `NumPy` • `Matplotlib` • `Seaborn` • `Scikit-Learn`  

---

## Skills Demonstrated  
- Data Cleaning & Preprocessing  
- Exploratory Data Analysis (EDA)  
- Feature Engineering  
- Classification Modeling  
- Model Evaluation & Optimization  
- Business Insight Generation  

---

## Repository Structure  
```plaintext
├── data/                # Dataset files  
├── notebooks/           # Jupyter notebooks for EDA & modeling  
├── models/              # Saved trained models  
├── visuals/             # Plots & charts generated during analysis  
├── requirements.txt     # Python dependencies  
└── README.md            # Project documentation  
