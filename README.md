# Customer Churn Prediction

##  Problem Statement
Customer churn is a critical problem for telecom businesses as it directly affects revenue.  
This project aims to predict customers who are likely to churn using machine learning techniques.

---

##  Objective
- Identify customers at high risk of churn  
- Improve customer retention strategies  
- Support business decision-making  

---

##  Dataset
The dataset includes:
- Customer demographics  
- Service usage details  
- Contract and payment information  
- Billing data (Monthly & Total Charges)  
- Target variable: **Churn Label**

---

##  Data Preprocessing
- Handled missing values in Total Charges  
- Standardized categorical values  
- Cleaned and prepared data for modeling  

---

##  Exploratory Data Analysis
Key insights:
- Month-to-month contracts show higher churn  
- Customers with low tenure are more likely to churn  
- Higher monthly charges increase churn probability  
- Lack of technical support leads to higher churn  

---

##  Feature Engineering
- Created features such as total services and average charges  
- Grouped customers based on tenure  

---

##  Model Building

### Baseline Model
- Logistic Regression was used to establish initial performance  

### Final Model
- LightGBM was used as the main model to capture complex patterns  

---

##  Model Optimization
- Applied **GridSearchCV** for hyperparameter tuning  
- Tested multiple parameter combinations to find the best model  
- Used **threshold tuning** to improve recall for churn prediction  

---

# Model Evaluation

##  Logistic Regression (Baseline)

- Accuracy: **81%**
- Recall (Churn): **54%**

Although Logistic Regression achieved higher accuracy, 
it failed to identify many churn customers due to low recall.

---

##  LightGBM (Before Tuning)

- Accuracy: **76%**
- Recall (Churn): **81%**

LightGBM significantly improved recall, making it better 
at identifying churn customers compared to Logistic Regression.

---

##  LightGBM (After Tuning)

- Accuracy: **76%**
- Recall (Churn): **85%**

After applying GridSearchCV and threshold tuning, 
the model showed further improvement in recall, 
successfully identifying more high-risk customers.

---

##  Key Observation

- Logistic Regression → High accuracy, low recall  
- LightGBM → Slightly lower accuracy, but high recall  
- Tuned LightGBM → Best performance for churn detection  

---

##  Final Conclusion

Since the business objective is to identify churn customers, 
**recall is more important than accuracy**.

Therefore, the **tuned LightGBM model** was selected as the final model 
due to its superior ability to detect churn customers.

---

##  Business Impact
- Identifies customers likely to churn  
- Enables proactive retention strategies  
- Helps reduce customer loss and improve revenue  

---

##  Technologies Used
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- LightGBM  

---

##  How to Run
1. Open the notebook in Jupyter Notebook or Google Colab  
2. Install required libraries  
3. Run all cells  

---
