# 📊 Week 1 Internship Task – Edunet Foundation

## 🔍 Task Overview

This task involves performing data preprocessing and exploratory data analysis (EDA) on weather datasets collected from Kaggle. The goal is to clean, merge, analyze, and visualize the data to uncover meaningful patterns and detect any anomalies.

## 📁 Files Used

The following CSV files were used, each representing weather data from a different city:

- `692cbfc6503c10120449.csv` – Vizag  
- `ea3477533b1820120449.csv` – Hyderabad  
- `71085754c7aa13120449.csv` – Chennai  
- `6d67bef1862831120449.csv` – Mumbai  

## 📌 Steps Performed

### 1. **Importing Libraries**
Key Python libraries like `pandas`, `matplotlib`, and `seaborn` were imported for data handling and visualization.

### 2. **Loading and Labeling Data**
Each dataset was read using `pandas.read_csv()` and a new column `Location` was added to indicate the city of origin for each file.

### 3. **Merging Datasets**
All four datasets were merged into a single DataFrame using `pd.concat()`, resulting in a comprehensive dataset containing weather data across four locations.

### 4. **Saving and Downloading**
The merged dataset was saved as `merged_locations.csv` and downloaded using `files.download()` in Google Colab.

### 5. **Data Overview**
Basic inspection steps were performed:
- `.info()` to view data types and non-null counts.
- `.describe()` for statistical summary.
- `.isnull().sum()` to detect missing values.
- `.duplicated().sum()` to find duplicates.

### 6. **Encoding Categorical Data**
The `Location` column was encoded using one-hot encoding to prepare the dataset for analysis.

### 7. **Outlier Detection**
Outliers for numeric columns such as `temperature_2m`, `windspeed_10m`, `Power`, etc., were detected using the **IQR (Interquartile Range)** method. Outliers were stored and can be viewed per column.

### 8. **Data Visualization**
- **Box Plots**: Visualized distributions and identified outliers for each numeric column.
- **Pair Plot**: Displayed relationships and distributions across all selected features.

## 📊 Columns Analyzed
- `temperature_2m`
- `relativehumidity_2m`
- `dewpoint_2m`
- `windspeed_10m`
- `windspeed_100m`
- `winddirection_10m`
- `winddirection_100m`
- `windgusts_10m`
- `Power`

## ✅ Outcome
Successfully merged and cleaned four weather datasets, conducted an outlier analysis, and visualized the data to understand feature distributions and correlations. This forms a strong foundation for deeper statistical analysis and predictive modeling in upcoming weeks.
