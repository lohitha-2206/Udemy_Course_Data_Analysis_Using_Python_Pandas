# 🎓 Udemy Courses Data Analysis using Python Pandas

## 📌 Project Introduction

This project is based on performing data analysis operations on the Udemy Courses Dataset using Python and the Pandas library inside Jupyter Notebook. The dataset contains information related to course subjects, prices, subscribers, course levels, published dates, and different course categories available on the Udemy platform.

The main objective of this project is to understand how Python and Pandas are used in real-world online course data analysis for filtering, sorting, grouping, and analyzing structured datasets efficiently.

In this project, different data analysis techniques were implemented such as:

- Data Cleaning
- Filtering Records
- Sorting Data
- String Operations
- Date-Time Analysis
- Course Analysis
- Subscriber Analysis
- GroupBy Operations
- Exploratory Data Analysis (EDA)

This project provides practical exposure to working with online learning platform datasets and understanding how data analysts use Python for extracting meaningful insights from educational data.

---

# 📂 Dataset Information

The dataset contains records of courses available on the Udemy learning platform.

### Dataset Features:

- Course Title
- Subject
- Price
- Number of Subscribers
- Course Level
- Published Date
- Course Type (Free/Paid)

Each record in the dataset represents a specific Udemy course.

---

# 🛠️ Tools & Technologies Used

## 🐍 Python
Python was used as the programming language for performing data analysis and dataframe operations.

## 📊 Pandas
Pandas library was used for:
- Data Cleaning
- Data Manipulation
- Filtering Data
- Sorting Data
- Date-Time Analysis
- GroupBy Operations
- Subscriber Analysis

## 📓 Jupyter Notebook
Jupyter Notebook was used to execute Python code interactively and visualize outputs step-by-step.

---

# 🔍 Pandas Functions Implemented

## 🔹 import pandas as pd
Used to import the Pandas library.

### Syntax:
```python
import pandas as pd
```

---

## 🔹 pd.read_csv()
Used to import the CSV dataset into Jupyter Notebook.

### Syntax:
```python
data = pd.read_csv("Udemy_Courses.csv")
```

---

## 🔹 head()
Displays the first 5 rows of the dataset.

### Syntax:
```python
data.head()
```

---

## 🔹 unique()
Displays all unique values from a column.

### Syntax:
```python
data['subject'].unique()
```

---

## 🔹 value_counts()
Displays unique values along with their occurrence count.

### Syntax:
```python
data['subject'].value_counts()
```

---

## 🔹 Filtering Records
Used to access records based on specific conditions.

### Syntax:
```python
data[data['is_paid'] == True]
```

---

## 🔹 sort_values()
Sorts the dataframe according to column values.

### Syntax:
```python
data.sort_values('num_subscribers', ascending=False)
```

---

## 🔹 str.contains()
Used to find records containing a specific string.

### Syntax:
```python
data[data['course_title'].str.contains('Python')]
```

---

## 🔹 dtypes
Displays the datatype of each column.

### Syntax:
```python
data.dtypes
```

---

## 🔹 pd.to_datetime()
Converts the published date column into datetime format.

### Syntax:
```python
data['published_timestamp'] = pd.to_datetime(data['published_timestamp'])
```

---

## 🔹 dt.year
Extracts year values from the datetime column.

### Syntax:
```python
data['Year'] = data['published_timestamp'].dt.year
```

---

## 🔹 groupby()
Groups data according to a specific column.

### Syntax:
```python
data.groupby('level')['num_subscribers'].max()
```

---

# 📊 Tasks Performed in the Project

## ✅ Q1) Subject-wise Course Analysis

### Task:
Find all different subjects for which Udemy is offering courses.

### Code Used:
```python
data['subject'].unique()
```

### Explanation:
- Displays all unique course subjects
- Helps identify available course categories

---

# 📊 Q2) Maximum Number of Courses

### Task:
Find which subject has the maximum number of courses.

### Code Used:
```python
data['subject'].value_counts()
```

### Explanation:
- Counts courses in each subject category
- Helps identify the most popular subject

---

# 📊 Q3) Free Courses Analysis

### Task:
Show all the courses which are free of cost.

### Code Used:
```python
data[data['is_paid'] == False]
```

### Explanation:
- Filters free courses from the dataset
- Useful for identifying free learning resources

---

# 📊 Q4) Paid Courses Analysis

### Task:
Show all the courses which are paid.

### Code Used:
```python
data[data['is_paid'] == True]
```

### Explanation:
- Filters paid courses from the dataset
- Helps analyze premium courses

---

# 📊 Q5) Top Selling Courses

### Task:
Find the top selling courses.

### Code Used:
```python
data.sort_values('num_subscribers', ascending=False)
```

### Explanation:
- Sorts courses based on subscribers count
- Displays most popular courses

---

# 📊 Q6) Least Selling Courses

### Task:
Find the least selling courses.

### Code Used:
```python
data.sort_values('num_subscribers')
```

### Explanation:
- Sorts courses in ascending order
- Displays least popular courses

---

# 📊 Q7) Graphic Design Courses Analysis

### Task:
Show all Graphic Design courses where the price is below 100.

### Code Used:
```python
data[(data['subject'] == 'Graphic Design') & (data['price'] < 100)]
```

### Explanation:
- Applies multi-level filtering
- Displays affordable Graphic Design courses

---

# 📊 Q8) Python Courses Analysis

### Task:
List all the courses related to Python.

### Code Used:
```python
data[data['course_title'].str.contains('Python')]
```

### Explanation:
- Searches for Python-related course titles
- Useful for technology-specific analysis

---

# 📊 Q9) Courses Published in 2015

### Task:
Find all the courses published in the year 2015.

### Code Used:
```python
data['Year'] = data['published_timestamp'].dt.year

data[data['Year'] == 2015]
```

### Explanation:
- Extracts year from published date
- Filters records published in 2015

---

# 📊 Q10) Maximum Subscribers by Course Level

### Task:
Find the maximum number of subscribers for each course level.

### Code Used:
```python
data.groupby('level')['num_subscribers'].max()
```

### Explanation:
- Groups records by course level
- Displays maximum subscribers for each level

---

# 📌 Important Insights

✔️ Pandas makes online course data analysis simple and efficient.

✔️ Sorting operations help identify top and least popular courses.

✔️ Filtering records allows targeted course analysis.

✔️ String operations help search technology-specific courses.

✔️ Date-Time analysis helps identify publishing trends.

✔️ Real-world educational datasets can be analyzed efficiently using Python.

---

# 📁 Project Structure

```text
├── Udemy_Courses_Data_Analysis.ipynb
├── Udemy_Courses.csv
├── README.md
```

---

# 🎯 Final Conclusion

This project demonstrates how Python and Pandas can be used for real-world online course data analysis tasks. Different operations such as filtering records, sorting data, date-time analysis, grouping data, and extracting meaningful insights were successfully implemented.

Through this project, practical understanding was gained in:

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Data Manipulation using Pandas
- Sorting & Filtering Operations
- GroupBy Operations
- Date-Time Analysis
- Python-based Data Analytics

Overall, this project serves as a strong beginner-friendly foundation for learning Data Analysis and Data Science using Python.
