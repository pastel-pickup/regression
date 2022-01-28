# Predicting Data Science Salaries Based on Job Post Features on Indeed.com
Mai Tran

# Abstract
With the explosion in data and data science jobs, it is important explore the job market for data professionals using data science job post features, and to explore underlying predictive relationships between various job post features to predict data role salary. These features include Company Rating, Remote vs Non-Remote, Old vs New (old = older than 29 days), Non-Urgent vs Urgent, Easily Apply vs No Easily Apply, Job Title, Company, and Location. It was found these features vary widely between different data roles, so it is recommended to have a predictive model for each data role. 

# Design
1) Data Harvesting - utilized BeautifulSoup to scrape data jobs for Data Scientist (1025 jobs), Data Analyst (1053 jobs), Data Engineer (664 jobs), and Machine Learning Engineer (1002 jobs) roles resulting in 3,744 unique jobs in overall dataset with at least nine of the following features: Salary, Company Rating (low is < 3.5), Remote vs Non-Remote, Old vs New (old > 29 days), Non-Urgent vs Urgent, Easily Apply vs No Easily Apply, Job Title, Company, and Location. 

2) Data Cleaning - dropped duplicate rows to get unique, non-repeating jobs for each role; one-hot encoded categorical data with binary boolean values; filled in missing data with median data value for ExtractedSalary. 

3) Predictive Analysis - performed predictive analysis for Data Scientist role on features using following regression methods in scikit-learn: Linear, Lasso, Ridge, and Elastic Net. 

# Data
The Data Scientist role dataset contains 1025 unique jobs with 9 features including the target variable (salary). Data Analyst dataset contains 1053 unique jobs. Data Engineer contains 664 unique jobs. Machine Learning Engineer contains 1002 unique jobs. It was found 70% of Data Scientist job dataset contains job posts that are 30 days or older. The overall dataset of the project contains 3,744 unique data jobs. Only Data Scientist dataset was used for predictive modeling. 

# Algorithms
1) Linear Regression - Since there was no correlational relationship between any of the features, R_squared was not used as a model fitting metric. Therefore, Median Absolute Error (MAE) was used as a metric to compare between training and test models. Training MAE: 10.6. Testing MAE: 14.5
3) Lasso Regression - Training MAE: 10.9. Testing MAE: 12.0
4) Ridge Regression - Training MAE: 10.8. Testing MAE: 14.3
5) Elastic Net Regression - Training MAE: 10.8. Testing MAE: 12.0

Therefore, it was found both Lasso and Elastic Net Regression models yielded the least error. Lasso Path (LARS) path was constructed from Lasso Regression to explore correspondence between feature coefficients and double-bar graph. It was found there was correspondence. For Data Scientist jobs, urgent jobs pay less than non-urgent jobs. Therefore, it makes sense for the coefficient of Urgent (green line in LARS graph) to be a negative coefficient. All the other features had a positive effect on the salary of Data Scientist with their coefficients being positive. See illustration in Communication section. 

# Tools
1) BeautifulSoup for web scraping
2) Numpy and Pandas for data manipulation
3) Scikit-learn for modeling
4) Matplotlib and Seaborn for plotting

# Communication
<img width="563" alt="DS_sal_LARS" src="https://user-images.githubusercontent.com/67651332/151572462-70429e1e-cf9d-4f7c-97c5-8fb9011fa7df.PNG">
LARS GRAPH FOR DATA SCIENTIST SALARIES

![DA_sal](https://user-images.githubusercontent.com/67651332/151572815-cf865f8c-5233-486a-8fb8-e29f401676cd.png)
![DE_sal](https://user-images.githubusercontent.com/67651332/151572817-23c9c483-3202-47d1-a705-690a89615c6f.png)
![ML_sal](https://user-images.githubusercontent.com/67651332/151572820-445d8762-0d36-45cf-bd18-5ba963d3a73a.png)

