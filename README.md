# FUTURE_DS_03

# 🎓 **Student Satisfaction Survey Analysis — Internship Project**

## 📌 Project Overview

This project analyzes **student satisfaction survey data** collected from an autonomous college to evaluate **faculty performance and overall learning experience**. Using **Google Colab, pandas, seaborn, and Matplotlib**, the goal is to extract meaningful insights from structured rating data and open-ended questions.

The study explores **syllabus coverage, communication effectiveness, teaching methodology, student support, assessment fairness, and more** by analyzing the feedback provided across different courses.

---

## 🎯 Objectives

This project aims to:

✔ Load and explore student feedback data
✔ Clean and prepare survey fields for analysis
✔ Evaluate descriptive statistics for faculty performance
✔ Analyze distribution of weightages (ratings 1–5)
✔ Compute correlations between rating categories
✔ Categorize feedback questions into meaningful themes
✔ Visualize scoring patterns across different themes and courses
✔ Produce insights for academic improvement

---

## 🗂️ Dataset Description

The dataset contains feedback submitted by students, with columns such as:

* **SN** – Unique identifier
* **Questions** – Survey items evaluating teaching & learning
* **Total Feedback Given** – Number of responses received
* **Total Configured** – Expected number of responses
* **Weightage 1–5** – Rating counts for each question
* **Average / Percentage** – Pre-computed combined score
* **Course Name** – Specific course being evaluated
* **Basic Course** – Broader category of the course

### Additional Columns Created

* **Average** – Extracted numerical value from “Average / Percentage”
* **Theme** – Categorization of questions into common themes

---

## 🧰 Tools & Libraries

| Tool / Library           | Purpose                        |
| ------------------------ | ------------------------------ |
| **Google Colab**         | Notebook environment           |
| **pandas**               | Data wrangling & preprocessing |
| **numpy**                | Numeric operations             |
| **matplotlib / seaborn** | Visualization                  |
| **warnings**             | Suppress irrelevant warnings   |

---

## 🛠 Data Cleaning & Preparation

Key processing steps included:

### ✔ Mount Google Drive

Used to access dataset from Colab.

### ✔ Load dataset using pandas

```python
df = pd.read_csv(file_path, encoding='latin1', index_col='SN')
```

### ✔ Clean and extract numeric average score

The “Average / Percentage” column is split into a numeric value:

```python
df["Average"] = df["Average/ Percentage"].str.split("/").str[0].astype(float)
```

### ✔ Categorize feedback questions into themes

Themes include:

* **Syllabus Coverage & Preparation**
* **Communication & Teaching Methodology**
* **Assessment & Feedback**
* **Growth & Opportunities**
* **Teacher Support & Engagement**
* **Skills & Employability**

A custom mapping assigns each question to its respective theme.

---

## 📊 Analysis Conducted

### ⭐ 1. Descriptive Statistics

Generated summary metrics for average ratings, including mean, standard deviation, min/max values, and percentiles.

### ⭐ 2. Distribution of Average Scores

A histogram and KDE plot reveal how overall scores are distributed across all questions.

### ⭐ 3. Weightage Frequency Analysis

Summed Weightage 1–5 columns and visualized rating frequencies to understand how often each level is selected.

### ⭐ 4. Correlation Analysis

A heatmap was created to identify relationships between different weightage scores.

### ⭐ 5. Thematic Analysis

Each question was assigned to a theme, enabling:

* Comparison of score distributions per theme
* Identification of high- and low-performing teaching domains

### ⭐ 6. Course-Level Insights

Calculated average feedback scores per “Basic Course” and visualized as a bar chart.

---

## 📈 Visualizations Included

The notebook includes several clear and insightful visual outputs:

* **Histogram** of average feedback scores
* **Bar chart** showing frequency of each weightage rating
* **Correlation heatmap** for Weightage 1–5
* **Boxplot** of theme-based score distribution
* **Bar chart** of average scores by Basic Course

These visuals make it easy to interpret overall patterns and identify areas needing attention.

---

## 🔍 Key Insights

Based on the analysis:

* Most feedback scores cluster around **3.5–4.5**, indicating moderate to high satisfaction.
* Weightage 4 and 5 received significantly more counts across questions.
* Themes related to **Communication**, **Teacher Support**, and **Teaching Methodology** show strong performance.
* Some areas such as **Assessment & Feedback** show more variability, suggesting room for improvement.
* Differences between **Basic Courses** highlight varying teaching effectiveness across departments.

---

## 📁 Final Deliverables

Your project submission includes:

✔ Google Colab notebook (`.ipynb`)
✔ Clean, well-commented Python script (auto-generated)
✔ Visualizations of rating distributions, correlations, and theme comparisons
✔ Insights summary for faculty evaluation and academic quality enhancement

---

## 🚀 How to Run This Project

1. Open Google Colab
2. Upload the notebook or Python script
3. Upload the CSV dataset to the Colab environment
4. Run all cells sequentially
5. Interpret the output charts and insights

---

## 💡 Future Enhancements

* Include sentiment analysis on open-ended comments
* Build a scoring model to predict low-performing courses
* Create a Looker Studio or Power BI dashboard
* Add automated reporting using Python

---

## 👨‍💻 Author

**Brian Ouko**  

Data Scientist | Analyst | Researcher   
Passionate about improving education, events, and social systems using data.
Just let me know!

