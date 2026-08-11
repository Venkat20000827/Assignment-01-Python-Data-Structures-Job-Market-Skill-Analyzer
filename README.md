# Assignment-01-Python-Data-Structures-Job-Market-Skill-Analyzer
# 📊 Job Market Skill Analyzer

A beginner-friendly **Data Science portfolio project** built with Python to analyze the skills requested in data and analytics job postings.

This project demonstrates how Python data structures, loops, functions, text processing, filtering, and file handling can be combined to extract useful insights from job-market data.

> **Project Type:** Data Science / Python Data Analysis  
> **Level:** Beginner → Intermediate  
> **Primary Language:** Python  
> **Environment:** Jupyter Notebook / Google Colab

---

## 🎯 Project Overview

The **Job Market Skill Analyzer** is a compact Python program designed to analyze skills mentioned in job postings for data and analytics roles.

The project works with job posting information such as:

- Job ID
- Job Role
- Company
- Skills

The notebook allows users to add new job postings, clean and normalize skill data, calculate skill frequencies, search for jobs by skill, identify common skills, and save structured data to a CSV file.

The project follows the requirements of the **Advanced Data Science Program – Assignment 01: Python Data Structures – Job Market Skill Analyzer**. The assignment specifically asks for job data management, interactive posting addition, skill cleaning, frequency analysis, search functionality, lambda/filter usage, unique-skill extraction, and file handling. 

---

## 💡 Business Problem

Recruitment teams and job seekers often need to understand which technical skills are frequently requested in the job market.

For example:

- Which skills appear most frequently?
- How many jobs require Python?
- Which roles mention SQL?
- What are the unique skills in the dataset?
- Which roles contain at least one commonly requested skill?

This project provides a simple Python-based solution to answer these questions.

---

## 🚀 Key Features

### 1. Job Data Management

The project stores job postings using Python dictionaries and lists.

Each posting contains:

```text
Job_ID
Role
Company
Skills
```

Example:

```text
ID: 1 | Role: Data Analyst | Company: ABC Corp | Skills: Excel SQL Python
```

---

### 2. Interactive Job Posting Addition

Users can enter new job postings interactively.

The program collects:

- Role
- Company
- Skills

The `Job_ID` is automatically generated from the current maximum ID.

Example:

```text
Enter how many job want to add: 2
Enter role: Junior Data Analyst
Enter company: BrightData
Enter skills: Excel, SQL, Python
```

---

### 3. Skill Cleaning & Normalization

A custom function is used to clean skill text.

The cleaning process:

- Converts text to lowercase
- Replaces commas with spaces
- Removes leading/trailing spaces
- Normalizes multiple spaces

Example:

```text
Input:
Excel, SQL, Python

Output:
excel sql python
```

This makes skill comparison and counting more consistent.

---

### 4. Skill Extraction & Frequency Analysis

The cleaned skill strings are split into individual skill tokens.

The project then:

1. Creates a consolidated skill list
2. Counts skill occurrences
3. Sorts skills by frequency
4. Displays the top 5 skills

Example:

```text
Top skills by frequency:
python: 4
sql: 3
ml: 2
excel: 2
statistics: 1
```

The exact result changes if additional job postings are entered.

---

### 5. Basic Job-Market Statistics

The project calculates:

- Total number of job postings
- Number of unique skills
- Jobs mentioning Python

Example:

```text
Total Jobs: 5
Unique skills: 8
Jobs mentioning Python:
['Data Analyst', 'Data Scientist', 'Data Engineer', 'ML Engineer']
```

---

### 6. Skill Search Function

The project contains a reusable function:

```python
find_jobs_by_skill(skill_query)
```

It searches job postings for a particular skill and returns:

```text
(Job_ID, Role, Company)
```

Example:

```python
find_jobs_by_skill("sql")
```

Possible result:

```text
[
    (1, 'Data Analyst', 'ABC Corp'),
    (3, 'Business Analyst', 'DataWorks'),
    (4, 'Data Engineer', 'InfraTech')
]
```

The search query is normalized using lowercase conversion and whitespace stripping.

---

### 7. Lambda & Filter

The project demonstrates functional programming concepts using:

- `lambda`
- `filter()`
- `any()`

It identifies roles containing at least one skill whose frequency is 2 or more.

Example:

```text
Roles with at least one common skill:
['Data Analyst', 'Data Scientist', 'Data Engineer', 'ML Engineer']
```

---

### 8. Unique Skill Set

All extracted skills are converted into a Python `set` to remove duplicates.

The unique skills are then sorted alphabetically.

Example:

```text
['deeplearning',
 'excel',
 'ml',
 'powerbi',
 'python',
 'spark',
 'sql',
 'statistics']
```

---

### 9. File Handling

The project demonstrates Python file handling using the `csv` module and exception handling.

The cleaned job records can be stored in CSV format with:

```text
Job_ID,Role,Company,Skills
```

The current notebook writes the cleaned records to:

```text
job_data.csv
```

---

## 🛠️ Technologies & Concepts Used

### Programming

- Python
- Jupyter Notebook / Google Colab

### Python Concepts

- Variables
- Lists
- Dictionaries
- Sets
- `for` loops
- `if / elif / else`
- Functions
- `lambda`
- `filter()`
- `any()`
- List operations
- String methods
- Exception handling
- CSV file handling

### Data Processing

- Text normalization
- Skill extraction
- Frequency counting
- Filtering
- Sorting
- Unique value extraction

---

## 📁 Project Structure

```text
Job-Market-Skill-Analyzer/
│
├── Assignment_01_Python_Data_Structures_Job_Market_Skill_Analyzer.ipynb
├── job_data.csv
└── README.md
```

### File Description

| File | Description |
|---|---|
| `Assignment_01_Python_Data_Structures_Job_Market_Skill_Analyzer.ipynb` | Main Jupyter Notebook containing the complete analysis |
| `job_data.csv` | CSV output generated by the current notebook |
| `job_skills.csv` | Assignment-specified name for the cleaned job records |
| `top_skills.txt` | Assignment-specified text output for top skills and counts |
| `README.md` | Project documentation |

> **Implementation note:** The assignment specification asks for `job_skills.csv` and `top_skills.txt`. The current notebook implementation writes `job_data.csv` and does not yet create `top_skills.txt`. For a portfolio submission, these filenames should be aligned with the assignment requirements.

---

## ▶️ How to Run the Project

### Option 1: Jupyter Notebook

1. Clone or download this repository.
2. Open Jupyter Notebook.
3. Open:

```text
Assignment_01_Python_Data_Structures_Job_Market_Skill_Analyzer.ipynb
```

4. Run the cells from top to bottom.
5. When prompted, enter new job-posting information.

### Option 2: Google Colab

1. Upload the `.ipynb` file to Google Colab.
2. Open the notebook.
3. Run all cells sequentially.
4. Provide inputs when the interactive cells request them.

---

## 🔄 Project Workflow

```text
Job Posting Data
       ↓
Display Job Records
       ↓
Add New Job Postings
       ↓
Clean & Normalize Skills
       ↓
Extract Individual Skills
       ↓
Count Skill Frequency
       ↓
Generate Job-Market Insights
       ↓
Search Jobs by Skill
       ↓
Find Roles with Common Skills
       ↓
Create Unique Skill Set
       ↓
Save Structured Data
```

---

## 📈 Example Dataset

The initial project dataset contains five roles:

| Job ID | Role | Company | Skills |
|---:|---|---|---|
| 1 | Data Analyst | ABC Corp | Excel SQL Python |
| 2 | Data Scientist | XyZ Ltd | Python ML Statistics |
| 3 | Business Analyst | DataWorks | Excel SQL PowerBI |
| 4 | Data Engineer | InfraTech | Python SQL Spark |
| 5 | ML Engineer | AI Labs | Python ML DeepLearning |

---

## 🎓 Skills Demonstrated

This project is useful as a portfolio piece because it demonstrates practical understanding of core Python and early data-analysis concepts:

- Data structure manipulation
- Data cleaning
- Text processing
- Frequency analysis
- Basic statistics
- Search and filtering
- Functional programming concepts
- File handling
- Exception handling
- Writing reusable functions

These are foundational skills for progressing toward **Data Analyst, Data Scientist, Machine Learning Engineer, and AI/ML roles**.

---

## 🔮 Future Improvements

This project can be extended into a more advanced Data Science project by adding:

- Pandas-based data processing
- Matplotlib / Seaborn visualizations
- Skill frequency bar charts
- Role-wise skill analysis
- Company-wise skill analysis
- Salary analysis
- Job-location analysis
- NLP-based skill extraction
- Skill-demand trends
- Interactive Streamlit dashboard
- Machine-learning-based job recommendation
- Automated resume-to-job skill matching

---

## 🧠 Learning Outcome

Through this project, I practiced how to transform raw job-posting information into structured data and extract meaningful insights using Python.

The project helped strengthen my understanding of:

```text
Python Data Structures
        ↓
Data Cleaning
        ↓
Data Extraction
        ↓
Frequency Analysis
        ↓
Filtering & Searching
        ↓
Basic Data Insights
        ↓
File Handling
```

---

## 👨‍💻 Author

**Venkatesh**

Aspiring Data Scientist | Python | Data Analysis | Machine Learning

---

## ⭐ Portfolio Note

This project is part of my journey toward becoming a **Data Scientist**. It demonstrates my ability to work with structured data, perform basic data cleaning and analysis, and build a Python-based analytical solution from a real-world-style business problem.

More advanced projects will build on these foundations using **Pandas, NumPy, SQL, Statistics, Machine Learning, Data Visualization, and Deep Learning**.
