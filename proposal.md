# NYC Data Scientist Salary Prediction Based Job Posts For Year 2022
Mai Tran

# What is the framing question of your analysis, or the purpose of the model/system you plan to build?
- To perform accurate salary analysis and prediction for Data Scientist job posts in NYC for the year 2022. 

# Who benefits from exploring this question or building this model/system?
- Job seekers such as recent graduates, career changers, part-time or gig workers
- HR Specialists
- Recruiters
- Economists
- Investors
- Corporate staff

# What dataset(s) do you plan to use, and how will you obtain the data?
- Data Scientist job posts on Indeed job site for year 2022
- H1B Salary Database for year 2022 (for ground truth comparison)

# What is an individual sample/unit of analysis in this project? What characteristics/features do you expect to work with?
- An individual sample is a Data Scientist job post with the following features:
  1. salary (numeric)
  2. company employee rating (numeric)
  3. years of experience (numeric)
  4. post age (numeric)
  5. today's date
  6. job title
  7. location
  8. education
  9. required skills: (Julia + C++) vs (Python + SQL)
  10. company name

# If modeling, what will you predict as your target?
- High-paying Data Scientist jobs require more years of experience and are from high-revenue companies

# How do you intend to meet the tools requirement of the project?
- BeautifulSoup: data scraping
- Pandas: data manipulation
- Numpy and Scikit: data calculation and analysis
- Seaborn: data visualization

# Are you planning in advance to need or use additional tools beyond those required?
- Might use MongoDB or Amazon RDS for data storage

# What would a minimum viable product (MVP) look like for this project?
- I would have scraped all the necessary data and put them in a Pandas data frame with at least one visualization
