
# Investment Dashboard Power BI 📊

## Introduction
In today’s fast-paced financial world, understanding how investors allocate their funds across different avenues is crucial for portfolio optimization and strategic planning.  

Our **Investment Dashboard Power BI project** dives deep into investor preferences, offering clear insights into how funds are distributed among:  

- Mutual Funds  
- Equity Markets  
- Gold  
- Government Bonds  
- Fixed Deposits  
- PPF  

This interactive dashboard transforms raw financial data into actionable intelligence for analysts, advisors, and decision-makers.



---
## 🔹 Project Objectives 💡  
The main goals of this project are to uncover **patterns and trends in investment behavior**. Specifically, we aim to:  

1. **Visualize Investment Distribution** → Show the share of each investment avenue using treemaps.  
2. **Identify the Most Popular Investments** → Highlight top avenues by total preference score and investor count.  
3. **Track Investor Trends** → Monitor how preferences vary across demographics (e.g., gender, age) or over time.  
4. **Aggregate Total Preferences** → Calculate total preference scores across all investors.  
5. **Highlight Investor Count** → Display the number of unique investors engaged with different products.  

---

## 🔹 Data Preparation ⚙️  

### 1. Dataset Used  
- Table: `Finance_data`  
- Columns:  
  - **Demographics:** `gender`, `age`, `Source` (investment awareness source)  
  - **Investments:** `Mutual_Funds`, `Equity_Market`, `Debentures`, `Government_Bonds`, `Fixed_Deposits`, `PPF`, `Gold`  

### 2. Unpivoting Investment Columns  
To simplify analysis, investment columns were **unpivoted** in Power Query:  

- Original columns (`Mutual_Funds` → `Gold`) were transformed into:  
  - `InvestmentType` (categorical, e.g., Mutual_Funds, Gold)  
  - `PreferenceScore` (numeric, score/rank of preference)  

This conversion from wide format → long format made it possible to build dynamic, scalable visuals.  

### 3. Calculated Measures (DAX)  

**Total Preference Score**  
```DAX
TotalPreferenceScore =
SUMX (
    Finance_data,
    Finance_data[Mutual_Funds] +
    Finance_data[Equity_Market] +
    Finance_data[Debentures] +
    Finance_data[Government_Bonds] +
    Finance_data[Fixed_Deposits] +
    Finance_data[PPF] +
    Finance_data[Gold]
)



## Dashboard
The dashboard provides an **interactive view of financial behaviors**, making it easy to compare investment avenues, monitor popularity, and gain insights into portfolio allocation.

### Key Visuals 📈
- **Treemap:** Shows the share of each investment type with percentages and values.  
- **Bar Chart:** Ranks the most popular investment avenues.  
- **Card Visuals:** Display total preference score and total unique investors.  
- **Line Chart (Optional):** Shows trends in investment preferences over time, if time-series data is available.  

---

## Visualization Tools 🛠️
- **Tool Used:** Power BI Desktop  
- **Dataset Used:** Finance dataset with multiple investment columns per investor  
- **Visualizations Included:** Treemap, Bar Chart, Card Visual, Line Chart (optional), Data Labels with percentages  

---

## How It Works ⚙️
1. **Data Preparation:** The dataset is unpivoted in Power BI to convert multiple investment columns into a long-format table with `Attribute` (investment type) and `Value`.  
2. **Total Preference Calculation:** The total preference score is calculated using the sum of all investment values.  
3. **Unique Investors:** Total unique investors are calculated using `DISTINCTCOUNT(CustomerInfo)`.  
4. **Dynamic Visuals:** Treemap, bar chart, and line chart interactively update when filters or slicers are applied.  

---

## Conclusion 🏁
In a world driven by data, the **Investment Dashboard Power BI Project** empowers financial analysts, advisors, and decision-makers to explore investor behaviors with clarity.  

From understanding the most preferred investment avenues to tracking portfolio distribution, this project turns complex datasets into meaningful insights.  

With this dashboard, stakeholders can:  

- Make **data-driven investment decisions**  
- Optimize **portfolio strategies**  
- Understand **investor engagement patterns**  

---

## Contact & Collaboration 🤝
Feel free to reach out for any questions or suggestions about this project. I’m open to discussions and eager to assist.  

**LinkedIn:** [Your LinkedIn Link]  

---


⭐ Don’t forget to **follow and star** this repository if you find it valuable!
# 📊 Investment Dashboard in Power BI  

## 🔹 Introduction  
In today’s fast-paced financial world, understanding how investors allocate their funds across different avenues is essential for portfolio optimization and strategic planning.  

This **Power BI Investment Dashboard** explores investor preferences and behaviors, providing clear insights into how funds are distributed among:  

- Mutual Funds  
- Equity Markets  
- Gold  
- Government Bonds  
- Fixed Deposits  
- Public Provident Fund (PPF)  

By transforming raw financial data into meaningful visuals, this project delivers actionable intelligence for analysts, advisors, and decision-makers.  

---

