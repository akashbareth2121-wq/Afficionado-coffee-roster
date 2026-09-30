# Product Optimization & Revenue Contribution Analysis — Afficionado Coffee Roasters

An interactive dashboard analyzing transaction-level sales data from a coffee retailer to identify revenue drivers, underperforming products, and menu optimization opportunities.

**Live dashboard:** https://coffee-revenue-dashboard-2026.streamlit.app/

## The Problem

A coffee retailer's menu has dozens of products across coffee, tea, bakery, and other categories, but not every item pulls its weight. Without breaking revenue down by product and category, it's easy to keep underperforming items on the menu simply because no one has quantified how little they actually contribute. This project analyzes 149K+ transaction records to find out which products are genuinely driving revenue, and which ones are just taking up shelf space.

## What I Found

**Category-level split:** Coffee is the dominant category at 38.6% of revenue, followed by Tea at 28.1%. Bakery (11.8%), Drinking Chocolate (10.4%), and Coffee Beans (5.7%) make up most of the rest, with a long tail of smaller categories contributing the final 5.4%.

**Revenue concentration (Pareto):** Across the full catalog of 80 product types, 42 products — 52.5% of the catalog — generate 80% of total revenue. The remaining 38 products (47.5% of the catalog) generate only 20%. That's a much flatter concentration curve than a classic 80/20 split, which tells a different story than "a few products carry the business" — here, revenue is spread across a genuinely large share of the menu, and the long tail is proportionally large too. This flatness also shows up at the individual product level: the single top product accounts for only 3.03% of total revenue — compare that to a business with one dominant hero SKU, where the top product alone might carry 15-20%.

**Scale of the business:** Across the full dataset, total sales volume reached 214,470 units, at an average revenue of ₹3.26 per unit.

**Product segmentation:** Classifying products by revenue and sales volume into Hero, Potential, and Dead categories showed 41 products as high performers actively driving the business, against 35 underperforming products. The single strongest performer was Sustainably Grown Organic (Lg), driving the highest revenue in the catalog. The clearest underperformer was Dark Chocolate, showing up in the bottom 10 products by revenue with consistently low contribution — a direct candidate for removal or repositioning.

**Operational pattern:** Sales peak at 10:00 and hit their lowest point at 20:00 — a finding that goes beyond product-level analysis into staffing and inventory timing, and wasn't something I set out to look for, but the hourly breakdown made it obvious.

## A Real Technical Problem I Ran Into

I was new to building heatmaps and Pareto charts in this level of detail, and both gave me real trouble before they looked right. The heatmap's color scale and cell sizing were the hardest part — the default settings either washed out the differences between mid-range values or made the extremes so dominant that nothing else was readable. I had to manually tune the color scale until the contrast actually matched the data instead of just looking colorful.

The Pareto chart had a separate problem: with dozens of product labels on the x-axis, the default horizontal labels overlapped into an unreadable blur. I had to rotate the axis labels to make them legible without cutting product names short.

On top of that, getting the overall dashboard color theme to feel intentional (rather than default Streamlit styling) took several iterations — small thing, but it's the difference between a dashboard that looks like a template and one that looks designed.

## Core Analytical Areas

- **Product Performance** — top/bottom products by revenue and volume, product ranking
- **Revenue Contribution** — product-wise and category-wise revenue share
- **Pareto Analysis (80/20)** — revenue concentration and long-tail detection
- **Demand Analysis** — revenue by hour, category demand patterns
- **Product Segmentation** — Hero / Potential / Dead classification by revenue vs. sales volume

## Key KPIs

| KPI | Definition |
|---|---|
| Top Product Share | Highest single product's revenue ÷ Total revenue |
| Sales Volume | Total units sold across the full catalog |
| Revenue Share | Selected segment's revenue ÷ Total revenue |
| Concentration | % of products required to generate 80% of total revenue |
| Revenue per Unit | Total revenue ÷ Total units sold |

## Tech Stack

| Category | Tools |
|---|---|
| Language | ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) |
| Data Processing | ![Pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white) |
| Visualization | ![Matplotlib](https://img.shields.io/badge/Matplotlib-ffffff?style=for-the-badge&logo=plotly&logoColor=black) ![Seaborn](https://img.shields.io/badge/Seaborn-4C78A8?style=for-the-badge) ![Plotly](https://img.shields.io/badge/plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white) |
| Dashboard | ![Streamlit](https://img.shields.io/badge/streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white) |

## Dashboard Features

- Interactive filtering by category, product type, and store location
- Adjustable "Top N Products" view
- Revenue Contribution Tree (treemap) broken down by category and sub-category
- Product Ranking, Revenue Concentration (Pareto), and Product Performance Matrix views
- Hourly demand heatmap showing peak and low-demand periods

## Project Structure

```
Afficionado-coffee-roaster/
├── app.py
├── requirements.txt
├── Afficionado Coffee Roasters.xlsx
├── Final_research_paper.pdf
├── .devcontainer/
├── .gitignore
├── .gitattributes
└── README.md
```

## Run It Locally

```bash
git clone https://github.com/Pratham719/Afficionado-coffee-roster.git
cd Afficionado-coffee-roaster
pip install -r requirements.txt
streamlit run app.py
```

## What I'd Do Differently

Given more time, I'd connect the operational finding (peak at 10:00, low at 20:00) back to the product segmentation — right now they're two separate views, but the more useful analysis would show whether Hero products and Dead products have different demand curves throughout the day, which would make the recommendation more actionable for staffing and inventory decisions, not just menu decisions.

## About

Built by Pratham Rangoonwala, Data Analyst Intern at Unified Mentor, as an independent portfolio project.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pratham-ds/)
[![Streamlit](https://img.shields.io/badge/Live_Dashboard-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://coffee-revenue-dashboard-2026.streamlit.app/)
