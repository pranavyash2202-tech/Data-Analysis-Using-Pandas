# 📊 Data Analysis using Pandas

## 📌 Internship Task 2 – Alfido Tech

This project was developed as part of the **Python Developer Internship at Alfido Tech**.  
The objective of this task is to demonstrate data analysis skills using the Pandas library.

---

## 🎯 Objectives
- Load and inspect a CSV dataset  
- Handle missing or incorrect data  
- Apply filtering, grouping, and aggregation  
- Extract meaningful insights  

---

## 📁 Dataset
The dataset (`data.csv`) contains the following columns:
- Name  
- Age  
- City  

Some values are missing and handled during data cleaning.

---

## 🛠️ Technologies Used
- Python  
- Pandas  

---

## 💻 Code Implementation

```python
import pandas as pd

# Load dataset
df = pd.read_csv("data.csv")

# Display original data
print(df)

# Handle missing values
df["Age"].fillna(df["Age"].mean(), inplace=True)
df["City"].fillna("Unknown", inplace=True)

# Filter data
filtered = df[df["Age"] > 22]

# Group data
grouped = df.groupby("City")["Age"].mean()

print(filtered)
print(grouped)

