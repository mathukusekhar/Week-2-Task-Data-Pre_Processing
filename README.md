# Agriculture Data Collection and Cleaning Project

## 1. Project Overview

This project focuses on collecting, preparing, cleaning, and preprocessing agricultural data using Python.

The dataset contains information about different agricultural crops, states, seasons, cultivated area, production, and dates.

The main purpose of this project is to prepare raw agricultural data for further analysis and data science applications.

---

## 2. Dataset Columns

The dataset contains the following columns:

| Column       | Description                     |
| ------------ | ------------------------------- |
| `state`      | Name of the state               |
| `crop`       | Name of the agricultural crop   |
| `season`     | Crop growing season             |
| `area`       | Area used for cultivation       |
| `production` | Quantity of crop production     |
| `date`       | Date of the agricultural record |

The program also creates additional columns:

| Column              | Description                |
| ------------------- | -------------------------- |
| `yield`             | Production divided by area |
| `area_scaled`       | Scaled area value          |
| `production_scaled` | Scaled production value    |
| `yield_scaled`      | Scaled yield value         |

---

## 3. Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Visual Studio Code

---

## 4. Python Libraries Required

Install the required libraries using:

```bash
pip install pandas numpy scikit-learn
```

---

## 5. Project Structure

```text
Agriculture_Data_Project/
│
├── agriculture_data.csv
├── agriculture_cleaning.py
├── agriculture_cleaned.csv
└── README.md
```

### File Description

**agriculture_data.csv**

Contains the original/raw agriculture dataset.

**agriculture_cleaning.py**

Python program used to clean and preprocess the dataset.

**agriculture_cleaned.csv**

The cleaned dataset generated automatically by the Python program.

**README.md**

Contains project information and instructions for running the project.

---

## 6. Data Cleaning Process

The Python program performs the following steps:

### Step 1: Load Dataset

The program reads the CSV file using Pandas.

```python
df = pd.read_csv("agriculture_data.csv")
```

### Step 2: Check Dataset

The program displays:

* Number of rows
* Number of columns
* Column names
* First five records

### Step 3: Check Missing Values

Missing values are identified using:

```python
df.isnull().sum()
```

### Step 4: Remove Duplicate Records

Duplicate rows are removed to improve data quality.

```python
df = df.drop_duplicates()
```

### Step 5: Clean Text Data

The `state`, `crop`, and `season` columns are cleaned by:

* Removing extra spaces
* Converting text to a consistent format

### Step 6: Convert Numerical Data

The `area` and `production` columns are converted into numerical values.

Invalid numerical values are converted to missing values and handled appropriately.

### Step 7: Handle Missing Values

Missing numerical values are replaced using the median value.

Missing text values are replaced with:

```text
Unknown
```

### Step 8: Convert Date

The `date` column is converted into a proper date format.

### Step 9: Create Yield

A new agricultural feature called `yield` is created.

```text
Yield = Production / Area
```

This can help compare agricultural productivity.

### Step 10: Feature Scaling

The numerical features are scaled using `StandardScaler`.

The following columns are scaled:

* Area
* Production
* Yield

### Step 11: Generate Summary

The program calculates:

* Total production
* Total cultivated area
* Average yield
* Number of states
* Number of crops
* Production by crop
* Production by state

### Step 12: Save Clean Dataset

The final cleaned dataset is saved as:

```text
agriculture_cleaned.csv
```

---

## 7. How to Run the Project

### Step 1: Install Python

Install Python from:

https://www.python.org/downloads/

During installation, enable:

```text
Add Python to PATH
```

### Step 2: Install Visual Studio Code

Install VS Code from:

https://code.visualstudio.com/

Install the Python extension from the VS Code Extensions section.

### Step 3: Open the Project

Open the `Agriculture_Data_Project` folder in VS Code.

### Step 4: Open Terminal

Select:

```text
Terminal → New Terminal
```

### Step 5: Install Libraries

Run:

```bash
pip install pandas numpy scikit-learn
```

### Step 6: Run the Program

Run:

```bash
python agriculture_cleaning.py
```

If `python` does not work, try:

```bash
python3 agriculture_cleaning.py
```

---

## 8. Expected Output

After successful execution, the terminal will display information such as:

```text
Dataset loaded successfully!

--- FIRST 5 RECORDS ---

--- DATASET SIZE ---

--- MISSING VALUES BEFORE CLEANING ---

Duplicate rows found:

Text columns cleaned.

Numerical columns converted.

Date column converted.

Yield column created.

Numerical features scaled.

--- MISSING VALUES AFTER CLEANING ---

--- AGRICULTURE SUMMARY ---

--- TOTAL PRODUCTION BY CROP ---

--- TOTAL PRODUCTION BY STATE ---

CLEANING COMPLETED SUCCESSFULLY!

Cleaned dataset saved as:
agriculture_cleaned.csv
```

---

## 9. Project Workflow

```text
Raw Agriculture Dataset
          |
          v
     Load CSV File
          |
          v
    Check Data Quality
          |
          v
   Remove Duplicates
          |
          v
    Handle Missing Data
          |
          v
     Clean Text Data
          |
          v
  Convert Data Types
          |
          v
     Convert Dates
          |
          v
    Create Yield Feature
          |
          v
     Scale Features
          |
          v
   Generate Summaries
          |
          v
 Save Cleaned Dataset
```

---

## 10. Objective

The main objective of this project is to transform raw agricultural data into a clean and structured dataset that can be used for:

* Agricultural data analysis
* Crop production analysis
* State-wise production comparison
* Crop yield analysis
* Data visualization
* Machine learning
* Future agricultural prediction projects

---

## 11. Future Improvements

The project can be extended in the future by adding:

1. Data visualization using Matplotlib.
2. Crop production prediction.
3. Weather data integration.
4. Soil data integration.
5. Machine learning models.
6. Crop yield prediction.
7. Interactive dashboards.
8. Web-based agricultural analytics.

---

## 12. Conclusion

This project provides a simple and systematic approach to agricultural data preparation. The raw dataset is loaded, checked, cleaned, transformed, and saved as a new cleaned dataset.

The process improves data quality and prepares the information for future analysis and machine learning applications.

The project is designed to be easy to understand and execute using Python and Visual Studio Code.
