# Data Scientist Salary Prediction in NYC Based on Job Result Features by Mai Tran

# Minimum Viable Product (MVP)
1. Successfully web scraped 962 NYC Data Scientist job posts from Indeed for Linear Regression Analysis. Data set made up the following target variable and features: JobNum, JobTitle, Company, Location, CompanyRating, Salary, Remote, Urgent, EasilyApply, PostedDate, ExtractedSalary (target variable), PostAge. 

2. Since 70% of job posts were 30+ days old, they were filtered out. Only job posts younger than 30 days old were analyzed for Linear Regression. Linear Regression showed best fit between training and validation data when all features were analyzed except for EasilyApply. Mean absolute error: 14.8 for training data, and 13.3 for validation data as shown with both code and graph below: 

