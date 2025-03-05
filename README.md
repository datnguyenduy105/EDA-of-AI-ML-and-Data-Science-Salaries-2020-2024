# Exploratory Data Analysis of AI, ML, and Data Science Salaries (2020-2024)

## Table of Contents

1.  [Project Overview](#project-overview)
2.  [Dataset](#dataset)
3.  [Methodology](#methodology)
    *   [3.1 Data Acquisition and Loading](#data-acquisition-and-loading)
    *   [3.2 Data Cleaning and Preprocessing](#data-cleaning-and-preprocessing)
    *   [3.3 Data Transformation and Feature Engineering](#data-transformation-and-feature-engineering)
    *   [3.4 Exploratory Data Analysis (EDA) and Visualization](#exploratory-data-analysis-eda-and-visualization)
4.  [Insights](#insights)
5.  [Recommendations](#recommendations)
6.  [Tools Used](#tools-used)
7.  [Conclusion](#conclusion)

## 1. Project Overview

This project performs an exploratory data analysis (EDA) on a dataset of AI, ML, and Data Science salaries from 2020 to 2024. The primary goal is to identify salary trends and patterns based on factors such as experience level, job title, employment type, remote work arrangement, company location, and company size. The analysis aims to provide valuable insights into the salary landscape within the AI, ML, and Data Science domains. Importantly, a significant number of duplicate entries (over 50%) were intentionally retained, recognizing them as representations of multiple survey submissions rather than data errors.

## 2. Dataset

The dataset is sourced from [ai-jobs.net](https://ai-jobs.net/) and is titled "The Global AI, ML, Data Science Salary Index for 2024". It contains salary information crowdsourced from professionals and employers worldwide. 

## 3. Methodology

This EDA project uses a structured approach encompassing data cleaning, transformation, and exploratory analysis.

### 3.1 Data Acquisition and Loading

### 3.2 Data Cleaning and Preprocessing

### 3.3 Data Transformation and Feature Engineering

To facilitate a more insightful analysis, several data transformations were performed:

*   **Job Title Categorization:** A custom Python function (`map_job_title()`) was implemented to categorize the highly granular `job_title` column into broader, more manageable categories. This function utilizes a dictionary-based mapping approach, assigning job titles like "Data Scientist," "Data Engineer," and "Data Analyst" to predefined categories based on keyword matching (lowercase). Titles not explicitly listed default to "Data Scientist."  This addresses the high cardinality and variability of job titles.

*   **Remote Work Model Creation:** A custom function (`map_remote_ratio()`) transformed the `remote_ratio` column (numerical values representing the percentage of remote work) into categorical values: 'Onsite', 'Hybrid', and 'Remote'. This simplifies analysis of remote work's effect on salary.

*   **Label Renaming:** Existing categorical columns (`experience_level`, `employment_type`, `company_size`, `company_location`) were re-labeled with more descriptive and consistent naming conventions to improve readability.  For Example: Replacing "EN" for entry-level to "Entry Level".

### 3.4 Exploratory Data Analysis (EDA) and Visualization

The core of the methodology involves EDA using descriptive statistics and data visualization.

*   **Descriptive Statistics:** Measures such as mean, median, standard deviation, percentiles, and counts were calculated for relevant variables.  The `skim()` function from the `skimpy` library was used for quick summary statistics and histograms.
*   **Data Visualization:** Seaborn, Matplotlib, and Plotly were used to generate histograms, box plots, bar charts, scatter plots, and other visualizations to explore the relationships between salary and other variables (experience level, job title, employment type, remote work, company size, location, and employee residence).

## 4. Insights

*   **High Demand for Data Scientists:** Data Scientist positions are the most in-demand, comprising over half of all job postings.
*   **Strong Growth in the Data Science Market:** 2024 sees a surge in hiring demand in Data Science, especially for roles in Machine Learning, AI, and Data Engineering.
*   **The US is the Main Hub:** The majority of job postings and employees in Data Science are located in the United States.
*   **Medium-sized Companies Dominate Hiring:** Medium-sized companies tend to hire more Data Science professionals.
*   **Onsite Work Remains Prevalent:** Despite the growth of remote work, onsite work is still the most common model.
*   **Steady Salary Growth:** Salaries in Data Science tend to increase steadily, particularly in management, Data Science, and Data Engineering roles.
*   **Experience and Position Greatly Influence Salary:** Salaries increase with experience, with management positions typically having the highest salaries.
*   **Salaries Vary by Country:** Salaries for Senior Data Scientists vary greatly between countries.
*   **Roles of Technology and Analytics:** Positions related to technology and data analysis are dominating the job market.
*   **Variety in Work Models:** Although onsite work is still the most common, there is a significant number of remote positions.

## 5. Recommendations

*   **For Job Seekers:** Focus on Data Scientist, Data Engineering, and Machine Learning/AI positions. Develop technical and data analysis skills. Consider opportunities in the US and at medium-sized companies.
*   **For Employers:** Prioritize finding and attracting experienced Data Scientist professionals. Offer competitive salaries and flexible work models. Consider expanding remote recruitment.
*   **For Those Seeking Career Advancement:** Invest in developing specialized skills, particularly in AI/Machine Learning. Consider transitioning into management positions.

## 6. Tools Used

*   Python
*   Pandas
*   Seaborn
*   Matplotlib
*   Plotly
*   Skimpy (for data summarization)
*   NLTK and WordCloud

## 7. Conclusion

This EDA provides a valuable foundation for understanding salary trends in the AI, ML, and Data Science fields. Further analysis, potentially with more refined job title categorization and predictive modeling, could further enhance these insights. The presence of numerous duplicate entries highlights the importance of data collection methods and potential biases.  The complete Jupyter Notebook contains detailed findings and visualizations.


