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

The final product is a **visually rich analytics dashboard** that brings together financial, subscription, and client data in a cohesive layout using Python and Matplotlib/Seaborn. With a 2x2 grid layout, each chart is designed to surface key business insights clearly and efficiently.

### 🧩 What’s Included:

| Visualization | Chart Type | Insight |
|---------------|------------|---------|
| **Client Distribution - Finance Lending vs Blockchain** | Bar Chart | Compare client counts across Finance Lending and Blockchain sectors. |
| **Renewal Rates by Industry** | Heatmap | Identify industries with high or low renewal tendencies. Highlights the "Gaming" industry (if present). |
| **Inflation Rate During Renewals** | Histogram with KDE | Understand how inflation trends impact customer renewal periods. Includes an average line for clarity. |
| **Median Amount Paid per Year by Payment Method** | Line Plot | Spot trends in median annual payments across various payment methods. |

### ⚙️ Dashboard Features

**Grid layout (2x2)**: Clean organization using `matplotlib`'s `GridSpec`.
**Color-coded visuals**: Utilizes Seaborn’s `Set2` and `YlGnBu` palettes for aesthetic clarity.
**Annotations & Highlights**:
  Bar labels for easy comparison.
  Highlighted heatmap cell for the Gaming industry (if applicable).
  KDE overlay and vertical line to show average inflation rate.

### 🖥️ Built With

`Python`: Core logic and data processing.
`pandas`: Data wrangling and pivot tables.
`matplotlib` & `seaborn`: Charting and visual styling.
`Jupyter Notebook`: Development and visualization integration.

This dashboard serves as a powerful tool to derive insights from finance and subscription-related datasets. It offers a clear, structured layout that facilitates storytelling and informed decision-making—ideal for internal reviews, stakeholder presentations, or interactive app extensions.

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
