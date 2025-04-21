## 🌐 Finance & Subscription Analytics Dashboard

Welcome to the **Skygeni Analytics Project** — your one-stop interactive Python dashboard to dive deep into financial performance, subscription behaviors, and client insights! This notebook brings data to life through clean visuals and actionable metrics.

### 🧰 Libraries Used

| Library | Purpose |
|--------|---------|
| `pandas` | Data manipulation and preprocessing |
| `numpy` | Numerical operations |
| `matplotlib.pyplot` | Basic plotting framework |
| `seaborn` | Advanced and aesthetic statistical plotting |
| `%matplotlib inline` | Render plots directly inside the notebook |

## 📂 Data Sources

### 1. `financial_information.csv`  
📊 **Purpose:** Tracks macroeconomic indicators across financial quarters to assess external influences on client behaviors and renewals.

| Column Name | Description |
|-------------|-------------|
| `Unnamed: 0` | Auto-generated index column (can be safely dropped). |
| `start_date` | Beginning of the financial quarter. |
| `end_date` | End of the financial quarter. |
| `inflation_rate` | Inflation rate (%) during that time period. |
| `gdp_growth_rate` | GDP growth rate (%) for the same quarter. |

### 2. `industry_client_details.csv`  
🏢 **Purpose:** Provides contextual data to segment clients based on industry, size, and geography.

| Column Name | Description |
|-------------|-------------|
| `client_id` | Unique identifier for each client. |
| `company_size` | Size classification: Small, Medium, or Large. |
| `industry` | Industry sector (e.g., Finance Lending, Blockchain). |
| `location` | Geographic location of the company (e.g., Mumbai, Chennai). |

### 3. `payment_information.csv`  
💳 **Purpose:** Captures revenue streams, preferred payment modes, and transactional patterns.

| Column Name | Description |
|-------------|-------------|
| `client_id` | Foreign key linking to client details. |
| `payment_date` | Date when the payment was made. |
| `amount_paid` | Payment amount in currency units. |
| `payment_method` | Mode of payment (e.g., Bank Transfer, Check, etc.). |

### 4. `subscription_information.csv`  
🔁 **Purpose:** Tracks client subscription lifecycles, renewals, and plan types to measure churn and customer loyalty.

| Column Name | Description |
|-------------|-------------|
| `client_id` | Foreign key to connect with client and payment data. |
| `subscription_type` | Type of subscription (Monthly, Yearly). |
| `start_date` | Subscription start date. |
| `end_date` | Subscription end date. |
| `renewed` | Boolean indicating if the subscription was renewed (True/False). |

## 📊 Visualizations Breakdown

### 📍 1. How many Finance Lending and Blockchain clients does the organization have? — *Bar Chart*  
**Dataset:** `industry_client_details.csv`  
**Chart Type:** Vertical Bar Chart  
**Insight:**  
Shows the count of clients from **Finance Lending** and **Blockchain** industries.

#### ✅ Why a Bar Chart?
Simple and effective for comparing category counts.
Clear visual contrast between two industry types.
Helps assess which sector has more client representation.

### 🔥 2. Which industry in the organization has the highest renewal rate? — *Heatmap*  
**Dataset:** `subscription_information.csv` + `industry_client_details.csv` (merged via `client_id`)  
**Chart Type:** Heatmap  
**Insight:**  
Displays the **renewal rate** (percentage of subscriptions renewed) for each industry.

#### ✅ Why a Heatmap?
Great for **visualizing intensity or percentage-based data** across categories.
Instantly highlights the highest and lowest renewal rates with color gradients.
Excellent for pattern spotting across industries.

### 📉 3. What was the average inflation rate when subscriptions were renewed? — *Histogram*  
**Dataset:** `subscription_information.csv` + `financial_information.csv` (joined by date)  
**Chart Type:** Histogram  
**Insight:**  
Analyzes the **distribution of inflation rates** during periods when subscriptions were successfully renewed.

#### ✅ Why a Histogram?
Ideal for showing **distribution** of a continuous variable (inflation rate).
Reveals whether renewals occurred during high, low, or stable inflation periods.
Helps understand macroeconomic influence on renewals.

### 💰 4. What is the median amount paid each year for all payment methods? — *Bar & Line Combo Chart*  
**Dataset:** `payment_information.csv`  
**Chart Type:** Combo Chart (Bar for methods, Line for median amount)  
**Insight:**  
Shows **median annual payments** across different payment methods (e.g., Bank Transfer, Check).

#### ✅ Why a Combo Chart?
Combines both **categorical (payment method)** and **summary metric (median amount)**.
Bars give category-wise breakdown, line adds trend clarity.
Useful for highlighting financial behavior by payment type over time.

## 📊 Interactive Dashboard Overview

The final product is a **streamlined and insightful eDashboard** that brings together all key metrics and visualizations for quick and interactive exploration. It offers a consolidated view of client behavior, economic influence, financial performance, and subscription dynamics.

### 🧩 What’s Included:

| Visualization | Chart Type | Insight |
|---------------|------------|---------|
| **Client Distribution - Finance Lending vs Blockchain** | Bar Chart | Instantly compare how many clients come from Finance Lending vs Blockchain sectors. |
| **Renewal Rates by Industry** | Heatmap | Visually identify which industries have higher customer loyalty through renewal behavior. |
| **Inflation Rate During Renewals** | Histogram | Observe macroeconomic trends (like inflation) during times when clients renewed subscriptions. |
| **Median Amount Paid per Year by Payment Method** | Line Plot | Analyze how different payment methods contribute to the overall revenue and detect yearly patterns. |

### ⚙️ Dashboard Features

**Interactive filters**: Slice by year, industry, or payment method.
**Tooltips**: Hover over data points for exact values.
**Color-coded visuals**: Easily identify high vs low performance segments.
**Responsive layout**: Optimized for desktop and widescreen presentations.

### 🖥️ Built With

`Python`: Data wrangling with **pandas**, visualizations using **seaborn** and **matplotlib**.
`Jupyter Notebook`: For exploratory development and prototyping.
`Streamlit` or `Plotly Dash` (Optional): If made fully interactive as a web app.

This dashboard synthesizes insights from multiple datasets, providing a unified view of financial, subscription, and industry-related metrics, enabling quick analysis and decision-making. The layout is designed for clarity and interactivity, empowering users to explore data across different segments and make informed choices.
  
## 🚀 How to Run

1. Clone this repo or download the `.ipynb` file.
2. Ensure you have the required libraries installed:
   pip install pandas numpy matplotlib seaborn
3. Open the notebook in Jupyter:
   jupyter notebook SkygeniProject.ipynb
4. Run all cells and enjoy the insights!

## ❤️ Why This Project?

This dashboard was created to turn rows of numbers into powerful, easy-to-digest stories. It’s perfect for stakeholders, finance teams, and product strategists to:

Make informed decisions  
Visualize core financial and subscription metrics
Track subscription trends  
Evaluate discount strategies
