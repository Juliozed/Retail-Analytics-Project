# 🛒 Retail Analytics — Data Analysis Project

A comprehensive end-to-end data analysis project built on a retail dataset, covering data ingestion, storage, transformation, and interactive visualization.

---

## 📌 Project Overview

This project analyzes retail transaction data to uncover insights around sales performance, customer behavior, and product trends. The pipeline spans from raw data processing in Python to structured storage in PostgreSQL and dynamic dashboards in Power BI.

---

## 📂 Dataset

| Attribute     | Details                     |
|---------------|-----------------------------|
| **Source**    | Retail Analytics Dataset    |
| **Rows**      | 9,997                       |
| **Columns**   | 27                          |
| **Format**    | CSV                         |

The dataset captures key retail dimensions such as orders, customers, products, categories, regions, sales, discounts, and profitability metrics.

---

## 🛠️ Tech Stack

| Tool           | Purpose                                      |
|----------------|----------------------------------------------|
| **Python**     | Data cleaning, exploration, and preprocessing|
| **PostgreSQL** | Data storage and SQL-based analysis          |
| **Power BI**   | Interactive dashboards and visualization     |

---

## 📁 Project Structure

```
retail-analytics/
│
├── data/
│   ├── raw/                  # Original downloaded dataset
│   └── processed/            # Cleaned and transformed data
│
├── notebooks/
│   └── eda.ipynb             # Exploratory Data Analysis notebook
│
├── sql/
│   ├── schema.sql            # Table definitions
│   └── queries.sql           # Analytical SQL queries
│
├── powerbi/
│   └── retail_dashboard.pbix # Power BI report file
│
├── requirements.txt          # Python dependencies
└── README.md
```

---

## ⚙️ Workflow

### 1. Data Collection
Downloaded the retail analytics dataset (9,997 rows × 27 columns) and stored the raw CSV in the `data/raw/` directory.

### 2. Data Cleaning & EDA (Python)
- Handled missing values and duplicates
- Standardized data types and column formats
- Performed exploratory data analysis (distributions, correlations, outliers)
- Exported the cleaned dataset for database ingestion

### 3. Data Storage & Analysis (PostgreSQL)
- Designed a relational schema to store the retail data
- Wrote SQL queries to analyze sales trends, regional performance, product profitability, and customer segments

### 4. Visualization (Power BI)
- Connected Power BI directly to the PostgreSQL database
- Built interactive dashboards covering:
  - Sales & revenue trends over time
  - Top-performing products and categories
  - Regional sales breakdown
  - Discount impact on profit margins
  - Customer segment analysis

---

## 📊 Key Insights

- Identified top-performing product categories driving the highest revenue
- Revealed regions with consistently low profit margins despite high sales volume
- Quantified the negative impact of high discount rates on overall profitability
- Segmented customers by purchase behavior to inform targeting strategies

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- PostgreSQL 13+
- Power BI Desktop

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/retail-analytics.git
cd retail-analytics

# Install Python dependencies
pip install -r requirements.txt
```

### Database Setup

```bash
# Create the database
psql -U postgres -c "CREATE DATABASE retail_analytics;"

# Run the schema
psql -U postgres -d retail_analytics -f sql/schema.sql

# Load the data (from within Python or via COPY command)
psql -U postgres -d retail_analytics -f sql/load_data.sql
```

### Running the Notebook

```bash
jupyter notebook notebooks/eda.ipynb
```

### Power BI Dashboard
Open `powerbi/retail_dashboard.pbix` in Power BI Desktop and update the PostgreSQL connection string with your local credentials.

---

## 📦 Requirements

```
pandas
numpy
matplotlib
seaborn
sqlalchemy
psycopg2-binary
jupyter
```

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🙋 Author

**Your Name**
[GitHub](https://github.com/your-username) · [LinkedIn](https://linkedin.com/in/your-profile)
