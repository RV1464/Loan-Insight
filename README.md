# Loan-Insight
## Abstract
In this project, a financial institution aims to predict when customers are likely to take a top-up loan. By analyzing both current and historical loan data, the objective is to identify opportunities for offering top-up loans to customers either during the active period of an existing loan or after its closure. The dataset includes detailed information about the current loans and other loans held by customers, encompassing borrower details, loan specifics, and asset information. The project involves exploratory data analysis (EDA), feature selection, and model development to create a predictive model that can identify high-potential customers for top-up loans. This predictive model can enhance the efficiency of the bank's call center operations by targeting only those customers with a higher likelihood of requiring additional loans.

## Detailed Report
### 1. Data Discovery
The data for this project includes two primary sources:

Current Loan Details: Information about each loan such as Borrower ID, Monthly Income, Address, Loan Frequency, Installment mode, Payment mode, Tenure, Authorization date, Maturity Date, Disbursal amount, and Loan-to-Value ratio.
Bureau Details: Records of other loans taken by the customer, both from the same bank and other financial institutions.
The data dictionary provides a clear explanation of the fields included in these datasets.

### 2. Data Exploration
Initially, data exploration was performed using basic Pandas functions:

info(): To get a concise summary of the dataset.
describe(): To generate descriptive statistics.
head(): To view the first few records.
shape(): To understand the dimensions of the dataset.
After receiving guidance from the instructor, I utilized pandas_profiling for a more comprehensive analysis, which provided detailed insights into the data distributions, missing values, correlations, and other important characteristics.

### 3. Data Aggregation
Data from the bureau table was aggregated and merged with the training data to create a comprehensive dataset that includes all relevant loan information for each customer. This process involved:

1. Joining the current loan details with the bureau details.
2. Summarizing the number of other loans, total amount borrowed, and repayment history for each customer.
### 4. Feature Selection
Feature selection was performed using Random Forest and Logistic Regression techniques to identify the most important variables for predicting top-up loan opportunities. This step included:

Evaluating the feature importance scores from the Random Forest model.
Using recursive feature elimination with Logistic Regression to refine the feature set.
### 5. Model Selection and Building
Without a provided test dataset, the original dataset was split into training (75%), validation (15%), and test (15%) sets. Three machine learning models were developed and compared:

Random Forest: For its ability to handle large datasets and complex interactions.
Logistic Regression: As a baseline model for its simplicity and interpretability.
XGBoost: For its superior performance in many classification tasks.
### 6. Model Evaluation and Comparison
The models were evaluated using metrics such as accuracy, precision, recall, and F1-score on the validation and test sets. Model comparison involved:

Assessing the performance of each model on the validation set.
Fine-tuning hyperparameters to optimize model performance.
Selecting the best-performing model based on the evaluation metrics.
## Conclusion
The developed predictive model identifies customers with a high likelihood of taking a top-up loan, thereby enabling the bank to target these customers effectively. This targeted approach not only improves the efficiency of the call center operations but also enhances customer satisfaction by offering timely and relevant financial products. The project's methodology, from data discovery to model evaluation, demonstrates a comprehensive approach to leveraging machine learning for predictive analytics in the banking sector.
