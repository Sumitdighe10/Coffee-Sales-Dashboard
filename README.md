# ☕ Coffee Sales Analytics Dashboard 📊  

## 📌 Overview  
This **Excel-based interactive dashboard** analyzes coffee sales data from **2019-2022**, leveraging **Pivot Tables, Pivot Charts, and Excel formulas** to extract meaningful insights. The project demonstrates **data gathering, transformation, and visualization** for financial and sales analysis.  

## 🚀 Features  
- **🔹 Data Cleaning & Integration**  
  - Used **XLOOKUP** to merge `Customer ID` with `Customer Name`, `Email`, and `Country`.  
  - Applied **INDEX/MATCH** to dynamically retrieve `Coffee Type`, `Roast Type`, `Size`, and `Unit Price`.  
  - Ensured a structured dataset by **removing duplicates and formatting columns** properly.  
- **📊 Dynamic Filtering & Visualization**  
  - **Slicers & Timeline** for real-time filtering by `Roast Type`, `Size`, `Loyalty Card`, and `Date Range`.  
  - **Pivot Charts & Tables** for insights into sales trends, top customers, and country-based performance.  
- **📈 Sales Insights**  
  - Identified a **13% YoY sales increase** in 2021.  
  - **Top 5 customers** contributed **22% of total revenue**.  
  - Sales distribution visualized across **United States, Ireland, and UK**.  

---

## 🛠 Tech Stack  
- **Microsoft Excel**: Pivot Tables, Pivot Charts, XLOOKUP, INDEX/MATCH  
- **Data Visualization**: Interactive dashboard with slicers & timeline  
- **Data Processing**: Excel formulas for data transformation & aggregation  

---

## 📁 Excel Formulas Used  

### **1⃣ XLOOKUP - Customer Data Retrieval**  
Fetching **Customer Name** based on `Customer ID`:  
```excel
=XLOOKUP(C2, Customers!A:A, Customers!B:B, "Not Found")
```
Fetching **Email Address** using `Customer ID`:  
```excel
=XLOOKUP(C2, Customers!A:A, Customers!C:C, "Not Found")
```
Fetching **Country** for each order:  
```excel
=XLOOKUP(C2, Customers!A:A, Customers!G:G, "Unknown")
```

### **2⃣ INDEX/MATCH - Product Data Lookup**  
Fetching `Coffee Type`, `Roast Type`, `Size`, and `Unit Price` from `Products` table:  
```excel
=INDEX(Products!B:B, MATCH(D2, Products!A:A, 0))
```
Fetching **Roast Type** based on `Product ID`:  
```excel
=INDEX(Products!C:C, MATCH(D2, Products!A:A, 0))
```
Fetching **Size** based on `Product ID`:  
```excel
=INDEX(Products!D:D, MATCH(D2, Products!A:A, 0))
```
Fetching **Unit Price** dynamically:  
```excel
=INDEX(Products!E:E, MATCH(D2, Products!A:A, 0))
```

### **3⃣ Sales Calculation**  
Total Sales for each order:  
```excel
=L2 * E2
```
Where:
- `L2` = **Unit Price**
- `E2` = **Quantity Ordered**  

---

## 🌟 Dashboard Components  

The final dashboard includes the following **visual elements**:  

1⃣ **📊 Total Sales Over Time** (Line Chart)  
   - **Shows monthly sales trends** for each `Coffee Type`.  
   - Uses a **date-based timeline slicer** for filtering.  

2⃣ **🌍 Sales By Country** (Bar Chart)  
   - Visualizes **sales performance by country** (`US`, `Ireland`, `UK`).  

3⃣ **👥 Top 5 Customers** (Bar Chart)  
   - Highlights the **top five customers by total sales**.  

4⃣ **🔎 Interactive Filters** (Slicers)  
   - **Roast Type**: `Dark`, `Light`, `Medium`.  
   - **Size**: `0.2 kg`, `0.5 kg`, `1 kg`, `2.5 kg`.  
   - **Loyalty Card**: `Yes`, `No`.  
   - **Order Date Timeline** (to adjust date ranges).  

---

## 📸 Screenshots  
![Dashboard Screenshot](Dashboard%20Screenshot.png)  

---

## 💾 How to Use  
1. **Download** 📂 `Coffee_Sales_Dashboard.xlsx`  
2. **Open in Microsoft Excel** 🖥️  
3. **Interact** with slicers & timeline to filter data dynamically  

---


---

## 👨‍💻 Author  
[Sumit Dighe](https://github.com/Sumitdighe10)  

---
