# 🚚 Delivery Delay Analysis

> An end-to-end data analytics project that investigates delivery performance and delay patterns using **SQL, Excel, Python (Jupyter) and Power BI** — from raw data to actionable business insights.

---

## 📑 Table of Contents

1. [Project Overview](#-project-overview)
2. [Business Problem](#-business-problem)
3. [Objectives](#-objectives)
4. [Repository Structure](#-repository-structure)
5. [Tech Stack](#-tech-stack)
6. [Dataset Description](#-dataset-description)
7. [Methodology](#-methodology)
8. [Key Analyses Performed](#-key-analyses-performed)
9. [Key Insights & Findings](#-key-insights--findings)
10. [Dashboard Preview](#-dashboard-preview)
11. [Recommendations](#-recommendations)
12. [How to Run This Project](#-how-to-run-this-project)
13. [Skills Demonstrated](#-skills-demonstrated)
14. [Future Enhancements](#-future-enhancements)
15. [Author](#-author)
16. [License](#-license)

---

## 📌 Project Overview

Timely delivery is one of the most important drivers of customer satisfaction and operational efficiency in logistics, e-commerce and supply-chain businesses. Late deliveries increase costs, damage brand trust and drive customer churn.

This project performs a **complete delivery delay analysis**. It covers the full analytics lifecycle:

- Collecting and organising **raw delivery data**
- **Cleaning and transforming** the data for reliability
- Running **SQL queries** for business-level aggregation
- Performing **exploratory data analysis (EDA)** in Python
- Building **Excel summaries** for quick reporting
- Designing an **interactive Power BI dashboard** for stakeholders

---

## 🎯 Business Problem

A logistics/delivery business needs to understand:

- **How often** are deliveries delayed?
- **Where and when** do delays occur most?
- **What factors** (region, carrier, distance, order type, time period, etc.) contribute to delays?
- **What actions** can reduce delays and improve on-time delivery rates?

Without clear answers, the business cannot optimise routes, allocate resources or set realistic delivery promises to customers.

---

## 🧭 Objectives

- Clean and standardise the raw delivery dataset
- Calculate core KPIs such as **On-Time Delivery Rate**, **Delay Rate** and **Average Delay Duration**
- Identify **patterns and root causes** behind delivery delays
- Segment performance by relevant dimensions (time, location, category, etc.)
- Present findings through an **interactive dashboard**
- Provide **data-driven recommendations** to improve delivery performance

---

## 📂 Repository Structure

```
Delivery-Analysis/
│
├── Raw Data/                        # Original, unmodified source data
├── Cleaned Data/                    # Processed, analysis-ready datasets
├── SQL File/                        # SQL scripts for querying & aggregation
├── Excel File/                      # Excel workbooks / pivot summaries
├── Power Bi/                        # Power BI report (.pbix) & dashboard files
├── Image/                           # Dashboard screenshots & charts
│
├── Delivery Delay Analysis.ipynb    # Python notebook: cleaning, EDA & visualisation
└── README.md                        # Project documentation
```

| Folder / File | Purpose |
|---|---|
| **Raw Data** | Untouched source files, kept for reproducibility |
| **Cleaned Data** | Output of the cleaning pipeline; feeds SQL, Excel and Power BI |
| **SQL File** | Queries used to compute KPIs and business metrics |
| **Excel File** | Pivot tables, summaries and quick-reference reports |
| **Power Bi** | Interactive dashboard (`.pbix`) |
| **Image** | Screenshots of visuals and dashboards used in documentation |
| **Delivery Delay Analysis.ipynb** | Main analysis notebook (data cleaning → EDA → insights) |

---

## 🛠 Tech Stack

| Category | Tools |
|---|---|
| **Programming** | Python (Pandas, NumPy) |
| **Visualisation** | Matplotlib, Seaborn, Power BI |
| **Database / Querying** | SQL |
| **Spreadsheet Analysis** | Microsoft Excel (Pivot Tables, formulas) |
| **Environment** | Jupyter Notebook |
| **Version Control** | Git & GitHub |

---

## 🗃 Dataset Description

> 📝 *Update this section with the exact schema of your dataset.*

The dataset contains delivery-level records. Typical fields include:

| Column | Description |
|---|---|
| `Order ID` | Unique identifier for each order/delivery |
| `Order Date` | Date the order was placed |
| `Promised / Expected Delivery Date` | Delivery date committed to the customer |
| `Actual Delivery Date` | Date the delivery was completed |
| `Delivery Status` | On-time / Delayed |
| `Region / City` | Delivery location |
| `Carrier / Partner` | Logistics provider handling the delivery |
| `Category` | Product or order category |
| `Delay (Days)` | Difference between actual and expected delivery dates |

**Derived fields created during analysis:**

- `Delay_Days` = Actual Delivery Date − Expected Delivery Date
- `Is_Delayed` = Boolean flag for late deliveries
- Date parts (month, weekday, quarter) for time-based trend analysis

---

## 🔬 Methodology

```
Raw Data → Data Cleaning → Feature Engineering → SQL Analysis → EDA (Python) → Excel Summary → Power BI Dashboard → Insights
```

### 1. Data Cleaning
- Handled **missing values** and **duplicate records**
- Corrected **data types** (especially dates)
- Standardised **text fields** and category labels
- Removed or flagged **outliers and invalid entries**

### 2. Feature Engineering
- Calculated delay duration and delay flags
- Extracted month, weekday and quarter for temporal analysis
- Created delay buckets (e.g. on-time, minor delay, major delay)

### 3. SQL Analysis
- Aggregated KPIs by region, carrier, category and time period
- Ranked best and worst performing segments
- Computed delay rates using grouping and conditional aggregation

### 4. Exploratory Data Analysis (Python)
- Distribution analysis of delay durations
- Trend analysis over time
- Segment-wise comparison and correlation checks
- Visualisations to surface patterns quickly

### 5. Excel Reporting
- Pivot tables for quick slicing
- Summary tables for non-technical stakeholders

### 6. Power BI Dashboard
- KPI cards, trend charts, geographic and categorical breakdowns
- Interactive slicers and filters for self-service exploration

---

## 📊 Key Analyses Performed

- ✅ Overall **on-time vs delayed** delivery split
- ✅ **Average and maximum delay** duration
- ✅ **Monthly / weekly trends** in delivery performance
- ✅ **Regional performance** comparison
- ✅ **Carrier / partner** performance comparison
- ✅ **Category-wise** delay analysis
- ✅ Identification of **high-risk segments**

---

## 💡 Key Insights & Findings

> 📝 *Replace the placeholders below with the real numbers from your analysis. Specific, quantified findings are what make a README stand out.*

- **Overall delay rate:** `XX%` of deliveries were delivered late
- **Average delay:** `X.X days` among delayed orders
- **Worst-performing region:** `<Region>` with a delay rate of `XX%`
- **Best-performing carrier:** `<Carrier>` with an on-time rate of `XX%`
- **Peak delay period:** `<Month / Weekday>` shows the highest delay concentration
- **Highest-risk category:** `<Category>` contributes the most delayed orders

---

## 🖥 Dashboard Preview

> 📝 *Add your screenshots from the `Image/` folder. Example below.*

```markdown
![Dashboard Overview](Image/dashboard_overview.png)
```

**Dashboard highlights:**
- KPI cards: Total Orders, On-Time %, Delay %, Avg. Delay Days
- Time-series trend of delays
- Region and carrier comparisons
- Interactive filters (date, region, category, carrier)

---

## ✅ Recommendations

Based on the analysis, the business can:

1. **Focus on high-delay regions** by adding local hubs or improving route planning
2. **Review underperforming carriers** and renegotiate SLAs or reallocate volume
3. **Plan capacity for peak periods** where delays spike
4. **Set realistic delivery promises** for high-risk categories
5. **Monitor KPIs continuously** using the Power BI dashboard for early warning

---

## ▶️ How to Run This Project

### Prerequisites
- Python 3.9+
- Jupyter Notebook / JupyterLab
- Power BI Desktop (to open the `.pbix` file)
- Any SQL client (MySQL / PostgreSQL / SQL Server)
- Microsoft Excel

### Steps

```bash
# 1. Clone the repository
git clone https://github.com/TrivediMan/Delivery-Analysis.git
cd Delivery-Analysis

# 2. (Optional) create a virtual environment
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

# 3. Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# 4. Launch the notebook
jupyter notebook "Delivery Delay Analysis.ipynb"
```

**Then:**
- Run the notebook cells top to bottom to reproduce cleaning and EDA
- Import files from `Cleaned Data/` into your SQL database and run scripts from `SQL File/`
- Open the `.pbix` file in `Power Bi/` with Power BI Desktop to explore the dashboard
- Open files in `Excel File/` for pivot-based summaries

---

## 🎓 Skills Demonstrated

- Data cleaning & preprocessing
- Feature engineering
- SQL querying & aggregation
- Exploratory data analysis
- Data visualisation & dashboard design
- KPI definition & business storytelling
- Excel pivot reporting
- End-to-end analytics workflow

---

## 🚀 Future Enhancements

- Add **predictive modelling** to forecast delivery delays (e.g. logistic regression, random forest)
- Integrate **external factors** such as weather, traffic and holidays
- Automate the pipeline with **scheduled data refresh**
- Build a **real-time dashboard** connected to a live database
- Perform **root-cause analysis** with additional operational data

---

## 👤 Author

**Man Trivedi**
**11244**
GitHub: [@TrivediMan](https://github.com/TrivediMan)

> *Feel free to connect, share feedback, or open an issue. If you found this project useful, please consider giving it a ⭐*

---

## 📄 License

This project is open for learning and portfolio purposes. Add a license of your choice (e.g. [MIT](https://choosealicense.com/licenses/mit/)) if you plan to allow reuse.
