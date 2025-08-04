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
* **Power BI:** For visualization, dashboard design, and interactive analysis. **The .pbix file can be found in `Reports` folder on this github repository**

### **2.2. Cloning Requirements**

1. Make sure you set up your environment and have all the libraries/languages listed above installed.
2. Download the book reading dataset from Pew Research: https://www.pewresearch.org/dataset/march-2016-libraries/. The dataset is only downloadable after you create an account using your organization/institution email.
3. This dataset has hard-coded columns to understand them; you need to read and reference the questionnaire that comes with the dataset upon download. You can also access this questionnaire in my `Reports` folder in this GitHub repository.
4. Run ``git clone https://github.com/Omoyi/Book-Reading-Analysis-Project.git`` in your terminal/command line
4. After forking or cloning this project, first run the code in the first Jupyter notebook because it is the only one in which I imported panda and loaded the data frame. If you run other notebook segments before running the first one, you might get an error about the data frame not being defined.

### **2.3. Python Report Analysis**

To access the report with extensive analysis and by step-by-step guide on data cleaning, feature engineering, and other findings and insights from my Python codes, please check and download the report named `Book Reading Report` under the Reports folder in this GitHub repository. Still, here is a short summary of what I did: 
- **Feature Selection**: This dataset had too many columns over 100, with some including location coordinates and other variables unrelated to my objectives that I listed above. So I had to study each hard column carefully and then select which would be part of my data frame.
- **Column Renaming**: Like I just mentioned, this dataset has coded columns, so to understand what I was dealing with. I quickly mapped the questionnaire using the `CMD+F/CTRL+F` to quickly search/find the column name and then see the question that was being asked in regards to that. That is how I added meaningful columns to my dataset in the preparation phase. For example, a column device1 referred to whether someone owned an electronic device, with corresponding 'a,b,c' standing for smartphone, laptop, tablet, etc...
- **Handling Coded Values**: Unfortunately, not just the columns but even row values were hard-coded; all rows were numerical, and most of them had recurring numbers: 98 and 99. After checking the questionnaire, I realized those were referring to "unknown" or "refused" inputs from respondents. This helped me then transform them into Null values
  ![Data Cleaning & Preparation](/Visuals/Cleaning.png)

- **Exploratory Data Analysis**: After doing all the cleaning and preparation, I went ahead with manipulating the data and displaying reports to better understand my dataframe. I also did some feature engineering and created a column to achieve my objective of knowing people's reading frequency: "Is_frequent_reader"
- **Classification Model Training**: I decided to train 2 models: **Logistic Regression** and **Random Forest Classifier** to see which one would have the highest accuracy rate, Logistic Regression won with +14% and it is the one I used for my Innovation prediction App below.
  ![Classification Models comparison](/Visuals/ModelTraining.png)


### **2.4. Innovation: Python Prediction App**
On line 172 in the ``readersDataCleaning.ipynb``Jupyter notebook file, I created an ipywidget user interface that predicts and recommends a user's reading habits.

![My recommendation app](/Visuals/Screen%20Shot%202025-08-03%20at%203.30.34%20PM.png)


## 3. Data Analysis & Visualization in Power BI

To display and communicate key problems and insights, I went with three leading questions:

### 3.1. How do age, gender, and education level affect reading frequency? (Especially my generation, Gen Z)

![Age, Gender, and Education on book reading](/Visuals/Screen%20Shot%202025-08-03%20at%209.19.55%20PM.png)
- **Gender**: The dashboard shows a noticeable difference in reading frequency by gender, with a higher percentage of female respondents being frequent readers compared to males.

- **Education**: There is a strong positive relationship between higher education levels and reading frequency, with those holding a postgraduate or professional degree having the highest percentage of frequent readers.

- **Age/Generation**: The average number of books read annually appears to be highest among Baby Boomers (60 - 79 years) and Gen X (45 - 60 years) respondents, while younger generations like **Gen Z** show a lower average.


### 3.2. Which types of devices (e-book readers, tablets, smartphones, laptops) are most strongly correlated with being a frequent reader?

![Types of device correlation on book reading](/Visuals/Screen%20Shot%202025-08-03%20at%2010.16.14%20PM.png)

- **Device Ownership**: The visuals show a strong correlation between dedicated reading devices and reading frequency. Owning an eBook Reader has the highest positive correlation with being a frequent reader. While smartphones are widely owned, they have the lowest correlation, suggesting that they are not the primary device for frequent reading.

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

