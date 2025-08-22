# Walmart Sales Forecasting with Prophet

## 📌 Project Overview
This project focuses on **time series forecasting and exploratory data analysis (EDA)** using Walmart's historical sales dataset. The dataset includes information about store sales, store details, promotional markdown events, fuel prices, temperature, CPI, unemployment rates, and holidays.  

The main objective is to **analyze patterns and forecast trends** in key economic factors (such as unemployment) and their potential impact on sales performance.  
We leverage **Facebook Prophet** to build a forecasting model that predicts future unemployment trends, which can serve as an important external factor in sales forecasting.

---

## 📂 Dataset Description
The project uses four datasets:

1. **features.csv** – Store-level features including:
   - `Temperature`, `Fuel_Price`
   - `MarkDown` (promotional discount indicators)
   - `CPI`, `Unemployment`
   - `IsHoliday` (holiday indicator)

2. **stores.csv** – Metadata about Walmart stores:
   - `Store ID`, `Type`, `Size`

3. **train.csv** – Historical weekly sales data:
   - `Store`, `Dept`, `Date`
   - `Weekly_Sales`, `IsHoliday`

4. **test.csv** – Test dataset for forecasting:
   - `Store`, `Dept`, `Date`, `IsHoliday`

---

## 🔎 Exploratory Data Analysis (EDA)
The EDA phase includes:
- **Barplots**: Comparing fuel prices during holiday vs non-holiday weeks.
- **Stripplots**: Analyzing temperature fluctuations across holidays.
- **Boxplots**: Exploring unemployment distribution during holidays vs non-holidays.

These visualizations help understand how external factors influence Walmart’s sales.

---

## 📈 Forecasting with Prophet
- We reformatted the dataset to fit Prophet’s requirements:
  - `Date` → `ds`
  - `Unemployment` → `y`
- Trained a **Prophet model** on unemployment rates.
- Generated forecasts for **365 future days**.
- Visualized results:
  - Forecast trend
  - Seasonal components
  - Changepoints (detected shifts in the trend)

---

## 📊 Key Visualizations
- **IsHoliday vs Fuel Price**  
- **IsHoliday vs Temperature**  
- **IsHoliday vs Unemployment**  
- **Prophet Forecast of Unemployment**  
- **Trend and Seasonal Components**  

---

## 🚀 Technologies Used
- **Python 3**
- **Pandas & NumPy** – Data processing
- **Seaborn & Matplotlib** – Data visualization
- **Prophet (Facebook/Meta)** – Time series forecasting

---

## 📌 Next Steps
- Expand forecasting to **Weekly_Sales** instead of only unemployment.  
- Incorporate **Markdown events and CPI** into the predictive model.  
- Build a **composite forecasting pipeline** for better accuracy.  
- Develop a dashboard for interactive visualization.

---

## 📜 License
This project is open-source and available under the MIT License.

---
👨‍💻 **Author**: *Your Name*  
📅 **Dataset Source**: [Kaggle - Walmart Sales Forecasting](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting)
