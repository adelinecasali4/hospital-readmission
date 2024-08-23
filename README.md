# Identifying Risk Factors and Preferred Hospitals for Hip/Knee Replacements: An Analysis of 2019-2022 Hospital Readmission Reduction Program Data  

## Project Overview  
Since 2012, the Centers for Medicare and Medicaid Services (CMS) have implemented the Hospital Readmission Reduction Program (HRRP) to track and reduce unnecessary hospital readmissions through financial penalties. This project aims to analyze 2019-2022 HRRP data to identify preferred and non-preferred hospitals for hip and knee replacements for a health insurance company, as well as to determine the risk factors associated with higher readmission rates for these procedures.  

## Background and Question
Since 2012, the Centers for Medicare and Medicaid Services have implemented the Hospital Readmission Reduction Program (HRRP). This program tracks hospital readmission rates and incentivizes hospitals to reduce unnecessary readmissions through financial penalties. Using the 2019-2022 readmission data from the HRRP, this analysis aims to identify the preferred and non-preferred hospitals for hip and knee replacements for a health insurance company. Furthermore, it will examine the risk factors associated with higher readmission rates for these procedures.  

##### Question:  
What risk factors are associated with hospital readmission rates for hip/knee replacements?  

##### Motivation:  
Understanding these risk factors can help health insurance companies guide patients towards hospitals with better outcomes, thereby improving patient outcomes and reducing costs associated with readmissions.  

##### Need:  
The insights from this analysis can be used to improve hospital performance, enhance patient care, and reduce costs. As of 2019, the average cost of readmission after hip/knee surgery was $8,588, and avoiding that cost would be highly beneficial for health insurance companies and consumers alike (Phillips et al., 2019).  

##### Novelty:  
Previous analyses have used these same or similar datasets with Logistic Regression and Random Forest models to identify the most important risk factors as they pertain to hospital readmission rates for hip/knee replacements. We will be trying to improve on this type of analysis by improving the performance of the models using various techniques. Prior analyses have implemented Random Forest models to extract important risk factors, but no prior analyses have used Random Forest to classify hospitals as preferred or non-preferred for hip/knee replacement, based on the important risk factors.  

##### Hypothesis:  
Hospitals with better Hospital Consumer Assessment of Healthcare Providers and Systems (HCAHPS) scores will have lower readmission rates for hip/knee replacements because higher patient satisfaction often correlates with better overall care quality and patient outcomes, including reduced complications and better post-discharge support (Edwards et al., 2015).  

## Data and Analysis
We will be using the datasets from the Centers for Medicare and Medicaid Services (Centers for Medicare & Medicaid Services, 2024). Our target variable will be the readmission rate after hip/knee surgery, using the 2019-2022 data as the training data and updated 2024 data as the test data. We will utilize predictors from the HCAHPS (Hospital Consumer Assessment of Healthcare Providers and Systems) dataset as well as Timely and Effective Care, containing information on average wait times and vaccination compliance, Complications and Deaths, containing information about the frequency of deaths and complications for procedures, and Payment and Spending metrics, which includes the costs associated with procedures. 

### Analysis Plan:
1.	Data Preprocessing:  
o	Handle missing values, outliers, and inconsistencies in the dataset.  
o	Exploratory data analysis will be performed.  
2.	Model Selection:  
o	Random Forest: This model will be used to determine the most significant risk factors associated with hospital readmission, post hip/knee replacement surgery. The model will then be used in a binary classification task, which will categorize hospitals as either “preferred” or “non-preferred”, based on the national average for hospital readmission post hip/knee surgery.  
o	Elastic Net: While prior analyses have used coefficients from Logistic Regression modeling to determine significant risk factors, this analysis will leverage L1 and L2 regularization via an Elastic Net model.   
o	Neural Network: After using Elastic Net and Random Forest to find significant risk factors, these risk factors will be utilized in a neural network model and used to classify hospitals as either “preferred” or “non-preferred”. Classification ability of the neural network model will then be compared with the classification ability of the Random Forest model.   
3.	Feature Importance Analysis:  
o	Identify which predictors significantly influence hospital readmission rate, post hip/knee replacement surgery.  
o	Linear regression analysis (Elastic Net) significant risk factors will be compared to tree-based analysis (Random Forest) significant risk factors for overlap.  
4.	Model Validation:  
o	Validate the model using cross-validation techniques (k-fold, nested) to ensure robustness and generalizability.  
o	Hyperparameter tuning will be performed. Assessment of the model’s performance will be based on accuracy, AUC, and ROC metrics.  
o	The 2024 data will be used as the test set for this analysis.  

### Assessment:
##### Successful Analysis:  
We will consider our analysis successful if we can identify clear risk factors associated with hospital readmission rates and accurately classify hospitals as preferred or non-preferred.  

##### Hypothesis Support:  
Our hypothesis will be supported if hospitals with better HCAHPS scores demonstrate statistically significantly lower readmission rates for hip/knee replacements.  

##### Pitfalls:  
A potential pitfall of our analysis plan is data quality and completeness. The dataset does contain missing values, and it will need to be preprocessed to handle these missing values, outliers, and inconsistencies. Another potential pitfall is not having adequate computing power to implement deep learning with the size of our dataset. Lastly, a pitfall that we need to keep an eye out for is overfitting. We will know we have overfitting if the train set far outperforms the test set, in terms of model accuracy. 
