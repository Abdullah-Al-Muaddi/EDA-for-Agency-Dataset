---

# **Exploratory Data Analysis (EDA) for Saudi Arabia Attorney (Agency) Dataset**

## **Overview**
This project performs exploratory data analysis (EDA) on multiple CSV files containing attorney (agency) data from different months in Saudi Arabia. The goal is to merge the files, clean the data, and provide insightful visualizations.

### **Tasks**
1. **Merge Data**: Combine multiple CSV files into one dataset.
2. **Data Cleaning**:
   - Check for null and duplicate values.
   - Convert data types.
   - Add new columns for better analysis.
3. **Data Visualization**: Create visual representations of the dataset.
4. **Download the cleaned and processed dataset**.

---

## **Setup & Requirements**
To run this project, you need to install the following Python libraries:
- **Pandas**: For data manipulation.
- **NumPy**: For numerical operations.
- **Matplotlib** & **Seaborn**: For creating static visualizations.
- **Plotly**: For creating interactive visualizations.
- **gdown**: To download files from Google Drive.
- **Arabic Reshaper**: To handle Arabic text formatting for the plots.

You can install the necessary libraries using the following commands:
```bash
pip install arabic_reshaper plotly gdown pandas numpy matplotlib seaborn
```

---

## **Steps to Run the Project**

1. **Download Attorney (Agency) Files**:
   Use `gdown` to download CSV files from Google Drive. The dataset includes files from November 2023, December 2023, January, February, and March.

2. **Merge Files**:
   The CSV files are read into Pandas DataFrames and then concatenated into a single DataFrame.

3. **Data Cleaning**:
   - Drop irrelevant columns (e.g., `التاريخ هجري`).
   - Handle missing values by dropping rows with null data.
   - Remove duplicate rows.
   - Convert columns to appropriate data types (e.g., convert string dates to datetime and numeric columns).
   
4. **Add New Features**:
   - Extract `الشهر`, `اليوم`, and `ايام الاسبوع` from the date column.
   - Calculate the cumulative number of agencies issued per day using the `groupby()` function.

5. **Data Visualization**:
   Several plots are generated to provide insights, including:
   - Histogram of agencies issued per day.
   - Bar plot showing the distribution of agencies by region.

6. **Download Processed File**:
   After cleaning and analyzing the data, the final dataset can be saved and downloaded for further use.

---

## **Visualizations**

1. **Distribution of Agencies Issued by Day**:
   - This plot shows how the number of agencies issued varies across the days of the month.

2. **Distribution of Agencies by Region**:
   - A bar plot depicting the total number of agencies issued per region, highlighting regional differences in agency issuance.

---

## **Conclusion**
This EDA provides a cleaned and structured dataset with key insights into agency issuance trends in Saudi Arabia. The code is designed to handle Arabic text, ensuring that Arabic columns and labels are correctly displayed in visualizations.

Feel free to extend this analysis or integrate the cleaned dataset into further projects!

---
