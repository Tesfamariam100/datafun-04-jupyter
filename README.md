# Project 4: Jupyter Notebook for Exploratory Data Analysis (EDA)

## Overview
Name: Tesfamariam
Date: 2024-02-02

Project Objectives:
The primary goal of Project 4 is to gain proficiency in the following areas:
- Setting up a Jupyter Notebook environment
- Conducting exploratory data analysis (EDA)
- Visualizing data using matplotlib and seaborn
- Documenting insights and observations
- 
## Deliverables

- GitHub Repository: datafun-04-jupyter
- Documentation: README.md
- Notebook: yourname_eda.ipynb
  
## Getting started

Complete the following steps before starting the project
- Create a New GitHub Repository: I create a new GitHub repository called datafun-04-jupyter.
- Set up Your Local Environment: I clone the repository to my local machine and set up a virtual environment.
- Install Dependencies: I install the required Python packages like pandas, matplotlib, and seaborn.
- Start Jupyter Notebook: I launch Jupyter Notebook and create a new notebook file named yourname_eda.ipynb.

## Load the Iris dataset into DataFrame
df = sns.load_dataset('iris')

## Inspect first rows of the DataFrame
print(df.head())
Initial Data Inspection: Display the first 10 rows, shape, and data types of each column.

python
Copy code
print(df.head(10))
print(df.shape)
print(df.dtypes)
Initial Descriptive Statistics: Use the DataFrame describe() method to display summary statistics.

python
Copy code
print(df.describe())
Initial Data Distribution for Numerical Columns: Plot histograms for numerical columns.

python
Copy code
df['sepal_length'].hist()
df.hist()
plt.show()
Initial Data Distribution for Categorical Columns: Display value counts for categorical columns.

python
Copy code
for col in df.select_dtypes(include=['object', 'category']).columns:
    sns.countplot(x=col, data=df)
    plt.title(f'Distribution of {col}')
    plt.show()
Initial Data Transformation and Feature Engineering: Perform necessary transformations on the data.

python
Copy code
### Example: Renaming a column
df.rename(columns={'sepal_length': 'Sepal Length'}, inplace=True)

### Example: Adding a new column
df['Sepal Area'] = df['Sepal Length'] * df['sepal_width']
Initial Visualizations: Create various chart types using seaborn and matplotlib.

python
Copy code
sns.pairplot(df, hue='species')
plt.show()