# 📊 Laptop Price Prediction Project

## 📌 Project Overview
This project focuses on analyzing laptop data and preparing it for machine learning.  
The goal is to clean raw data, perform feature engineering, visualize patterns, and prepare the dataset for model training.

---

## 📦 Libraries Used

- pandas → data handling  
- numpy → numerical operations  
- matplotlib → data visualization  
- sklearn → machine learning tools  

---

## 📂 Dataset Description

The dataset contains information about laptops such as:

- Company (Brand name)
- RAM
- Storage (SSD/HDD)
- Weight
- Operating System
- Price

---

## 🔍 Data Exploration

Initial steps include:

- Viewing first few rows using `head()`
- Checking dataset shape (rows and columns)
- Understanding data types using `info()`

These steps help in identifying missing values and data structure.

---

## 🧹 Data Cleaning

### Removing Unnecessary Columns

Columns like:
- Unnamed: 0
- ScreenResolution
- TypeName  

were removed because they are not useful for prediction.

---

### Handling Missing Values

- Rows with missing RAM values were removed.
- This ensures data quality for machine learning.

---

## 🔧 Feature Engineering

### RAM Processing

- Removed "GB" from RAM column
- Converted it into integer format
- Created new column: `Ram(GB)`

---

### Memory Processing

- Removed text like SSD, HDD, Flash Storage
- Converted TB into GB (1TB = 1000GB)
- Cleaned storage values for consistency

---

### SSD & HDD Extraction

- Extracted SSD and HDD values into separate columns
- Missing values filled with 0

---

### Weight Processing

- Removed "kg" from weight column
- Converted it into numeric format

---

### Price Conversion

- Converted price into integer format
- Required for machine learning model

---

### Feature Creation

A new HDD column was created based on price:

- Price > 30000 → 1024 GB
- 20000 < Price ≤ 30000 → 512 GB
- Price ≤ 20000 → 0 GB

This helps in improving model learning.

---

## 📊 Data Visualization

### Scatter Plot

- Shows relationship between company and price
- Helps identify trends

---

### Bar Chart

- Displays average price of laptops by company
- Uses different colors for better visualization

---

### Bar Chart with Values

- Shows exact values on top of bars
- Improves readability

---

## 🤖 Train-Test Split

Dataset is divided into:

- Training data (80%)
- Testing data (20%)

This helps in evaluating model performance and avoiding overfitting.

---

## 📌 Final Output

After preprocessing:

- Data is clean and structured  
- Features are properly engineered  
- Dataset is ready for machine learning  

---

## 🚀 Conclusion

This project demonstrates:

- Data cleaning techniques  
- Feature engineering methods  
- Data visualization skills  
- Preparation for machine learning  

---

## 🔮 Future Scope

- Apply machine learning models (Linear Regression, etc.)
- Improve prediction accuracy
- Deploy model using Streamlit
- Build interactive dashboard
