### **Customer Churn Prediction**

---

#### **Overview**

This project aims to predict customer churn for a telecommunications company based on various customer attributes. By analyzing a dataset with demographic and usage data, we explore factors that may contribute to customer churn and train machine learning models to predict churn probability. The analysis involves data cleaning, feature engineering, exploratory data analysis (EDA), and model training, using Random Forest and Logistic Regression models to predict churn.

---

#### **Project Structure**

1. **Data Preparation**
   - Load and clean the dataset.
   - Convert data types for consistency (e.g., `totalcharges` to numeric).
   - Handle missing values and ensure proper data formatting.

2. **Exploratory Data Analysis (EDA)**
   - Hypothesis generation based on domain knowledge about churn factors.
   - Visual analysis of customer characteristics influencing churn:
     - Senior citizens' churn rates.
     - Impact of gender, dependents, tenure, internet service, and payment methods on churn.
   - Statistical testing (Chi-square test) for feature significance in relation to churn.

3. **Feature Engineering**
   - Label encoding for categorical features.
   - One-hot encoding for creating binary features.
   - Combining numerical and encoded categorical features into a final dataset.

4. **Model Training**
   - Split data into training and testing sets.
   - Apply SMOTE for balancing the class distribution in the training set.
   - Train machine learning models:
     - Random Forest Classifier.
     - Logistic Regression.
   - Evaluate model performance using accuracy.

5. **Model Evaluation**
   - Feature importance analysis from the trained Random Forest model.
   - Save the trained model for production use.

---

#### **Key Features**

1. **Data Cleaning & Organization**
   - Removal of irrelevant columns.
   - Conversion of `totalcharges` from string to numeric values.
   - Imputation of missing values.
   
2. **Exploratory Data Analysis (EDA)**
   - Hypothesis-driven analysis of customer churn based on various attributes like tenure, internet service, payment method, etc.
   - Visualization of churn distribution across features using count plots and histograms.

3. **Feature Engineering**
   - Label encoding for categorical variables.
   - One-hot encoding to convert categorical variables into a machine-readable format.
   
4. **Modeling**
   - Random Forest Classifier and Logistic Regression models are used for churn prediction.
   - SMOTE is used to handle imbalanced class distribution.
   - Feature importance is extracted from the Random Forest model to interpret significant predictors of churn.

---

#### **Tools & Libraries**

- **Data Manipulation:** pandas, numpy
- **Visualization:** matplotlib, seaborn
- **Modeling:** scikit-learn (RandomForestClassifier, LogisticRegression), imbalanced-learn (SMOTE)
- **Serialization:** pickle (for saving the model)

---

#### **Insights**

- **Customer Demographics:** Senior citizens, customers with shorter tenure, and those without additional services like tech support are more likely to churn.
- **Service Usage:** Customers with Fiber optic internet service tend to churn less. Similarly, customers with higher monthly charges and no credit card payment method are more likely to churn.
- **Feature Importance:** The most important features influencing churn prediction include tenure, monthly charges, and tech support.

---

#### **Next Steps**

- **Model Tuning:** Explore hyperparameter tuning for the Random Forest model to improve accuracy.
- **Additional Features:** Investigate the impact of additional features like customer satisfaction scores, marketing efforts, or seasonal trends.
- **Model Deployment:** Implement the trained model into a production environment for real-time churn prediction.

---

#### **Acknowledgments**

This analysis utilizes open-source libraries for data processing, machine learning, and visualization. Special thanks to the contributors of these libraries and the dataset provider for making the data available for analysis.
