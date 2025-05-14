# **🛠 Exercise 2: Subplots for Bathing Soap & Facewash Sales**  

## **📈 Project Overview**  
This project visualizes **monthly sales data** for bathing soap and facewash using **Matplotlib subplots**. The dataset, stored in `company_sales_data.csv`, is analyzed to identify sales trends and fluctuations over time.  

## **📁 Folder Structure**  
```
exercise_2/
│── company_sales_data.csv  # Dataset file
│── exercise_2.ipynb        # Jupyter Notebook script for Colab
│── README.md               # Documentation file
```

## **🚀 Running the Script in Google Colab**  
### **🔹 Steps**  
1. **Open Google Colab:** [Google Colab](https://colab.research.google.com/)  
2. **Upload the dataset (`company_sales_data.csv`)**  
   - Click the **folder icon** in Colab’s sidebar.  
   - Click **“Upload”**, then select `company_sales_data.csv`.  
3. **Run the following code in a Colab cell**:  
   ```python
   import pandas as pd
   import matplotlib.pyplot as plt

   # Load the dataset
   data = pd.read_csv("company_sales_data.csv")

   # Extract relevant columns
   months = data["month_number"]
   bathing_soap_sales = data["bathingsoap"]
   facewash_sales = data["facewash"]

   # Create subplots
   fig, ax = plt.subplots(2, 1, figsize=(10, 7))  # 2 rows, 1 column

   # Bathing Soap Sales
   ax[0].plot(months, bathing_soap_sales, marker='s', linestyle='--', color='g', label="Bathing Soap")
   ax[0].set_title("Bathing Soap Sales Per Month")
   ax[0].set_ylabel("Units Sold")
   ax[0].legend()
   ax[0].grid(True)

   # Facewash Sales
   ax[1].plot(months, facewash_sales, marker='^', linestyle=':', color='r', label="Facewash")
   ax[1].set_title("Facewash Sales Per Month")
   ax[1].set_xlabel("Month Number")
   ax[1].set_ylabel("Units Sold")
   ax[1].legend()
   ax[1].grid(True)

   plt.tight_layout()
   plt.show()
   ```
✔️ **Press Shift + Enter** to execute the cell, and the subplots will be displayed in Colab! 🎉  

## **📊 Plot Analysis & Results**  
### **Bathing Soap Sales Analysis**  
- Sales started at around **8000 units** in the first month.  
- A **significant drop** to **6000 units** occurred in the second month.  
- Sales **fluctuated between 6000 and 10000 units** over the next several months.  
- A **strong upward trend** appeared in the last quarter, peaking at **12,000 units** in December.  
- This suggests **higher demand towards the year's end**, possibly due to seasonal effects or successful promotions.  

### **Facewash Sales Analysis**  
- Sales started at **1500 units** in January.  
- A **minor dip** to **1200 units** happened in February.  
- Sales remained **steady between 1200 and 1800 units** through most of the year.  
- A **notable increase** in sales emerged from the tenth month, **peaking at 2000 units in November** before slightly dropping to **1800 in December**.  
- The **rise towards the end of the year** might indicate **higher consumer demand or effective marketing**.  

## **📜 Code Explanation**  
✅ **Reads data** from CSV using `pandas.read_csv()`.  
✅ **Creates subplots** (`plt.subplots(2,1)`) for **side-by-side analysis**.  
✅ **Plots sales trends** for both products separately for easy comparison.  
✅ **Adds markers, labels, and grid lines** to improve readability.  


## **⚠️ Common Errors & Fixes**  
### **1️⃣ `FileNotFoundError: company_sales_data.csv`**  
✅ **Issue:** The dataset is missing or not uploaded.  
✅ **Fix:** **Upload the CSV** using the **folder icon in Colab** before running the script.  

### **2️⃣ `ModuleNotFoundError: No module named 'pandas'`**  
✅ **Issue:** Missing required libraries.  
✅ **Fix:** Install dependencies using:  
   ```python
   !pip install pandas matplotlib
   ```

## **🚀 Future Improvements**  
✅ Add **interactive features** (hover for details).  
✅ **Enhance visualization** (custom colors, themes).  
✅ **Compare multiple years of sales data** for trend analysis.  

## **📜 License**  
This project is open-source under the **MIT License**. Feel free to modify and distribute.  
