# ☕ Coffee Shop Sales Analytics

An interactive data analytics dashboard built to analyze coffee shop transaction data and identify **revenue drivers, product performance, customer demand patterns, and menu optimization opportunities**.

**Live Dashboard:** [Add your Streamlit live link here]

## 📊 Project Overview

This project analyzes **149K+ transaction records** from a coffee retailer to understand which products and categories contribute most to revenue, which products underperform, and how sales vary throughout the day.

The goal is to transform raw transaction data into actionable business insights using **Python, Pandas, NumPy, Matplotlib, Seaborn, Plotly, and Streamlit**.

## 🔍 Key Insights

### Category Performance

* Coffee contributes approximately **38.6% of total revenue**.
* Tea contributes approximately **28.1%**.
* Bakery contributes approximately **11.8%**.
* Drinking Chocolate contributes approximately **10.4%**.
* Coffee Beans contribute approximately **5.7%**.

### Revenue Concentration

* The dataset contains **80 product types**.
* **42 products (52.5%)** generate approximately **80% of total revenue**.
* The remaining **38 products (47.5%)** contribute approximately **20%**.
* The top individual product contributes around **3.03% of total revenue**, indicating that revenue is distributed across a broad range of products.

### Sales Volume

* Total sales volume: **214,470 units**
* Average revenue per unit: approximately **₹3.26**

### Product Performance

Products were segmented based on revenue and sales volume into:

* **Hero Products** — high revenue and high sales performance
* **Potential Products** — products with growth opportunities
* **Dead Products** — relatively low revenue and sales contribution

The analysis identified **41 high-performing products** and **35 underperforming products**.

### Demand by Hour

* Sales reach their highest level around **10:00 AM**.
* Sales reach their lowest level around **8:00 PM**.
* This provides useful information for **staffing, inventory planning, and operational decisions**.

## 📈 Core Analysis

* **Product Performance** — Top and bottom products by revenue and sales volume
* **Revenue Contribution** — Product-wise and category-wise revenue analysis
* **Pareto Analysis** — Identification of revenue concentration and long-tail products
* **Demand Analysis** — Sales trends by hour and category
* **Product Segmentation** — Hero, Potential, and Dead product classification

## 📌 Key KPIs

| KPI                   | Definition                                        |
| --------------------- | ------------------------------------------------- |
| Top Product Share     | Top product revenue ÷ Total revenue               |
| Sales Volume          | Total units sold                                  |
| Revenue Share         | Segment revenue ÷ Total revenue                   |
| Revenue Concentration | % of products required to generate 80% of revenue |
| Revenue per Unit      | Total revenue ÷ Total units sold                  |

## 🛠️ Tech Stack

| Category      | Tools                           |
| ------------- | ------------------------------- |
| Programming   | Python                          |
| Data Analysis | Pandas, NumPy                   |
| Visualization | Matplotlib, Seaborn, Plotly     |
| Dashboard     | Streamlit                       |
| Data Source   | Coffee shop transaction dataset |

## 🎯 Dashboard Features

* Interactive filtering by category
* Product-level analysis
* Store/location filtering
* Adjustable Top-N product analysis
* Revenue contribution treemap
* Product ranking
* Pareto revenue analysis
* Product performance matrix
* Hourly sales heatmap
* Revenue and sales-volume analysis

## 📂 Project Structure

```text
Coffee-Shop-Sales-Analytics/
│
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
├── data/
│   └── coffee_sales_data.xlsx
│
└── Final_research_paper.pdf
```

## 🚀 Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/akashbareth2121-wq/coffee-shop-sales-analytics.git
```

### 2. Open the project

```bash
cd coffee-shop-sales-analytics
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Streamlit dashboard

```bash
streamlit run app.py
```

The dashboard will open in your browser.

## 💡 Challenges & Learning

One of the main challenges was creating readable and meaningful visualizations from a large transaction dataset.

The **heatmap** required careful tuning of the color scale so that both high- and medium-demand periods remained visible.

The **Pareto chart** also required customization because the large number of product names caused overlapping labels. Axis rotation and formatting were used to improve readability.

Another learning experience was customizing the Streamlit dashboard so that it looked like a dedicated analytics application rather than a default Streamlit template.

## 🔮 Future Improvements

Future versions of this project could:

* Connect product segmentation with hourly demand
* Analyze Hero and Dead product demand throughout the day
* Add customer-level purchasing analysis
* Add sales forecasting
* Add inventory optimization
* Add automated business recommendations
* Deploy the dashboard with a custom domain

## 👨‍💻 About

**Built by Akash Bareth**

Data Analyst | Python | SQL | Data Visualization

This project was developed as a portfolio project to demonstrate practical skills in **data cleaning, exploratory data analysis, business analytics, data visualization, and interactive dashboard development**.

### 🔗 Connect With Me

* **GitHub:** https://github.com/akashbareth2121-wq
* **LinkedIn:** https://www.linkedin.com/in/akash-bareth-36660a420/

---

⭐ If you found this project useful, consider giving the repository a star!
