# Ideas for Final Project

## AI Impact on Jobs 2030
Predicting automation risk across global professions by 2030.

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

- How many jobs predicted has a highly chance to get automated by AI?


