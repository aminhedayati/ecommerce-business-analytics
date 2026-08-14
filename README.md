# E-Commerce Business Analytics

## Project Overview

This project analyzes the performance of an e-commerce marketplace using historical transaction data. The analysis focuses on revenue, customer behavior, delivery performance, payment behavior, customer reviews, seller performance, and product category performance.

The goal is to identify meaningful business patterns, uncover opportunities and operational issues, and translate the analytical findings into actionable business recommendations.

## Business Questions

The analysis addresses the following business questions:

1. How has marketplace revenue changed over time, and what factors are associated with revenue growth?
2. What customer behavior patterns can be observed, particularly around one-time and repeat purchasing?
3. How does delivery performance relate to customer satisfaction?
4. How does payment behavior vary with order value?
5. What patterns are associated with customer review scores?
6. How concentrated is revenue across sellers?
7. How does product category performance vary in terms of sales volume, revenue, and average item price?
8. Are there geographic patterns or concentrations in marketplace revenue?

## Dataset

This project uses the Brazilian E-Commerce Public Dataset by Olist, which contains anonymized information about orders, customers, sellers, products, payments, reviews, and geolocation.

The dataset is not included in this repository.

Download it from [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce/) and place the extracted files in `data/raw/`.

## Analysis Approach

The analysis follows a structured business analytics workflow:

1. **Data Profiling & Quality** — Examine the structure, completeness, uniqueness, and consistency of the source data.
2. **Metric & Analysis Setup** — Define the analytical grain, core metrics, and business measurement conventions.
3. **Descriptive Analysis** — Analyze revenue, customers, delivery performance, payments, reviews, sellers, and product categories.
4. **Cross-Analysis** — Examine relationships between key business dimensions to identify actionable patterns.
5. **Business Recommendations** — Translate the most relevant findings into practical business opportunities and operational priorities.
6. **Executive Summary** — Consolidate the main findings and recommendations into a concise business-level view.

## Key Findings

- **Revenue growth was primarily volume-driven.** Revenue increased by 137.3%, while order volume increased by 135.1%. Revenue per order increased by only 0.9%.

- **Repeat customers represent a small but high-value segment.** Only 3.12% of customers made repeat purchases, while repeat customers had a higher average spend than one-time customers (259.87 vs. 137.63).

- **Delivery delays are strongly associated with lower customer satisfaction.** Average review scores declined from 4.29 for on-time deliveries to 1.71 for orders delivered 15 or more days late.

- **Revenue is concentrated across sellers, but not dominated by a single seller.** The top 1 seller accounts for 1.72% of total revenue, while the top 10 and top 25 sellers account for 13.27% and 23.81%, respectively.

- **Product category revenue is strongly associated with sales volume.** The correlation between items sold and category revenue is 0.95, while differences in average item price also contribute to variation in category revenue.

- **Revenue is geographically concentrated.** São Paulo accounts for approximately 38.3% of marketplace revenue, while the five highest-revenue states account for approximately 73.9%.

## Business Recommendations

Based on the analysis, the following business priorities are recommended:

1. **Improve delivery reliability** by identifying and addressing the operational causes of late deliveries, particularly severe delays, given their strong association with lower customer satisfaction.

2. **Invest in customer retention** by identifying opportunities to convert one-time customers into repeat buyers, given the higher average spend observed among repeat customers.

3. **Monitor seller concentration** and maintain visibility into high-revenue sellers to manage marketplace dependency and potential seller-side risks.

4. **Prioritize high-value product categories** by considering both sales volume and average item price when evaluating category performance and growth opportunities.

5. **Investigate geographic concentration** and evaluate whether the strong concentration of revenue in leading states creates operational or expansion opportunities.

6. **Further investigate payment behavior** to understand the relationship between installment usage and order value before designing targeted payment strategies.

## Project Structure

```text
.
├── data/
│   └── raw/
├── notebooks/
│   ├── 01_data_profiling.ipynb
│   ├── 02_data_quality.ipynb
│   ├── 03_analysis_setup.ipynb
│   ├── 04_revenue_analysis.ipynb
│   ├── 05_customer_analysis.ipynb
│   ├── 06_delivery_analysis.ipynb
│   ├── 07_payment_analysis.ipynb
│   ├── 08_review_analysis.ipynb
│   ├── 09_seller_analysis.ipynb
│   ├── 10_product_analysis.ipynb
│   ├── 11_business_analysis.ipynb
│   ├── 12_business_recommendations.ipynb
│   └── 13_executive_summary.ipynb
├── .gitignore
├── README.md
└── requirements.txt
```

The notebooks are organized as a progressive analysis workflow, starting with data profiling and quality checks and ending with cross-analysis, business recommendations, and an executive summary.

## Tools & Technologies

- **Python** — Data analysis and processing
- **Pandas** — Data manipulation and analysis
- **NumPy** — Numerical computing
- **Matplotlib** — Data visualization
- **Jupyter Notebook** — Interactive analysis and documentation
- **Git / GitHub** — Version control and project management

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/aminhedayati/ecommerce-business-analytics.git
cd ecommerce-business-analytics
```

### 2. Create and activate a virtual environment

```bash
python -m venv .venv
```

On Windows:

```bash
.venv\Scripts\activate
```

On macOS/Linux:


```bash
source .venv/bin/activate
```

### 3. Install dependencies


```bash
pip install -r requirements.txt
```

### 4. Download the dataset

Download the Brazilian E-Commerce Public Dataset from Kaggle and place the extracted CSV files in:

```text
data/raw/
```

### 5. Run the notebooks

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Then open the notebooks in the notebooks/ directory and run them in numerical order, starting from 01_data_profiling.ipynb.

## Limitations

- The analysis is primarily descriptive and identifies associations rather than causal relationships.
- Some data quality issues and timestamp inconsistencies were identified in the source data and were retained as anomalies where there was not enough evidence to determine the correct values.
- The dataset represents historical marketplace activity and may not reflect current business conditions.
- Some findings are based on aggregated historical behavior and should be validated with additional operational or experimental analysis before making major business decisions.
