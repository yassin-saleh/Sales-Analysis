# 🛍️ Sales Data Dashboard

An interactive Excel-based sales dashboard designed to analyze retail store performance, calculate KPIs, and visualize trends.

---

## 📂 File: `sales_data.xlsm`

This file contains 6 key sheets:

---

### 1. **Retail Store Sales**

The main dataset containing:
- Customer Name  
- Product Category & Name  
- Order & Delivery Dates  
- Quantity and Unit Price  
- Country and Payment Method  
- Total Cost, Revenue, and Net Profit  

#### 🧮 Calculated Fields:

| Column         | Description                                           |
|----------------|-------------------------------------------------------|
| `Year`         | Extracted using `=YEAR(Order Date)`                   |
| `Month`        | Extracted using `=TEXT(Order Date, "mmmm")`           |
| `Day`          | Extracted using `=DAY(Order Date)`                    |
| `Delivery Time`| Days between order and delivery (`=Delivery - Order`) |
| `Total Cost`   | `=Quantity * Unit Cost` or calculated by product %    |
| `Sales Revenue`| `=Quantity * Unit Price`                              |
| `Net Profit`   | `=Sales Revenue - Total Cost`                         |


---

### 2. **Cost Per Unit**

Defines cost percentages for each product to calculate profitability.

| Product     | Cost % |
|-------------|--------|
| Smartphone  | 0.75   |
| Headphones  | 0.65   |
| Laptop      | 0.85   |
| Tablet      | 0.70   |

---

### 3. **KPI**

Displays high-level metrics:
- **Total Cost:** 957,223.45  
- **Sales Revenue:** 1,471,551  
- **Net Profit:** 514,327.55  
- **Customers:** 555  


---

### 4. **Analysis**

This sheet includes both statistical and hypothesis testing tools:

#### 📊 Descriptive Statistics:
- Summary metrics such as **mean**, **median**, **standard deviation**, **minimum**, **maximum**, and more (e.g., **count**, **range**, etc.).
- Applied to key performance indicators like **delivery time**, **quantity**, **unit price**, **sales revenue**, and **net profit**.

![Descriptive Statistics](https://github.com/yassin-saleh/Sales-Analysis/blob/main/SALES%20ANALYSIS/Analysis/Descriptive%20Statistics.png)


#### 🧪 T-Test Analysis:
- Statistical comparison between two groups (e.g., different product categories or payment methods).
- Used to test if there is a **significant difference** in metrics like revenue or profit.
- Implemented using Excel’s `T.TEST()` function.

![T-Test](https://github.com/yassin-saleh/Sales-Analysis/blob/main/SALES%20ANALYSIS/Analysis/T-Test.png)


---

### 5. **SALES FORM**

This sheet allows the user to **input new sales data** directly and dynamically into the system.

#### 🧾 How it works:

- You **fill out** fields like: `Customer Name`, `Product`, `Category`, `Date`, `Quantity`, `Unit Price`, etc.
- After entering the data, you **click the `Submit` button**.
- A macro runs to **automatically transfer the data** into the main **Retail Store Sales** sheet.
- Once submitted:
  - The form **clears itself** (data is erased for next entry).
  - All calculations (Total Cost, Revenue, Net Profit) and dashboard values **update automatically**.
- You can modify or extend the VBA macro logic to suit your business rules.

📌 **Note:** Make sure to enable macros for the submit functionality to work properly.

![Sales Form](https://github.com/yassin-saleh/Sales-Analysis/blob/main/SALES%20ANALYSIS/Sales%20Form/Sales%20Form.png)

---

### 6. **Dashboard**

A visual dashboard for exploring data trends and performance.

![Dashboard](https://github.com/yassin-saleh/Sales-Analysis/blob/main/SALES%20ANALYSIS/DashBoard/DashBoard.png)



