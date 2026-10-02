 
# Medical Insurance Cost Analysis & Machine Learning

## Project Overview

This project analyzes a medical insurance dataset using Python, Pandas, NumPy, Matplotlib, and Seaborn.

The main objective is to understand the factors associated with medical insurance charges and prepare the dataset for machine learning.

The project includes:

* Data loading and understanding
* Exploratory Data Analysis (EDA)
* Missing-value checking
* Duplicate removal
* Data type checking
* Categorical data encoding
* Feature engineering
* BMI categorization
* Standardization of numerical features
* Dataset preparation for machine learning

## Dataset

The dataset contains **1,338 records and 7 columns** before duplicate removal.

### Features

| Column     | Description                   |
| ---------- | ----------------------------- |
| `age`      | Age of the individual         |
| `sex`      | Gender                        |
| `bmi`      | Body Mass Index               |
| `children` | Number of children/dependents |
| `smoker`   | Smoking status                |
| `region`   | Residential region            |
| `charges`  | Medical insurance charges     |

After duplicate removal, the notebook contains **1,337 records**.

## Data Cleaning

The following preprocessing steps were performed:

1. Checked dataset shape and columns.
2. Checked missing values.
3. Checked data types.
4. Rounded BMI and insurance charges.
5. Removed duplicate records.
6. Converted categorical variables into numerical representations.
7. Renamed:

   * `sex` → `is_Gender`
   * `smoker` → `is_smoker`
8. Applied one-hot encoding to the `region` column.
9. Converted encoded columns to integer format.
10. Standardized numerical features using `StandardScaler`.

The notebook reports **zero missing values** in all seven original columns.

## Exploratory Data Analysis

### Dataset Statistics

Before duplicate removal:

* Records: **1,338**
* Features: **7**
* Average age: **39.21 years**
* Average BMI: **30.66**
* Average children/dependents: **1.09**
* Average insurance charges: **13,270.42**
* Maximum insurance charges: **63,770.43**

### Smoking Distribution

The dataset contains:

* **1,064 non-smokers**
* **274 smokers**

This means smokers represent approximately **20.5%** of the original dataset.

### Gender Distribution

The dataset contains:

* **675 males**
* **662 females**

The gender distribution is relatively balanced.

### Region Distribution

The original dataset contains:

| Region    | Records |
| --------- | ------: |
| Southeast |     364 |
| Southwest |     325 |
| Northwest |     325 |
| Northeast |     324 |

The Southeast region has the highest number of records in the dataset.

### Children Distribution

The number of children/dependents is distributed as follows:

| Children | Records |
| -------: | ------: |
|        0 |     574 |
|        1 |     324 |
|        2 |     240 |
|        3 |     157 |
|        4 |      25 |
|        5 |      18 |

Individuals with zero children/dependents form the largest group.

## Feature Engineering

BMI was converted into categories using the following ranges:

* Underweight
* Normal
* Overweight
* Obese

The notebook's resulting categories contain:

| BMI Category | Records |
| ------------ | ------: |
| Obese        |     706 |
| Overweight   |     386 |
| Normal       |     221 |
| Underweight  |      24 |

These categories were then converted into dummy variables for further analysis/model preparation.

## Feature Scaling

`StandardScaler` was applied to:

* `age`
* `bmi`
* `children`

This transforms numerical features to a standardized scale, which can be useful before applying many machine-learning algorithms.

## Key Insights

Based on the analysis performed in the notebook:

1. The dataset contains **1,338 observations** and **7 original features**.
2. No missing values were detected.
3. One duplicate record was removed, leaving **1,337 records**.
4. The dataset contains more non-smokers than smokers.
5. Male and female records are relatively balanced.
6. Southeast has the largest number of records among the four regions.
7. Most individuals have zero children/dependents.
8. The BMI categorization shows that the **Obese** category is the largest group in the processed data.
9. Insurance charges have a wide range, from approximately **1,121.87 to 63,770.43** in the original data.
10. The processed dataset was prepared with encoded categorical features and standardized numerical features for potential machine-learning use.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## Project Structure

```text
Medical-Insurance-Analysis/
│
├── Machine_learning.ipynb
├── insurance.csv
└── README.md
```

## How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Install required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 3. Open Jupyter Notebook

```bash
jupyter notebook
```

### 4. Open

```text
Machine_learning.ipynb
```

Make sure `insurance.csv` is available in the same project directory.

## Future Improvements

The next stage of this project can include:

* Train-test split
* Linear Regression
* Decision Tree Regression
* Random Forest Regression
* Model evaluation using MAE, MSE, RMSE, and R²
* Hyperparameter tuning
* Feature importance analysis
* Actual insurance-charge prediction
* Model deployment using Streamlit or FastAPI

## Conclusion

This project demonstrates a complete **data preprocessing and exploratory analysis workflow** for a medical insurance dataset.

The dataset was inspected, cleaned, transformed, encoded, feature-engineered, and standardized, making it suitable for the next stage of machine-learning model development.
