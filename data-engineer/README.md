# Data Modeling Challenge — Data Analytics Engineer

## Introduction

Welcome to the **Toys Inc.** data modeling and quality assurance case study. This exercise is designed to assess your proficiency in data modeling using Python, as well as your ability to identify, assess, and correct data quality issues.

---

## Task Overview

### Company Background

Toys Inc. is a renowned global toy company that sells toys online. They've recently collated sales data from different regions, but suspect there may be data inconsistencies and inaccuracies in their dataset. They're looking for insights into sales performance, customer preferences, and growth opportunities.

### Datasets Provided

| File | Description |
| --- | --- |
| `sales_data.json` | Transactional sales data |
| `products.csv` | Product details including name, category, price and supplier |
| `customers.json` | Customer information, such as names and sign-up dates |

---

## Your Tasks

### 1. Data Integrity Check

- Load and inspect the datasets.
- Identify and document data quality issues found in each dataset.

### 2. Data Cleaning

- Design and implement data cleaning steps to address the issues identified.

### 3. Data Modeling

- Create a unified data model in Python that links these datasets.
- Write a Python function that computes the total sales for each product category over the **latest 6 months** in the dataset.

### 4. Business Analysis

Using the cleaned and modeled data, provide answers to the following business questions:

1. Which product category has the highest sales volume in the **North** region over the past 3 months?
2. Identify the **top 5 customers** by sales value since their signup date.
3. Are there any products that have **never been sold**? If yes, list them.
4. Calculate the **average sales price** of the `Action Figure` category products.

### 5. Documentation

- Include a `README.md` or detailed instructions detailing how to set up, run your solution, and how to validate the results.

---

## Submission Guidelines

1. Your Python scripts (data cleaning, data modeling, and analysis).
2. `requirements.txt` (if using a virtual environment).
3. `README.md` including:
   - Step-by-step setup and running instructions.
   - Detailed explanation of data quality issues found and the methods used to address them.
   - Your data modeling approach and any assumptions made.
   - Results from your analysis task.

---

## Evaluation Criteria

| # | Criterion | What we look for |
| --- | --- | --- |
| 1 | Data Integrity and Cleaning | Ability to identify and correct data quality issues |
| 2 | Data Model Design | Coherence, logic, and optimization of the data model |
| 3 | Code Quality | Cleanliness, modularity, maintainability |
| 4 | Analysis Accuracy | The precision of your 6-month sales computation |
| 5 | Documentation | Clarity, thoroughness, and organization of your written explanations and instructions |

---

## Rules

- We understand your time is precious and would not want you to spend more than **3 to 4 hours** on this, over the span of **one week max**.
- The outcome should be runnable locally on a UNIX-flavored OS (macOS, Linux).
