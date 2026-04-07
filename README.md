# Credit Risk & Probability of Default Analysis

A data-driven credit risk model built on 100,000+ SME loan records to help lenders identify high-risk borrowers, assess creditworthiness before approval, and reduce bad debt through predictive scoring.

---

## Business Problem 
Small and medium enterprise (SME) lending carries significant default risk. Banks and NBFCs need a reliable, data-backed way to:

 - Predict which borrowers are likely to default before disbursing a loan
 - Assess creditworthiness using borrower financial and demographic signals
 - Reduce bad debt by flagging high-risk profiles early in the approval process

This project simulates a real-world credit risk workflow — from raw loan data to a scored, interpretable model that a credit analyst could act on.

---

## Dataset
100,000+ SME loan records
Features include: loan amount, tenure, interest rate, borrower financials, employment type, credit history, and repayment behaviour
Target variable: default (1 = defaulted, 0 = repaid)

---

## Approach  
### 1. Exploratory Data Analysis

Identified class imbalance (defaults are rare events)
Analysed distributions of key risk drivers: loan-to-income ratio, credit history length, delinquency flags
Visualised default rates across borrower segments

### 2. Data Preprocessing

Handled missing values using median imputation and mode fill
Encoded categorical variables (employment type, loan purpose)
Feature engineering: derived debt-to-income ratio, repayment stress index
Train/test split with stratification to preserve default ratio

### 3. Model Building

Logistic Regression (primary model — interpretable for credit risk context)
Evaluated with ROC-AUC, Precision-Recall curve, confusion matrix
Threshold tuning to balance false negatives (missed defaults) vs false positives (wrongly rejected borrowers)

---

## Results
ROC-AUC  0.80
Model    Logistic Regression
Records  100,000+

An ROC-AUC of 0.80 means the model correctly ranks a defaulter above a non-defaulter 80% of the time — a strong baseline for a binary credit risk classifier.
---

## 🔗 Project Assets  
- 📄 [Project Documentation (Google Doc)](https://docs.google.com/document/d/1PNo-soZtDdzU0iG_qEZ6Rxp3yacSM5BRRa1WvY32g34/edit?usp=sharing)

---

## Key Insights
 - Debt-to-income ratio was the single strongest predictor of default
 - Borrowers with no prior credit history had 2.3x higher default rates
 - Short-tenure, high-interest loans showed disproportionate default clustering
 - Model identified a high-risk segment (top 20% of scores) that accounts for ~65% of all defaults — enabling targeted intervention
   
---

## Business Impact
A credit team using this model could:

  - Reject or flag the top-risk decile before disbursement
  - Reduce expected default losses by prioritising manual review on borderline cases
  - Use the probability score as an input into loan pricing (higher risk → higher rate)
    
---

## Tools & Technologies
Python · Pandas · Scikit-learn · Matplotlib · Seaborn · Excel · SQL
    

