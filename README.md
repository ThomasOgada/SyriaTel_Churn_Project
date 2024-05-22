# SyriaTel Churn Project.
### Project Overview.
This project is about SyriaTel, a telecommunication company based in Syria in the Middle has a telecommunications sector experiencing rapid growth in mobile and internet penetration. 
The company plays a vital role in connecting people and businesses.
However, increasing competition and evolving customer preferences pose challenges for customer retention.
Understanding and addressing the drivers of churn are crucial for SyriaTel to sustain business success and enhance customer satisfaction.
Customer churn is a phenomenon where customers cease doing business with a company, is a critical concern for telecommunications companies like SyriaTel.
Retaining customers is essential for maintaining revenue and growth in this competitive industry. 
Identifying factors contributing to churn, such as service dissatisfaction or competitive offers, SyriaTel can take targeted actions to mitigate churn and improve customer retention.

## Problem Statement
SyriaTel, a telecommunications company, faces the challenge of customer churn, where customers discontinue their services. This attrition impacts revenue and profitability. The business seeks to proactively identify customers at risk of churning and implement effective retention strategies to mitigate revenue loss and maintain customer loyalty.

Specifically, the project aims to address the following questions:

1.What are the primary factors driving customer churn for SyriaTel?

2.Which machine learning modelling technique to apply in accurately predicting Churn so as to take proactive measures?

3.What actionable insights can SyriaTel derive from the predictive model to improve customer retention efforts?

4.What strategies can SyriaTel put in place to reduce churn rate?.
### Main Stakeholders
Main Stakeholders:
Senior Management: Interested in overall business impact and strategic insights for decision-making.
Marketing Team: Needs to design targeted retention campaigns based on model predictions.
Customer Service Team: Requires insights to proactively address customer issues and improve service.
Data Science Team: Responsible for developing, validating, and maintaining the predictive model.
IT Department: Supports data infrastructure, model deployment, and integration with existing systems.
Sales Team: Uses insights to enhance customer interaction and retention efforts.
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/1a7617f7-27e6-49c7-a62e-2a3d224150fe)

## Methodology
### Data Collection: 
Gather and preprocess customer data, including numerical, categorical, and string columns.
For purposes of this project, the 'SyriaTel_df.csv' dataset was used.
The dataset had 3,333 rows and 21 columns
The columns provided had numerical, categorical and string  data types.
### Data Preparation.
Outlier identification and handling.
One hot and Cording Categorical Columns.
After Data preparation, a dataframe of 3,333 rows and 67 columns were adopted for further analysis. 
Main columns colums considered for the analysis included
Numerical Colums :'Account Length', 'Area Code', 'Number Vmail Messages', 'Total Day Minutes', 'Total Day Calls', 'Total Day Charge', 'Total Eve Minutes', 'Total Eve Calls', 'Total Eve Charge', 'Total Night Minutes', 'Total Night Calls', 'Total Night Charge', 'Total Intl Minutes', 'Total Intl Calls', 'Total Intl Charge', 'Customer Service Calls‘
Categorical Columns: “State”, “International Plan, “Voice Mail Plan”,”Churn”
### Data Analysis: 
Perform exploratory data analysis (EDA) to identify key churn indicators.
Assesing descriptive statistics of the dataset.
visualizing outputs in Barcharts, Histograms, scatterplots and Heatmap to understand the
distribution and correlation of various features.
Computing the normality and spread of the numerical variables.
Inferential Statistics Hypothesis testing using ANOVA(Analysis of Variance)
### Feature Engineering: 
Encode categorical variables including State', 'International Plan', 'Voice Mail Plan', 'Churn'.
normalizing all the features using the  StandardScaler MinMax.
### Model Building: 
Feature Engineering
One Hot Encoding(Dealing with categorical Data)
Normalization/Standadization
Split- Train Test
Model Evaluation
Use machine learning models such as Logistic Regression, Decision Trees, KNN, and XGBoost.
### Model Evaluation: 
Validate models using k-fold cross-validation and select the best-performing model.
Deployment: Implement the model to predict churn and support retention strategies.

## Results.
Geographical Location of the Syria.
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/3230a47c-896f-4995-9842-6bb02761967e)

### Descriptive Statistics
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/79aff6f9-c73b-4f8d-924e-2a94a17066f9)
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/815ab5d4-b6a9-48e6-b885-fb2e97998cbe)
Total number of customer is 3,333.
Mean account length 101.1.
Max account length 243.
Mean Total Day Calls is approximately 100 calls.
Max Total Night Calls is 175.
Std for Total Day Change is 9.3.
Max Customer Service Calls is 9.
### Univariant Analysis
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/ad812dc7-5c37-4676-910a-cd39724baead)
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/4cf61821-bd0c-4a4c-9078-e734c93fd038)
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/18776527-2608-42a7-b570-ad1d07ca8557)
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/3ff728a2-770e-41a2-b493-6e9823fb6ff0)
Account length is positively skewed.
Total Intl Calls is positively skewed.
Total Day Minutes is nearly uniformly distributed.
Majority of customers do not use the Voice Mail Messages.
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/74831997-05d3-4213-9c5c-9b22a4c0ce62)
#### Distribution of Churn per State
Below plots shows how the churn customer are distriuted per State.
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/a49a5c0c-666f-49a0-96e7-a9b564f4fce8)
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/3e1f8ed2-0cfb-4fd5-bb9a-a52b64712de1)
WV state has the highest number of customers.
CA state has the lowest number of customers.
Other states with considerable number of customers include:
MN, NY,AL,WI,CR,CH among others.
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/c109b7dd-4cd0-4869-a180-9ad6714b50d0)

### Bivariant Analysis
#### Distribution per Customer Category
Customers were categorised into Relatively New, Retained, Sticky and Loyalists.
Customers with with account length <= 50 "Relatively New"
Where account lenght <= 100 "Retained Customers"
Where Account length <= 150 "Sticky Customers"
Else "Loyalists".
The distiribution was as below:
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/a8650115-ea8d-4808-a586-afcedf1656e3)
Results indicated that:
•	Retained and Sticky customer categories have majority of the churn.
•	Loyalists and relatively new customers have least least churn.
•	Majority of the total customers are under the Retained and Sticky customer categories.
### Multivariant Analysis
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/020dda03-b458-4431-8963-1691f8218e97)
The scatter plot shows the distirituibion of churn and not churn using two numerical columns such as Total Minutes,Total Day Minutes.

### Data Preparation
#### Idenfying Outliers
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/763eb9b9-6d26-476b-a8a5-3a6e68ef4bc3)
Indicating numerical columns with outliers.
Distributions before and after handling outliers
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/970afa1f-3d83-4222-ab12-3a570474a946)
Distributions of the numerical columns after removing outliers.
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/8432b1f8-ec2c-442c-9bc9-d38fac89601c)
### Normality and Spread
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/ca0f0808-5b24-4bfe-be31-20821e4e1feb)
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/b9e7bfe5-ebf0-4252-899b-f2cb44334e76)
Account length is positively skewed.
Total Intl calls is negatively skewed
Total Day Minutes has the highest std.
Total Intl Charge has the lowest std.
Avg Total Day Charge is 30.5
Avg Total Eve Calls is 100.1
Avg Intl minutes 10.2
### Correlation Matrix
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/0b337bfe-cf12-4f82-b7a6-66b0beb15df1)
Results indicated that features that are highly correlated included:
Total Day Charge and Total Day Minutes.
•	Total Eve Charge and Total Eve Minutes.
•	Total Night Charge and Total Nights Minutes
Total Intl charge and Total Minutes.
•	This offers insights on opportunities for better packages and loyalty programs.

### Hypothesis Testing 
Null Hypothesis (H0): There is no significant influence of the various factors to churn rate in SyriaTel.

Alternate Hypothesis (H1): There is a significant influence of the various factors to churn rate in SyriaTel.
Results were as follows 
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/3daadf09-10cc-4e08-938c-4a097cc4ae22)

Conclusion
Features such as 'Account Length', 'Area Code', 'Total Day Calls', 'Total Eve Calls', and 'Total Night Calls' have their p-values are greater than the significance level of 0.05. Therefore, we fail to reject the null hypothesis (H0) for these features. This suggests that there is no significant influence of these factors on the churn rate in SyriaTel.

Remaining features including 'Number Vmail Messages', 'Total Day Minutes', 'Total Day Charge', 'Total Eve Minutes', 'Total Eve Charge', 'Total Night Minutes', 'Total Night Charge', 'Total Intl Minutes', 'Total Intl Calls', 'Total Intl Charge', and 'Customer Service Calls', the p-values are extremely low (close to 0). Therefore, we reject the null hypothesis (H0) for these features. This indicates that there is a significant influence of these factors on the churn rate in SyriaTel.

In conclusion, there was evidence to suggest that most numerical features have a significant influence on the churn rate in SyriaTel, except for 'Account Length', 'Area Code', 'Total Day Calls', 'Total Eve Calls', and 'Total Night Calls'

## Modeling
Models performed included Logistic Regression, Decision Tree, KNN and XGBoost models have been built to answer the research questions.

Data Split criteria
# Split the data into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.20, random_state=1, stratify=y)

### Baseline Logistic Regression Model
From the above split, logististic regression model was performed.
Results:
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/cbc2387e-31d2-43c5-82f6-45b655801585)
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/0a5648c0-a02d-408f-84a8-339c36a4b784)
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/364c2e58-5e54-41b2-b40d-a30289cb3400)
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/e8f2f039-2dee-40b4-9f54-e6e08ebbe75d)

•	The model has high accuracy but struggles with precision and recall for the churn class.
•	Suggesting that while it correctly predicts the majority of 'no churn' cases,
•	It fails to adequately identify 'churn' cases.
•	Therefore the need to consider other model techniques
### Decision Tree Model
Given the above performance, a decision tree model was conducted that gave below results.
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/a3c0163c-e351-45e6-9031-ee33b71e1a9d)
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/5d4b088c-0968-4769-a1a6-5d5339858f83)
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/149e762b-a28a-47e5-a413-a9639d816764)

Observations
While the Decision tree model has improved in terms of accuracy, precion,Recall and F1-Score,
It has a lower ROC-AUC meaning that it may predict alot of false positives which may in this case mean predicting alot of Churn which may not be the true case.
Based on the above comparison, we proceed to perform other models.

### KNN model
With use of the appriapriate libraries, split data a KNN model was perform.
Results 
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/8212699e-49fc-44a3-86ac-14df35bf0f3e)
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/da569268-88b8-4b4f-9189-e4cfd4e5c77b)
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/e8aa0846-285f-4fc1-a4b6-be03d99dc3c8)

KNN Model Performance:
Accuracy: 0.8575712143928036
Precision: 0.6
Recall: 0.09183673469387756
F1-Score: 0.1592920353982301
ROC-AUC Score: 0.5406459596140741
•	The accuracy is reduced while it has a higher ROC-AUC Score compared with the previous model.
As this was not convincing, another model model was performed.

### XGBoost Model
Relevant libraries were loaded,
XGBoost Model was performed gave the following results.
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/a3830d71-834b-4858-8a6c-699bf5299c2d)
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/324f86f3-da53-4dc6-a4c3-7e61a5c0484e)
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/712e9a6d-386f-4f6f-a601-8ca813bfe0e0)


# Model Performance Comparison
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/7c8cd633-f49a-4c6f-b94d-b33cfe589d14)
![image](https://github.com/ThomasOgada/SyriaTel_Churn_Project/assets/151352742/036154e6-d05d-4256-868c-35c897cce8e2)
XGBoost Model Performance:
Accuracy: 0.9460269865067467
Precision: 0.8690476190476191
Recall: 0.7448979591836735
F1-Score: 0.8021978021978022
ROC-AUC Score: 0.8837380294824432

Based on the above score, a for loop function was implemented to identfiy the best performing model.
The results were as follows.
![Uploading image.png…]()

XGBoost Model was identified as the best performing model.

### Cross Validation of the Best performing Model.
A cross validation was done with a k = 5.
The results were as below.
Logistic Regression: Average Cross-validation Score = 0.8668
Decision Tree: Average Cross-validation Score = 0.9096
KNN: Average Cross-validation Score = 0.8571
XGBoost: Average Cross-validation Score = 0.9542
Indicating that XGBoost had the highest Average Cross-validation Score = 0.9542.
### Hyperparameter tuning on the XGBoost Model
In order to improved the performance of the model, hyperparameter tuning was conducted on the model.
The results indicated that:
![Uploading image.png…]()


### Variable of Importance 
Identify important variables that SyriaTl can keep monitoring, variable of importance indicated the following variables were identified as Variables of Importance in descending order include.
•	Total Day Minutes
Total Eve Minutes
•	Total Night Minutes
•	Total Night Calls
•	Account Length
•	Total Eve Calls
•	Customer Service Calls
•	Total Intl Calls
•	Intl Pla
•	Number of Vmail Messeges
•	This provides insights of the variables to consider in developing churn mitigation strategies




















