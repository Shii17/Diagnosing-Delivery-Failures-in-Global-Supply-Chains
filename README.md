# 🚚 Diagnosing Delivery Failures in Global Supply Chains

> An end-to-end supply chain analysis uncovering why orders arrive late and what it costs the business. Covers EDA, root cause analysis by region and shipping mode, and a Random Forest model predicting late delivery risk.

---

## 📌 Table of Contents
- [Business Problem](#business-problem)
- [Key Findings](#key-findings)
- [Project Workflow](#project-workflow)
- [Tech Stack](#tech-stack)
- [ML Model](#ml-model)
- [Project Structure](#project-structure)
- [How to Run](#how-to-run)
- [Dataset](#dataset)

---

## 🧩 Business Problem

Late deliveries are one of the most costly and visible failures in supply chain operations — they erode customer trust, inflate operational costs, and quietly drain profit margins. This project investigates **180,000+ orders** from a global e-commerce supply chain to answer:

- How widespread is the late delivery problem?
- Which regions, shipping modes, and customer segments are most affected?
- Can we predict which orders are at risk *before* they ship?

---

## 💡 Key Findings

- **~54% of all orders** were delivered late, making delays the norm rather than the exception
- **First Class** and **Same Day** shipping modes had disproportionately high delay rates despite being premium options
- **Central America** and **Western Europe** emerged as the highest-delay regions
- Orders placed on **certain days of the week and hours** showed measurably higher delay rates — suggesting operational bottlenecks
- Delayed orders were strongly correlated with **profit loss**, confirming the direct financial impact of delivery failures

---

## 🔄 Project Workflow

```
Raw Data → Data Cleaning → Feature Engineering → EDA → Root Cause Analysis → ML Modeling
```

1. **Data Cleaning** — Removed redundant, PII, and single-value columns; excluded cancelled orders; parsed date fields
2. **Feature Engineering** — Derived delay metrics, profitability flags, and time-based order features
3. **Exploratory Data Analysis** — Profitability distribution, delay distributions, business KPIs
4. **Root Cause Analysis** — Delay % broken down by region, shipping mode, customer segment, department, and order status
5. **Time-Based Analysis** — Delay trends across month, day of week, and hour of day
6. **ML Modeling** — Random Forest classifier with SMOTE balancing to predict late delivery risk

---

## 🛠 Tech Stack

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?logo=scikit-learn)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C)
![Imbalanced-learn](https://img.shields.io/badge/Imbalanced--learn-SMOTE-green)

---

## 🤖 ML Model

| Detail | Value |
|---|---|
| Model | Random Forest Classifier |
| Target | `Late_delivery_risk` |
| Encoding | Frequency Encoding |
| Class Balancing | SMOTE |
| Train/Test Split | 80/20 |

**Features used:** Shipping Mode, Days for Shipment (Scheduled), Customer Segment, Department Name, Order Region, Order Type, Category Name, Order Month, Order Hour

---

## 📁 Project Structure

```
├── Supply_Chain_Analysis.ipynb   # Main analysis notebook
├── requirements.txt              # Python dependencies
├── images/                       # Chart exports for README
└── README.md
```

---

## ▶️ How to Run

1. Clone the repository
   ```bash
   git clone https://github.com/your-username/supply-chain-delivery-diagnostics.git
   cd supply-chain-delivery-diagnostics
   ```

2. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```

3. Download the dataset from Kaggle (link below) and place it in the project folder

4. Open and run the notebook
   ```bash
   jupyter notebook Supply_Chain_Analysis.ipynb
   ```

---

## 📦 Dataset

**DataCo Supply Chain Dataset** — publicly available on Kaggle

🔗 [Download here](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis)

> The dataset contains 180,519 orders with 53 features covering customer info, order details, shipping, and delivery status across global regions.

---

## 👩‍💻 Author

**Shivani Prasad**  
📎[LinkedIn](https://linkedin.com/in/shivani-prasad-48b48b272)  • 🐙 [GitHub](https://github.com/Shii17)

---

*If you found this project useful, consider giving it a ⭐*
