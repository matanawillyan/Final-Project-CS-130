# Ideas for Final Project

## AI Impact on Jobs 2030
This dataset simulates the future of work in the age of artificial intelligence.
It models how various professions, skills, and education levels might be impacted by AI-driven automation by the year 2030.

https://www.kaggle.com/datasets/khushikyad001/ai-impact-on-jobs-2030?resource=download

Questions I should use:

- How many jobs predicted has a highly chance to get automated by AI?
- What are the jobs that has the highly chance to get automated by AI, and what they have in common?
- What are the jobs that the technology are most improving?
- What the average salary and years of experience relates to a job being automated?

The code I will use for these questions and to build the notebook:

First of all import Pandas and Matplotlib libraries to help with data frames, series, plots and visualization:

> "import pandas as pd"
>
> "import matplotlib.pyplot as plt"

Load the dataset:

> "df = pd.read_csv("AI_Impact_on_Jobs_2030.csv")
>
> (_defining "df" as the csv file_)

> "df.head" 
> (_used to show the first 5 rows of the file_)

To get more info about the csv file:

> "df.shape" (_used to see the number of rows and columns_)
>
> "df.info()" (_for data types and missing values_)  
> 
> "df.describe(include="all")" (_summary statistics_)

Finally, about how I would answer those questions:

### How many jobs predicted has a highly chance to get automated by AI?

> "high_risk = df[df["Automation_probability_2030"] > 0.7]"
>
> "count_high_risk = len(high_risk)"
>
> "percentage_high_risk = (count_high_risk / len(df)) * 100"
>
> "count_high_risk, percentage_high_risk"

### Which jobs have the highest automation probability, and what do they have in common?

#### Top 5 most automatable jobs:

> "top_five_jobs = df.sort_values("Automation_Probability_2030", ascending=False).head(5)

- This gives the 5 jobs most likely to be automated by 2030.
It is the basis for analyzing what “high-risk jobs” have in common.

#### Common education level of the top 5 jobs:

> "top_five_jobs["Education_Level"].value_counts()"

- It can show patterns like:
Most high-risk jobs require only a high school diploma.

### Which jobs have the highest technology growth factor?

> "top_tech_growth = df.sort_values("Tech_Growth_Factor", ascending=False.head(5))"
>
> "top_tech_growth"

- Finds the five jobs most affected by fast technological progress.

### How do salary and experience relate to automation probability?

#### Correlation Salary vs Experience:

> "df[["Average_Salary", "Years_Experience", "Automation_Probability_2030"]].corr()"

Interpretation:  

A number close to 1.0 → strong positive relationship  
A number close to –1.0 → strong negative relationship.  
A number near 0 → no relationship

- If Salary has a negative correlation with automation probability, it means:
Higher-paying jobs are less likely to be automated.

#### Scatterplot: Salary vs Automation

> "plt.scatter(df["Average_Salary"], df["Automation_Probability_2030"])
plt.xlabel("Average Salary")
plt.ylabel("Automation Probability (2030)")
plt.title("Salary vs Automation Risk")
plt.show()"

You can visually see if:  
- High-salary jobs tend to stay safe  
- Low-salary jobs have higher risk

#### Scatterplot: Experience vs Automation
> "plt.scatter(df["Years_Experience"], df["Automation_Probability_2030"])
plt.xlabel("Years of Experience")
plt.ylabel("Automation Probability (2030)")
plt.title("Experience vs Automation Risk")
plt.show()"

Same idea as the salary plot, but now you check:  
- Does having more years of experience protect a job from automation?  
- Are jobs that don't require years of experience more likely to be automated?