# Book Reading Data Analysis Project

## 1. Project Overview

A python data analysis project using a dataset from pewresearch.org on book reading behaviors from March 7 - April 4, 2016 after interviewing people between the ages of 16 - 95 in the US. 

**My main objectives in this analysis are**: 

- To determine and compare the average number of books read annually across different age groups and analyze this data to identify any a decline in reading frequency over time. 

- To identify how generational preferences for different book formats, such as print, e-books, and audiobooks, may correlate with changes in reading frequency. 

- To present these findings through clear and compelling visualizations to provide actionable insights into generational reading trends. 

## 2. Instructions

### **2.1. Tools Used**

* **Python (Jupyter Notebook, Matplotlib, Panda, and Seaborn libraries):** For initial data loading and preparation.
* **Power BI:** For visualization, dashboard design, and interactive analysis.

### **2.2. Cloning Requirements**

1. Make sure you set up your environment and have all the libraries/languages listed above installed.
2. Download the book reading dataset from Pew research: https://www.pewresearch.org/dataset/march-2016-libraries/
3. The dataset is only downloadable after you create an account using your organization/institution email.
4. Run ``git clone https://github.com/Omoyi/Book-Reading-Analysis-Project.git`` in your terminal/command line
4. After forking or cloning this project first run the code in the first jupyter notebook because it is the only one in which I imported panda and loaded the data frame. If you run other notebook segments before running the first one you might get an error about the dataFrame not being defined.

### **2.3. Python Report Analysis**

To access the report with extensive analysis and step by step guide on findings and insights from my python codes check and download the report named `Book Reading Report` under Reports folder in this github repositories

### **2.4. Innovation: Python Prediction App**
On line 172 in the ``readersDataCleaning.ipynb`` jypyter notebook file, I created an ipywidget user interface that predicts and recommends a user's reading habits.

![My recommendation app](/Visuals/Screen%20Shot%202025-08-03%20at%203.30.34%20PM.png)


## 3. Data Analysis & Visualization in PowerBI

To display and communicate key problems and insights, I went with three leading questions:

### 3.1. How does age, gender, and education level affect reading frequency? (Especially my generation Gen x)

![Age, Gender, and Education on book reading](/Visuals/Screen%20Shot%202025-08-03%20at%209.19.55%20PM.png)
- **Gender**: The dashboard shows a noticeable difference in reading frequency by gender, with a higher percentage of female respondents being frequent readers compared to males.

- **Education**: There is a strong positive relationship between higher education levels and reading frequency, with those holding a postgraduate or professional degree having the highest percentage of frequent readers.

- **Age/Generation**: The average number of books read annually appears to be highest among Baby Boomer (less than ) and Gen X respondents, while younger generations like Gen Z show a lower average.


### 3.2. Which types of devices (e-book readers, tablets, smartphones, laptops) are most strongly correlated with being a frequent reader?

![Types of device correlation on book reading](/Visuals/Screen%20Shot%202025-08-03%20at%2010.16.14%20PM.png)

- **Device Ownership**: The visuals show a strong correlation between dedicated reading devices and reading frequency. Owning a device has the highest positive correlation with being a frequent reader. Smartphones are widely owned, and they appear to have the highest correlation especially for female respondents, suggesting that they might be one of the primary devices for frequent reading for females.

- **Demographic Insights (in the Table Visual)**: The table confirms that female respondents, on average, are slightly older and have a significantly higher sum of books read over the year compared to male respondents.

### 3.3. What are the most common reading habits (e.g., reading print books vs. e-books) among different demographic groups?

![Reading habits per Education Levels](/Visuals/Screen%20Shot%202025-08-03%20at%2010.33.57%20PM.png)

**Book Formats**: Across all education levels, print books remain the most popular format. However, the use of other formats like audiobooks and ebooks appears to increase with higher levels of education.

## 4. Biases in my Data

### 4.1. Selection Bias
This data is based on a survey of individuals who chose to respond. This means the sample may not be a true representation of the general population. For example, it might over-represent individuals who are more engaged with reading or the specific platform where the survey was hosted.

### 4.2. Response Bias
The data, particularly the number of books read and whether someone is a frequent reader, is self-reported. People may not recall the exact number of books they read or might be inclined to overstate their reading habits, which could introduce inaccuracies.

### 4.3. Data Cleaning Assumptions
My decisions during the data cleaning process could have introduced assumptions. For example, I filled missing age values with the median and missing books_read_in_1_year values with 0. While these were logical assumptions, they are still a form of manupulation that can subtly influence the results.

### 4.4. Interpretation Bias 
The visuals themselves can lead to certain interpretations. For example, while my charts show a correlation between factors this does not imply causation. Other factors that I don't know may be at play.

## 5. Key Findings

* A higher percentage of female respondents are frequent readers compared to males.
* Reading frequency shows a strong positive correlation with higher education levels, with postgraduate degree holders having the highest percentage of frequent readers. The average number of books read is highest among Baby Boomers and Gen X, and it decreases with younger generations.
* The strongest correlation with being a frequent reader is the ownership of a dedicated eBook reader. Smartphone ownership shows the lowest correlation with frequent reading in general.
* While print books remain the most popular format across all education levels, the usage of digital formats like audiobooks and ebooks is more prevalent among those with a higher education.

## 6. Conclusion & Recommendations

- Given the strong correlation between eBook reader ownership and reading frequency, prioritize digital marketing efforts toward e-reader platforms to capture the most engaged reading audience might yield more profitable.

- To appeal to a wider audience, especially those with higher education, develop a content strategy that includes a strong mix of print, audio, and ebook formats.

## 7. Dashboard Interactivity

``Slicers``: The dashboard features interactive slicers for Gender, Education, and Generation. You can select one or more categories in any of these slicers to filter all the visuals on the page and see how the data changes for a specific demographic.

``Cross-Filtering``: All visuals on the dashboard are interconnected. Clicking on a specific bar or data point in one chart (e.g., clicking on "Female" in the gender chart) will automatically filter the rest of the visuals, allowing you to perform a detailed cross-analysis.

``Drill-Down Capability``: The "Generation" column allows for a high-level overview of age groups, but you can also use the original age column to see a more granular breakdown if needed.

