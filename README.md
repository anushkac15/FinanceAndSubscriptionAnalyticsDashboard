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

We’ve stitched together insights from four powerful CSV datasets:

1. `financial_information.csv` – Profit, sales, and cost metrics.
2. `industry_client_details.csv` – Regional, industry, and category information.
3. `payment_information.csv` – Details on client payment statuses.
4. `subscription_information.csv` – Plan types, renewal patterns, and pricing.

## 📊 Visualizations Breakdown

### 📍 1. Total Profit by Region — *Column Chart*
**Insight:** Which region brings in the most cash?

This vertical bar chart showcases the total profit from each region.
Great for comparing regional performance at a glance.

### 🧩 2. Total Count by Category — *Pie Chart*
**Insight:** What’s the distribution of clients by category?

A pie chart slices the total client distribution by category.
Helps understand which market segments dominate.

### 📦 3. Total Profit by Sub-Category — *Bar Chart*
**Insight:** Which sub-products or services are cash cows?

Horizontal bars showing profit per sub-category.
Useful for zooming into granular performance.

### 📈 4. Profit & Sales by Discount — *Combo Chart (Line + Bar)*
**Insight:** Is discounting helping or hurting profits?

Line graph for profits, bar chart for sales — all plotted against varying discount rates.
Reveals trade-offs and tipping points.

### 🌳 5. Total Profit by Sub-Category — *Treemap*
**Insight:** A visual jungle of profits!

Block size reflects profit magnitude.
Easy to spot top performers at a glance.

### 🌱 6. Total Sales by Sub-Category — *Treemap*
**Insight:** Where is the volume?

Similar treemap focusing on total sales.
Reveals demand hotspots.

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
**Visualize core financial and subscription metrics**  
Track subscription trends  
Evaluate discount strategies
