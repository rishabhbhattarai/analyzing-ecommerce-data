
---

## 🛒 Analyzing eCommerce Data in Tableau

### 📊 Project Overview

This project explores sales data from **Munchy’s Pet Supply**, a fictitious U.S.-based pet-supply retailer. The goal is to analyze eCommerce data, model relationships between datasets, and design an **executive dashboard** in Tableau that highlights sales performance and shipping optimization opportunities.

The project demonstrates real-world data analytics workflow — including **data modeling, cleanup, metric creation, and interactive visualization** — to extract actionable insights that drive smarter business decisions.

---

### 🎯 Objectives

**Primary Goal:**
Build an executive dashboard to analyze eCommerce sales performance.

**Secondary Goal:**
Develop a **what-if analysis** to optimize shipping costs and identify potential savings.

---

### 🐶 About Munchy’s Pet Supply

* **Products:** Pet food, supplements, cleaning, and grooming supplies
* **Target Market:** Pet owners across the U.S.
* **Business Goals:** Increase sales and reduce shipping costs

---

### 🧩 The Dataset

The dataset consists of **four CSV files**, each serving a specific function in the data model.

#### **1. Sales Table**

| Column           | Description                                              |
| ---------------- | -------------------------------------------------------- |
| Transaction Date | Date of purchase                                         |
| Customer ID      | Unique identifier for each customer                      |
| Description      | Product name                                             |
| Stock Code       | Product code                                             |
| Invoice No       | Identifier for each sale (can include multiple products) |
| Quantity         | Units purchased                                          |
| Sales            | Total sales amount                                       |
| Unit Price       | Price per unit                                           |

#### **2. State Mapping Table**

| Column      | Description                            |
| ----------- | -------------------------------------- |
| Order State | Original state name/variation          |
| State       | Standardized state name                |
| Region      | Region of the U.S. (e.g., West, South) |

#### **3. Product Table**

| Column             | Description                                    |
| ------------------ | ---------------------------------------------- |
| Stock Code         | Product identifier                             |
| Weight             | Product weight per unit                        |
| Landed Cost        | Cost of goods sold + freight to U.S. warehouse |
| Shipping_Cost_1000 | Average cost of shipping 1000 miles            |
| Description        | Product name                                   |
| Category           | Product category (e.g., Pet Food, Accessories) |

#### **4. Customer Table**

| Column               | Description                   |
| -------------------- | ----------------------------- |
| Customer ID          | Unique customer identifier    |
| Order City           | City of purchase              |
| Order Postal         | Postal code                   |
| Order State          | Customer’s U.S. state         |
| Latitude / Longitude | Customer location coordinates |

---

### 🚚 Shipping Costs & What-If Analysis

#### **Shipping Costs 101**

* Baseline assumption:
  Each additional quantity in a shipment costs ~**70%** of the cost of shipping that product individually.
* Example:
  Shipping 1 jar = 10, Shipping 9 jars = 45, total (5 per jar average).

#### **What-If Analysis**

* Explore the effect of bulk purchases on shipping costs.
* Use parameters to test alternative quantity or distance assumptions.
* Visualize cost differences using area and lollipop charts.

---

### 🧮 Project Workflow

1. **Data Modeling**

   * Join `Sales`, `Products`, `Customers`, and `State Mapping` tables.
   * Ensure referential consistency across keys.

2. **Data Cleanup**

   * Remove null invoices and invalid transactions via data source filters.
   * Standardize state and region fields using the mapping table.

3. **Metric Creation**

   * Build custom measures:

     * `Profit %`
     * `Shipping (Baseline)`
     * `Shipping (What-if)`
     * `Shipping (Difference)`

4. **Executive Dashboard**

   * **BANS**: Sales, Profit, Profit %, Shipping (baseline)
   * **Views**: Top Sellers, Sales by State, Regional Performance

5. **What-If Dashboard**

   * **BANS**: Shipping Baseline, What-if, Difference
   * **Charts**: What-if Area Chart, Shipping Cost Lollipop Chart
   * Use parameter controls for scenario adjustments.

---

### 💡 Key Insights

* **Top Sellers:** Pet food and disposable products dominate total sales.
* **Most Profitable:** Electronics (e.g., pet cameras) yield the highest profit margins.
* **Customer Distribution:** Major clusters in **California, Florida, and Texas**, making them prime marketing targets.
* **Shipping Optimization:**
  Incentivizing customers to purchase higher quantities can reduce per-unit shipping costs and boost profitability.

---

### 📈 Tableau Dashboard

Interactive dashboards are published on Tableau Public:

🔗 [Executive Dashboard](#)
🔗 [Shipping Cost What-If Analysis](#)

*(Replace “#” with your actual Tableau Public URLs)*

---

### 🛠️ Tools Used

* **Tableau Desktop** – for data visualization and dashboard design
* **Excel / CSV files** – for data storage and transformation
* **Data Modeling & Parameters** – for building calculated fields and what-if scenarios


---