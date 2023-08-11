## **Data Modeling Challenge (Data Engineer)**

### **Introduction**

Welcome to the Toys Inc. data modeling and quality assurance case study. This exercise is designed to assess your proficiency in data modeling using Python, as well as your ability to identify, assess, and correct data quality issues. Familiarity with **`dbt`** (Data Build Tool) will be beneficial but is optional.

### **Task Overview**

**Company Background:**

*Toys Inc.* is a renowned global toy company that sells toys online. They've recently collated sales data from different regions, but suspect there may be data inconsistencies and inaccuracies in their dataset. They're looking for insights into sales performance, customer preferences, and growth opportunities.

**Datasets Provided:**

1. **`sales_data.json`** - Contains transactional sales data.
2. **`products.csv`** - Product details including name, category, and recommended age group.
3. **`customers.json`** - Customer information, such as names and sign-up dates.

**Your Tasks:**

1. **Data Integrity Check**:
    - Load and inspect the datasets.
    - Identify and document data quality issues found in each dataset.
2. **Data Cleaning**:
    - Design and implement data cleaning steps to address the issues identified.
3. **Data Modeling**:
    - Create a unified data model in Python that links these datasets.
    - Write a Python function that computes the total sales for each product category over the past 6 months.
4. **dbt (Optional)**:
    - Set up a dbt project.
    - Design dbt models to transform the raw datasets into a star schema.
    - Generate a dbt model for the analysis task mentioned above.
    - Validate data integrity using dbt tests.
5. **Business Analysis**:
    
    Using the cleaned and modeled data, provide answers to the following business questions:
    
    - Which product category has the highest sales volume in the North region over the past 3 months?
    - Identify the top 5 customers by sales value since their signup date.
    - Are there any products that have never been sold? If yes, list them.
    - Calculate the average sales price of the 'Action Figure' category products.
    - How many sales transactions were processed for customers who signed up in the last year?
6. **Environment Containerization**:
    - Ensure your code and its dependencies are either packaged within a Docker container or in a Python virtual environment.
    - Include a **`README.md`** or detailed instructions detailing how to set up, run your solution, and how to validate the results.

### **Submission Guidelines**

1. Your Python scripts (data cleaning, data modeling, and analysis).
2. Any dbt projects, models, and tests (if you utilized dbt).
3. **`Dockerfile`** and **`docker-compose.yml`** (if using Docker) **or** **`requirements.txt`** (if using a virtual environment).
4. **`README.md`** including:
    - Step-by-step setup and running instructions.
    - Detailed explanation of data quality issues found and the methods used to address them.
    - Your data modeling approach and any assumptions made.
    - Results from your analysis task.
    - Explanation of your dbt design (if applicable).

### **Evaluation Criteria**

1. **Data Integrity and Cleaning**: Ability to identify and correct data quality issues.
2. **Data Model Design**: Coherence, logic, and optimization of the data model.
3. **Code Quality**: Cleanliness, modularity, maintainability.
4. **Analysis Accuracy**: The precision of your 6-month sales computation.
5. **dbt Utilization (if applicable)**: Adherence to best practices, model structure, and testing capability.
6. **Environment Setup**: How easy it is to set up and run your solution. Consideration of containerization or a virtual environment.
7. **Documentation**: Clarity, thoroughness, and organization of your written explanations and instructions.

### **Rules**
We understand your time is precious and would not want you to spend more than **3 to 6 hours** on 
this over the span of **one week** max. The outcome should be runnable locally on a UNIX-flavored 
OS (MacOS, Linux).