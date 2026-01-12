# TATA Data Visualisation: Empowering Business with Effective Insights
## Forage Job Simulation - Tableau Analytics Project

This repository contains the Tableau dashboards and analysis created for the **Tata Data Visualisation: Empowering Business with Effective Insights** virtual job simulation on Forage.

---

## 📋 Project Overview

This project simulates working as a data analyst supporting **C-level executives** (CEO and CMO) of an online retail business with data-driven insights for:
- Revenue forecasting and seasonal planning
- Market expansion strategy
- Customer retention and segmentation

**Deliverables:**
- 4 interactive Tableau dashboards answering executive questions
- Data cleaning and validation process
- Business recommendations and actionable insights

---

## 🧹 Data Cleaning & Methodology

### Raw Data
- **Original dataset:** 500,000+ transactions
- **Data quality issues identified:**
  - Negative quantities (store returns)
  - Invalid unit prices (data entry errors)
  - Missing CustomerID values

### Cleaning Steps Applied

| Check | Rule | Impact |
|-------|------|--------|
| **Quantity Validation** | Quantity ≥ 1 unit only | Removed all returns |
| **Price Validation** | Unit Price > $0 | Removed ~8% corrupted records |
| **Customer Identification** | Exclude missing CustomerID | Ensured customer-level accuracy |

### Final Dataset
- **Cleaned records:** ~40,000 transactions
- **Data completeness:** ~95%
- **Calculated field:** Revenue = Quantity × Unit Price

---

## 📊 Tableau Dashboards

### Dashboard 1: Monthly Revenue Trend (2011)

**Stakeholder:** CEO  
**Business Question:** What seasonal revenue patterns exist in 2011 for forecasting purposes?

**Visual Type:** Line Chart
- **X-axis:** Invoice Date (Monthly granularity, 2011 only)
- **Y-axis:** Revenue (Calculated: Quantity × Unit Price)

**Key Findings:**
- 📈 **Peak Season:** September → November (~1,162K revenue in November)
- 📉 **Seasonal Drop:** Slight December decline despite holiday season
- 🎯 **Critical Window:** 3-month peak (Sept-Nov) for inventory & marketing planning

**Business Insights:**
- Holiday shopping season drives 40%+ of Q4 revenue
- November peak followed by December dip suggests early customer stocking behavior
- **Recommendation:** Plan supply chain and marketing budgets backward from September-November window for 2012 forecasting

---

### Dashboard 2: Top 10 Countries by Revenue (Excluding UK)

**Stakeholder:** CMO  
**Business Question:** Which countries generate highest revenue and what is the revenue-to-volume relationship?

**Visual Type:** Side-by-Side Bar Chart
- **Categories:** Top 10 Countries (excluding United Kingdom)
- **Measures:** Revenue (Bar 1) | Quantity Sold (Bar 2)
- **Sort:** Descending by Revenue

**Top Performers:**
| Rank | Country | Revenue | Quantity |
|------|---------|---------|----------|
| 1 | Netherlands | 🥇 | ~200K units |
| 2 | EIRE | 🥈 | ~150K units |
| 3 | Germany | 🥉 | ~120K units |
| 4 | France | — | ~110K units |
| 5 | Australia | — | ~80K units |

**Key Insights:**
- ✅ Strong **volume + value correlation** in top 5 markets
- ✅ Healthy order sizes indicate market maturity
- ✅ Stable purchasing behavior = lower expansion risk

**Business Recommendations:**
- **Priority Expansion Targets:** Netherlands, EIRE, Germany, France
- **Strategy:** Aggressive campaigns & faster go-to-market execution
- **Rationale:** These markets have proven online retail viability

---

### Dashboard 3: Top 10 Customers by Revenue

**Stakeholder:** CMO  
**Business Question:** Who are our highest-value customers and how concentrated is revenue?

**Visual Type:** Vertical Bar Chart (Sorted Descending)
- **Dimension:** CustomerID (Top 10 by total revenue)
- **Measure:** Revenue
- **Filter:** Excluded records with missing CustomerID

**Revenue Concentration Insight:**
- 👥 **Top 10 customers** = ~8-10% of total revenue
- 📊 **Customer base size** = Top 10 represent only ~0.3% of all customers
- ⚠️ **Risk Level:** High revenue concentration = churn risk

**Top Customer IDs:**
14646 | 18102 | 17450 | 16446 | 14911 | [+ 5 more]

**Customer Behavior Pattern:**
- These aren't one-time buyers
- They are **repeat purchasers** with strong loyalty
- High lifetime value indicates product satisfaction

**Business Recommendations:**
- 🎯 **VIP Treatment:** White-glove customer service for top 10
- 🎁 **Loyalty Programs:** Early product access, exclusive deals
- 📞 **Priority Support:** Dedicated account management
- 📊 **Churn Prevention:** Monitor these accounts closely; retention ROI is extremely high

---

### Dashboard 4: Global Demand Map (Excluding UK)

**Stakeholder:** CEO  
**Business Question:** Which regions show highest demand for expansion opportunities?

**Visual Type:** Filled Geographic Map / Symbol Map
- **Geography:** Country-level
- **Metric:** Total Quantity Sold
- **Filter:** United Kingdom excluded
- **Labels:** Country names and quantity visible on map

**Demand Zones - Strategic Breakdown:**

**🟢 HIGH-DEMAND ZONES (Aggressive Expansion)**
- Western Europe Cluster:
  - **Netherlands:** ~200K units
  - **EIRE:** ~150K units
  - **Germany:** ~120K units
  - **France:** ~110K units
- **Asia-Pacific Leader:**
  - **Australia:** ~80K units (untapped potential)

**🟡 SECONDARY DEMAND (Opportunistic Growth)**
- Spain, Sweden, Belgium, Switzerland, Japan show moderate but consistent demand

**🔴 WEAK/EMERGING MARKETS (Pilot Testing)**
- Brazil, Czech Republic, Saudi Arabia (~80-356 units)
- Minimal online retail traction
- Require different go-to-market approaches

**Geographic Insight:**
- Online retail penetration already proven in Western Europe & Australia
- Customer behavior & payment infrastructure established = lower risk
- Expansion opportunity exists in weaker markets but requires validation first

**Business Recommendations - Two-Pronged Strategy:**

1. **AGGRESSIVE EXPANSION (2012)**
   - Target: Germany, Netherlands, EIRE
   - Action: Maximize marketing spend, optimize inventory, establish local partnerships
   - Expected ROI: High (proven markets)

2. **EXPLORATORY TESTING (2012)**
   - Target: USA, Saudi Arabia, Brazil, Eastern Europe
   - Action: Run pilot programs before full investment
   - Goal: Validate if online retail model works in these regions
   - Expected ROI: Moderate-to-High (depends on pilot success)

---

## 📁 Repository Structure

```
tata-data-visualisation/
├── README.md                                    # This file
├── Tata_Forage_Online_Retail.twbx              # Tableau workbook (all dashboards)
├── Tata_Forage_Executive_Presentation.pdf      # PowerPoint/PDF presentation
└── data/
    └── cleaned_retail_data_methodology.txt     # Data cleaning notes
```

---

## 🚀 How to View the Dashboards

### Option 1: Tableau Desktop/Public (Recommended)
1. Download `Tata_Forage_Online_Retail.twbx`
2. Open with **Tableau Desktop** or **Tableau Public** (free)
3. Navigate through dashboard tabs:
   - `Q1_Monthly_Revenue_2011`
   - `Q2_Top_Countries_No_UK`
   - `Q3_Top_Customers`
   - `Q4_Global_Demand_Map`

### Option 2: Tableau Server (If Published)
- Access the hosted dashboards at: `[Your Tableau Server URL]`

---

## 💡 Key Skills Demonstrated

✅ **Data Cleaning & Validation**
- Conditional formula logic for data quality checks
- Handling missing values and data entry errors
- Calculating derived metrics (Revenue field)

✅ **Tableau Dashboard Development**
- Time series analysis (line charts)
- Comparative analysis (side-by-side bars)
- Ranking & segmentation (vertical bars)
- Geographic visualization (maps)

✅ **Executive Communication**
- Translating data into business recommendations
- Connecting insights to strategic decisions
- Framing recommendations for C-suite stakeholders

✅ **Business Analytics**
- Seasonal trend analysis & forecasting
- Market opportunity identification
- Customer concentration & risk analysis
- Revenue-volume correlation analysis

---

## 📈 Key Takeaways & Recommendations

| Question | Insight | Action |
|----------|---------|--------|
| **Q1: Revenue Trends** | 3-month peak (Sep-Nov) drives 40% of revenue | Plan inventory & marketing backward from peak season |
| **Q2: Market Opportunity** | Top 5 countries have proven online retail fit | Invest aggressively in established markets |
| **Q3: Customer Concentration** | Top 10 = 10% revenue, 0.3% customers | Implement VIP retention programs immediately |
| **Q4: Expansion Strategy** | Europe strong; emerging markets need pilots | Dual approach: Scale proven + test new markets |

---

## 📚 Resources Used

- **Data Source:** Forage TATA Job Simulation
- **Tool:** Tableau (Desktop / Public)
- **Data Period:** 2011 (with multi-year dataset available)
- **Business Context:** Online Retail Industry

---

## 🤝 Contributing

This is a portfolio project completed as part of the Forage virtual internship. 

For questions or feedback, please feel free to open an issue or contact me directly.

---

## 📄 License

This project is created for educational and portfolio purposes as part of the Forage TATA Data Visualisation Job Simulation.

---

## ✨ Next Steps for Your GitHub

1. **Create a new GitHub repository** with the name: `tata-data-visualisation` (or similar)
2. **Upload these files:**
   - This `README.md`
   - Your `Tata_Forage_Online_Retail.twbx` file
   - Your presentation PDF
   - Any data cleaning scripts (if applicable)

3. **Add these optional sections** if you want to enhance the repo:
   - Screenshots of each dashboard (as PNG images in `/screenshots`)
   - Data dictionary explaining each field
   - SQL or Python scripts used for data cleaning
   - Blog post about your approach

4. **Customize the README** with:
   - Your actual file names
   - Links to your Tableau Public profile (if you publish there)
   - Your LinkedIn profile for networking

5. **Make it discoverable:**
   - Add relevant topics/tags: `tableau`, `data-visualization`, `business-analytics`, `forage`
   - Write a compelling description in repository settings



