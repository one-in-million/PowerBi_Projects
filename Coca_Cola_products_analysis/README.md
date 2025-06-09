# 🥤 Coca-Cola Products Sales Analysis — Power BI Dashboard

This project presents a sales performance dashboard for Coca-Cola products using Power BI. The dashboard delivers interactive visualizations and KPIs that help analyze product-wise and region-wise performance over time.

---

## 📁 Project Structure

Coca_Cola_products_analysis/
├── Dataset/
│ └── coca-cola-sales-data.xlsx
├── screenshots/
│ ├── diet-coke-analysis.jpg
│ ├── overview.jpg
│ └── regional-analysis.jpg
├── coca-cola-dashboard.pbix
└── README.md


---

## 📊 Dataset

The dataset was sourced from a YouTube tutorial and contains mock sales data for Coca-Cola products across various regions.

📂 [Download Dataset](./Dataset/coca-cola-sales-data.xlsx)

- Columns include: Product, Region, Date, Units Sold, Price per Unit, Total Sales, etc.
- Cleaned and pre-processed in Power BI

---

## 📌 Dashboard Highlights

- 📈 Monthly trend of units sold and total sales
- 🥤 Product-wise breakdown (e.g., Diet Coke)
- 🌍 Regional sales comparison
- 🔁 Month-over-month (MoM) growth metrics
- 🧾 Transaction volume and pricing analysis

---

## 🧮 DAX Calculations Used

- **Total Sales**
  ```DAX
  1.Price = AVERAGE(Table1[Price per Unit])
  2.SALES MOM = VAR PM = CALCULATE([Total Sales],DATEADD('Date table'[Date],-1,MONTH))VAR CM =[Total Sales] RETURN IF(AND(CM,PM),CM/PM-1)
  3.Total Sales = SUM(Table1[Total Sales])
  4.Total units MOM = VAR PM = CALCULATE([Total units sold],DATEADD('Date table'[Date],-1,MONTH))VAR CM =[Total units sold] RETURN IF(AND(CM,PM),CM/PM-1)
  5.Total units sold = SUM(Table1[Units Sold])
  6.Transaction Count = COUNTROWS(Table1)

##📸 Screenshots
🔹 Overview Dashboard
🔹 Regional Analysis
🔹 Diet Coke Deep Dive

##🛠️ Tools Used
Power BI Desktop
Microsoft Excel (data source)
DAX for custom measures and calculations

📬 Contact
If you'd like to discuss this project, request a walkthrough, or collaborate:

📧 boomikams2104@gmail.com
🔗 LinkedIn – Boomika M S
💻 GitHub – one-in-million

📌 Note: This dashboard is created for educational and demo purposes based on publicly available sample data.
