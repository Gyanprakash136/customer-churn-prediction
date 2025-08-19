# 📊 Customer Churn Prediction (Logistic Regression from Scratch)

## 🔹 Overview  
This project predicts **customer churn** for a telecom company using **Logistic Regression implemented from scratch** (without using `sklearn`'s LogisticRegression).  
The goal is to identify customers who are likely to leave (churn) so that businesses can take preventive measures and reduce revenue loss.  

---

## 🔹 Problem Statement  
Customer churn is a critical business problem for subscription-based services. Acquiring new customers is often more costly than retaining existing ones.  
This project builds a **binary classification model** to predict whether a customer will **Churn (Yes)** or **Not Churn (No)** based on their demographic, account, and service details.  

---

## 🔹 Dataset  
- **Source**: [Telco Customer Churn Dataset (Kaggle)](https://www.kaggle.com/blastchar/telco-customer-churn)  
- **Rows**: 7043 customers  
- **Columns**: 21 (features + target)  

### Key Features:
- `gender`, `SeniorCitizen`, `Partner`, `Dependents` → Demographics  
- `tenure`, `MonthlyCharges`, `TotalCharges` → Account information  
- `PhoneService`, `InternetService`, `OnlineSecurity`, `TechSupport`, etc. → Services subscribed  
- `Contract`, `PaperlessBilling`, `PaymentMethod` → Billing details  
- **Target Variable**: `Churn` (Yes = 1, No = 0)  

---

## 🔹 Project Workflow  
1. **Data Preprocessing**  
   - Handle missing values  
   - Convert categorical variables (One-Hot Encoding)  
   - Scale numerical features  
   - Handle correlated features (drop `TotalCharges` due to high correlation with `tenure × MonthlyCharges`)  

2. **Exploratory Data Analysis (EDA)**  
   - Churn distribution (Yes/No)  
   - Churn vs Contract Type  
   - Tenure distribution by churn status  
   - Monthly Charges vs Churn  
   - Payment Method vs Churn  
   - Correlation heatmap (numerical features)  

3. **Model Development (From Scratch)**  
   - Implement **sigmoid function**  
   - Implement **binary cross-entropy loss**  
   - Implement **gradient descent optimization**  
   - Train logistic regression from scratch  
   - Compare with `sklearn`'s LogisticRegression  

4. **Model Evaluation**  
   - Accuracy, F1-Score  

---

## 🔹 Key Insights from EDA  
- Customers with **month-to-month contracts** churn the most.  
- **High monthly charges** are strongly linked with churn.  
- Customers with **short tenure (<12 months)** churn more.  
- Customers without **TechSupport or OnlineSecurity** are more likely to churn.  
- **Electronic check payment method** has the highest churn rate.  

---

## 🔹 Results  
- Logistic Regression (from scratch) achieved **~80% accuracy**.  
- Adding regularization improved stability and prevented overfitting.  
- Model performance was close to sklearn’s LogisticRegression baseline.  

---

## 🔹 Business Impact  
- Early churn prediction helps reduce **customer acquisition cost (CAC)**.  
- Telecom companies can design **retention strategies** (discounts, bundled services, better support).  
- Example: Reducing churn by 5% could save millions in revenue annually.  

---

## 🔹 Tech Stack  
- **Python** (Numpy, Pandas, Matplotlib, Seaborn)  
- **Logistic Regression implemented from scratch**  
- **Jupyter Notebook / Google Colab**  

---

## 🔹 How to Run  

1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/customer-churn-logistic-regression.git
   cd customer-churn-logistic-regression
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Run Jupyter Notebook or Python script:

bash
Copy
Edit
jupyter notebook Churn_Prediction.ipynb
🔹 Future Improvements
Implement Regularized Logistic Regression (L1/L2)

Handle class imbalance with SMOTE / resampling

Try other models (Random Forest, XGBoost, Neural Networks) for comparison

Deploy as a simple Flask/Django API for real-time predictions

🔹 Author
👤 Gyan Prakash
📧 gyan.official.work0902@gmail.com
🔗 LinkedIn[https://www.linkedin.com/in/gyan-prakash-7bb196262/] | GitHub[]https://github.com/Gyanprakash136]
