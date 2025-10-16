[🇧🇷 Para a versão em português, clique aqui.](./LEIA-ME.md)

---

# Project 01: Customer Churn Prediction Model

## 🎯 Business Objective
The goal of this project is to build a predictive machine learning model to identify customers who are at high risk of churning (canceling their service). By accurately predicting churn, the telecommunications company can proactively engage with these at-risk customers through targeted retention campaigns, ultimately reducing revenue loss.

## 📚 Libraries and Concepts Used
-   **Libraries:** `Pandas`, `Scikit-learn`
-   **Key Concepts:**
    -   **Machine Learning Workflow:** A complete, end-to-end process from data preparation to model evaluation.
    -   **Classification Problem:** Predicting a binary outcome (Churn vs. Not Churn).
    -   **Feature Engineering:** Selecting and preparing input variables (`tenure`, `MonthlyCharges`).
    -   **Train-Test Split:** `train_test_split` to ensure an unbiased model evaluation.
    -   **Model Training:** Using `LogisticRegression` as a baseline model.
    -   **Performance Evaluation:** Analyzing `Accuracy`, `Precision`, `Recall`, and the `Confusion Matrix`.

## 📖 Process Description
The project followed the standard machine learning workflow:
1.  **Data Preparation:** The "Telco Customer Churn" dataset was loaded using Pandas. The data was cleaned by handling non-numeric and missing values, and the target variable ('Churn') was converted into a binary format (0/1).
2.  **Train-Test Split:** The dataset was partitioned into an 80% training set and a 20% testing set to ensure the model could be validated on unseen data.
3.  **Model Training:** A Logistic Regression model was initialized and trained on the training data using the `.fit()` method.
4.  **Prediction:** The trained model was used to make predictions on the test set.
5.  **Evaluation:** The model's predictions were compared against the actual outcomes in the test set. The analysis focused not only on overall accuracy but critically on the confusion matrix to understand the business impact of different types of errors (specifically False Negatives).

## 📊 Results & Insights
The baseline Logistic Regression model achieved an **accuracy of ~78%**.

However, the key insight came from the **Confusion Matrix**. The model had a **low recall of 43%** for the churn class, meaning it failed to identify 57% of the customers who actually churned. These **False Negatives** represent the most significant cost to the business, as they are missed opportunities for retention.

## 💡 Conclusion
This project successfully demonstrates the entire process of building and evaluating a predictive model. While the baseline model provides a solid starting point, the analysis concludes that it is too "conservative" for a real-world application.

**Next Steps:** Future iterations would focus on improving the model's recall by:
-   Engineering more complex features.
-   Testing more advanced algorithms (e.g., Random Forest, Gradient Boosting).
-   Applying techniques to handle class imbalance.