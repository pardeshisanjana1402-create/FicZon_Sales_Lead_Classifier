# FicZon_Sales_Lead_Classifier
A machine learning project to predict sales lead conversion using classification models and data analysis techniques.

## Project Structure

FicZon-Sales-Lead-Classifier/
│
├── data/
│   ├── final_merged_dataset.csv
│
├── notebooks/
│   ├── data_preprocessing.ipynb
│   ├── eda_analysis.ipynb
│   ├── model_training.ipynb
│   └── final_report.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── eda.py
│   ├── models.py
│   └── evaluation.py
│
├── outputs/
│   ├── plots/
│   ├── confusion_matrix.png
│   └── feature_importance.png
│
├── README.md
└── requirements.txt

## Database Connection (MySQL)

In this project, the dataset was connected using a MySQL database and loaded into Python for further analysis and model building.

### Steps:
- Established connection to MySQL database using `mysql.connector`
- Queried required data from the database
- Loaded data into a Pandas DataFrame
- Closed the connection after fetching data

### Sample Code

```python
import pandas as pd
import mysql.connector

# Establish MySQL connection
conn = mysql.connector.connect(
    host="localhost",
    user="root",
    password="your_password",
    database="sales_lead_db"
)

# SQL query
query = "SELECT * FROM sales_leads_data"

# Load data into DataFrame
df = pd.read_sql(query, conn)

# Close connection
conn.close()

# Preview data
print(df.head())
---

## Project Goal

```markdown
## Project Goal

To build a machine learning model that predicts whether a sales lead will convert into a customer, helping businesses focus on high-potential leads.

## Data Preprocessing

* Load dataset
* Handle missing values
* Convert date columns into proper format
* Encode categorical variables
* Remove duplicates
* Prepare clean dataset
* Save cleaned data into `data/cleaned/`


## Exploratory Data Analysis (EDA)

* Analyze feature distributions
* Plot lead conversion rate
* Study relationships between variables
* Create countplots and histograms
* Identify key factors affecting conversion


## Model Building

**Models used:**

* Logistic Regression
* Decision Tree
* Random Forest

**Evaluation metrics:**

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC Score
* Confusion Matrix

Compare models and select the best performing one.


## Final Report

* Summary of dataset
* Key insights from EDA
* Model performance comparison
* Best model explanation
* Final conclusion


## Technplogies Used 

pandas
numpy
matplotlib
seaborn
scikit-learn

## Author

**Sanjana M. Pardeshi**
Machine Learning | Data Science
