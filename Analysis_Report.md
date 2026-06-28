DEVELOPERS ARENA – DATA SCIENCE INTERNSHIP
Week 3 task documentation
 
**Project Overview**
The objective of this project is to analyze a sales dataset using Python and the Pandas library. The program loads the dataset, removes missing values, calculates important sales metrics, and displays a simple sales report. This project helps in understanding basic data analysis using Python.
**Setup Instructions**
Open Google Colab.
Create a new notebook.
Copy and paste the Python code.
Run the first cell.
Click Choose Files and upload sales_data.csv.
Run the remaining cells.
The sales report will be displayed.
**Technical Details**
The project uses the following Pandas functions:
pd.read_csv() – Reads the CSV file.
isnull().sum() – Checks missing values.
dropna() – Removes missing values.
groupby() – Groups products together.
sum() – Calculates totals.
mean() – Calculates average sales.
idxmax() – Finds the best-selling product.
print() – Displays the report.


**How the Technical Requirements Were Met
Requirement**
How It Was Met
Use Pandas to load and analyze data
Used pd.read_csv() to load the dataset and Pandas functions to analyze it.
Handle missing values
Used isnull().sum() to check missing values and dropna() to remove them.
Calculate at least 3 different metrics
Calculated Total Sales, Best-Selling Product, Total Quantity Sold, and Average Sales.
Create a clean, formatted report
Displayed all results clearly using print() statements.
Add comments explaining each step
Added comments throughout the code for better readability.



·     Code Structure (With code and structure explained)




# ==========================================
# SALES DATA ANALYSIS USING PANDAS
# ==========================================


# Import required libraries
import pandas as pd
from google.colab import files


# ------------------------------------------
# Step 1: Upload the CSV File
# ------------------------------------------
print("Please upload the sales_data.csv file.")


uploaded = files.upload()


# ------------------------------------------
# Step 2: Read the Dataset
# ------------------------------------------
df = pd.read_csv("sales_data.csv")


# Display the first 5 rows
print("\nDataset Preview:")
print(df.head())


# ------------------------------------------
# Step 3: Check for Missing Values
# ------------------------------------------
print("\nMissing Values in Each Column:")
print(df.isnull().sum())


# Remove rows with missing values
df = df.dropna()


print("\nMissing values have been removed.")


# ------------------------------------------
# Step 4: Calculate Sales Metrics
# ------------------------------------------


# Total Sales
total_sales = df["Total_Sales"].sum()


# Total Quantity Sold
total_quantity = df["Quantity"].sum()


# Average Sales
average_sales = df["Total_Sales"].mean()


# Best Selling Product
best_product = df.groupby("Product")["Quantity"].sum().idxmax()


# Number of Products Sold
number_of_products = df["Product"].nunique()


# ------------------------------------------
# Step 5: Generate Sales Report
# ------------------------------------------


print("\n")
print("=" * 40)
print("        SALES ANALYSIS REPORT")
print("=" * 40)


print("Total Sales Revenue      :", total_sales)
print("Total Quantity Sold      :", total_quantity)
print("Average Sale Amount      :", round(average_sales, 2))
print("Best Selling Product     :", best_product)
print("Number of Products       :", number_of_products)


print("=" * 40)
print("Analysis Completed Successfully!")
print("=" * 40)

Imported the required libraries (pandas and Google Colab files module).
Uploaded and loaded the sales dataset into a DataFrame.
Cleaned the data by removing missing values.
Calculated key sales metrics such as total sales, average sales, total quantity sold, and best-selling product.
Displayed the analysis in a formatted sales report




Visual Documentation 
A successful code and its output 
**code**
<img width="963" height="493" alt="sales data code 1" src="https://github.com/user-attachments/assets/e3f10355-d5a7-4bd5-b650-7b05fc6f4bea" />
<img width="957" height="484" alt="sales data code 2" src="https://github.com/user-attachments/assets/20893493-133c-4cf8-b28d-5d6f980be4d4" />
<img width="967" height="495" alt="sales data 3" src="https://github.com/user-attachments/assets/89e1e6a7-6a69-4782-b9fa-3715d815d6ab" />
<img width="970" height="494" alt="sales data 4" src="https://github.com/user-attachments/assets/4699ac2d-c67a-4c79-ab36-71f89ab3ea92" />

**output**
<img width="962" height="488" alt="output" src="https://github.com/user-attachments/assets/5cb7f16c-838c-45e3-a7c3-7b48bebcda76" />









