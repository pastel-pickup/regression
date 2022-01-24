# Data Scientist Salary Prediction in NYC Based on Job Result Features by Mai Tran

# Minimum Viable Product (MVP)
1. Successfully web scraped 962 NYC Data Scientist job posts from Indeed for Linear Regression Analysis. Data set made up the following target variable and features: JobNum, JobTitle, Company, Location, CompanyRating, Salary, Remote, Urgent, EasilyApply, PostedDate, ExtractedSalary (target variable), PostAge. 
2. <img width="503" alt="jobs_df_ex" src="https://user-images.githubusercontent.com/67651332/150877112-1aa58ae9-f622-4634-98ad-d5cc5c6abaa5.PNG">

2. Since 70% of job posts were 30+ days old, they were filtered out. Only job posts younger than 30 days old were analyzed for Linear Regression. Linear Regression showed best fit between training and validation data when all features were analyzed except for EasilyApply. Mean absolute error: 14.8 for training data, and 13.3 for validation data as shown with graph below: 
3. ![train_valid](https://user-images.githubusercontent.com/67651332/150876624-c0e131c1-0950-4d32-a544-4e4b58ee6a9c.png)

Next Steps:
1. Test model on all data including posts of 30 days and older
2. Do similar modelling for other data job titles such as Data Engineer, Data Analyst, and Machine Learning Engineer
