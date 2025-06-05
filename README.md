# DAY2
# 🧠 Titanic EDA – AI & ML Internship Task 2

This repository contains my solution to **Task 2: Exploratory Data Analysis (EDA)** as part of the AI & ML Internship. The dataset used is the Titanic Dataset, and the goal is to understand patterns, visualize data, and derive insights before modeling.

---

## 📁 Dataset Used

- **Name:** Titanic Dataset  
- **Source:** [`titanic.csv`](https://www.kaggle.com/datasets/yasserh/titanic-dataset)  
- **Attributes:** PassengerId, Survived, Pclass, Name, Sex, Age, SibSp, Parch, Ticket, Fare, Cabin, Embarked

---

## 🧪 Notebook Content (Summary)

- Load and explore the data using **Pandas**
- Visualize distributions using **Seaborn and Matplotlib**
- Handle missing values
- Plot:
  - Histograms
  - Boxplots
  - Correlation heatmap
  - Pairplot
  - Countplots
- Check for skewness
- Extract patterns and observations

---

## 📘 Interview Questions & Answers

### 1. **What is the purpose of EDA?**  
To understand the structure, trends, and anomalies in the data using stats and visuals before modeling.

### 2. **How do boxplots help in understanding a dataset?**  
They show the median, quartiles, and outliers of numeric data, helping spot skewness or irregular spread.

### 3. **What is correlation and why is it useful?**  
Correlation measures the strength of linear relationships. It's useful for feature selection and identifying multicollinearity.

### 4. **How do you detect skewness in data?**  
By checking `.skew()` values or inspecting histograms. A long tail indicates skew.

### 5. **What is multicollinearity?**  
When two or more features are highly correlated, it can confuse linear models and affect accuracy and interpretability.

### 6. **What tools do you use for EDA?**  
Pandas, Matplotlib, Seaborn, and sometimes Plotly or Sweetviz.

### 7. **Can you explain a time when EDA helped you find a problem?**  
In this Titanic dataset, EDA showed many missing `Cabin` values, prompting us to drop it. We also filled `Age` and `Embarked` with sensible defaults.

### 8. **What is the role of visualization in ML?**  
To make patterns and trends visible and understandable, aiding in decisions like feature engineering or cleaning.

---

## ❓ My Questions and Learnings

### 🔹 What does Seaborn do?  
Seaborn simplifies statistical plots (e.g., boxplots, pairplots) and beautifies them with built-in themes.

### 🔹 What is `Parch`?  
It stands for **Parents/Children** on board. A family relationship count feature.

### 🔹 Why use `include='all'` in `describe()`?  
To include **categorical features** (not just numeric) in the summary statistics.

### 🔹 What is a heatmap used for?  
It **visually encodes numbers** (like correlation or missing values) using colors to spot patterns more quickly.

### 🔹 Why fill `Embarked` with mode?  
Because it’s a **categorical column**, and the mode (most frequent) is the least disruptive imputation.

### 🔹 What is a histogram for?  
To show the **frequency distribution** of numeric data by grouping into **bins**.

### 🔹 What are bins?  
Bins are intervals that group numeric values in histograms (e.g., Age 0–10, 11–20, etc.)

### 🔹 Why only boxplot for Age and Fare?  
Because they are **continuous features** with large integer ranges and clear outliers. `SibSp` and `Parch` are discrete counts and less prone to harmful outliers.

### 🔹 Why heatmap if we have correlation matrix?  
Matrix gives values, heatmap gives **visual cues**. Together, they make it easy to spot multicollinearity.

### 🔹 What is a pairplot?  
A grid of scatterplots for each pair of numerical features to show relationships and separability.

### 🔹 Why is `Sex` not in pairplot?  
Because it's **categorical**. Pairplots only use numerical variables for scatter comparisons.

### 🔹 What is skewness check?  
It tells how much a distribution **leans** left or right. Important for transformations (e.g., log, square root).

### 🔹 How does correlation help avoid multicollinearity?  
By **measuring linear association**; features with high correlation can be dropped to avoid duplicate signal.

### 🔹 Why does multicollinearity matter?  
It **confuses models**, especially linear ones, by making it hard to assign importance to the right variable.

---

## 📝 Final Observations

- Survival highly influenced by **Sex** and **Pclass**
- **Fare** and **Age** have high variance and outliers
- `Cabin` was mostly missing — dropped
- `Embarked` was filled with most common port: **Southampton**
- **SibSp** and **Parch** show family size might affect survival

---

## 📌 Tools Used

- Python
- Pandas
- Seaborn
- Matplotlib
- Jupyter / Kaggle Notebook

---
