# Amazon Sales Dashboard — Tableau

An interactive sales analytics dashboard built using **Tableau Public**, visualising Amazon India order data across products, categories, shipping status, geography, and time.

---

## Dashboard Preview

> Open the `.twbx` file in Tableau Desktop or view it live on Tableau Public.

---

## Key Metrics at a Glance

| Metric | Value |
|---|---|
| Currency | INR |
| Total Quantity Sold | 1,16,649 |
| Total Revenue | ₹7,85,92,678 |
| Total Categories | 9 |
| Total Products | 7,190 |
| Total Size Variants | 11 |

---

## Dashboard Visuals

The dashboard is built across **two pages** — Dashboard 1 and Dashboard 2 — with an interactive **Category filter** at the top that updates all charts simultaneously.

### 1. Quantity by Week and Category
A stacked bar chart showing weekly order quantity broken down by product category (March 2022 – June 2022). Helps identify which categories drive the most volume week by week and spot seasonal demand spikes.

### 2. Quantity by Courier Status and Category
A donut chart breaking down orders by fulfilment status:
- **Shipped** — 94.21%
- **Unshipped** — 5.79%
- **Cancelled** — 0.00%

Gives a quick view of overall delivery health and fulfilment efficiency.

### 3. Quantity by Sales Channel and Category
A highlight table comparing two sales channels:
- **Amazon.in** — 99.86%
- **Non-Amazon** — 0.14%

Also shows **B2B vs B2C split**:
- B2C (False) — 99.28%
- B2B (True) — 0.72%

### 4. Amount by Week and Category
A multi-line time series chart tracking weekly revenue (₹) per category from March to June 2022. Useful for identifying revenue peaks, category-level trends, and comparing performance over time. Hovering on a data point reveals the exact Category, Week, and Amount (e.g., Set category peaked at ₹26,73,684 on May 29, 2022).

### 5. Quantity by Status and Category
A horizontal bar chart listing all order fulfilment statuses and their quantities:

| Status | Quantity |
|---|---|
| Shipped | 62,459 |
| Shipped – Delivered to Buyer | 22,671 |
| Cancelled | 4,545 |
| Shipped – Returned to Seller | 1,404 |
| Shipped – Picked Up | 688 |
| Pending | 511 |
| Pending – Waiting for Pick Up | 218 |
| Shipped – Returning to Seller | 105 |
| Shipped – Out for Delivery | 25 |
| Shipped – Rejected by Buyer | 9 |
| Shipping | 8 |
| Shipped – Lost in Transit | 4 |
| Shipped – Damaged | 1 |

### 6. Top 10 States by Quantity and Category — Ship Service Level
A grouped bar chart ranking the top 10 Indian states by order volume, split by **Expedited** vs **Standard** shipping. Top performing states:

| State | Expedited | Standard |
|---|---|---|
| Maharashtra | 14,790 | 5,538 |
| Karnataka | 11,747 | 4,154 |
| Tamil Nadu | 7,612 | 2,800 |
| Telangana | 7,469 | 2,784 |
| Uttar Pradesh | 6,563 | 2,936 |
| Delhi | 4,376 | — |
| Kerala | 3,904 | — |
| West Bengal | 3,853 | — |
| Andhra Pradesh | 3,425 | — |
| Gujarat | 2,744 | — |

### 7. Map — Quantity by State
An interactive choropleth map of India shading each state by total order quantity. Darker shades indicate higher order volumes. Maharashtra, Karnataka, and Tamil Nadu are the highest-density regions.

### 8. Quantity by Size and Category
A stacked bar chart showing order quantities across clothing size variants (XS, S, M, L, XL, XXL, 3XL, 4XL, 5XL, 6XL, Free) for each product category. Key insight: M, L, and XL sizes consistently see the highest demand across all categories.

---

## Dataset

The dataset contains Amazon India sales order records covering the period **March 2022 to June 2022**.

Key fields used in the dashboard:

| Field | Description |
|---|---|
| Order Date | Week-level date of the order |
| Category | Product category (Set, Kurta, Western Dress, etc.) |
| Size | Size variant of the product |
| Qty | Number of units ordered |
| Amount | Order value in INR |
| Status | Fulfilment/shipping status |
| Courier Status | Courier-level delivery status |
| Sales Channel | Amazon.in or Non-Amazon |
| B2B | Whether the order is a business-to-business sale |
| Ship Service Level | Expedited or Standard shipping |
| Ship State | Indian state of the delivery address |

---

## Tools and Technologies

| Tool | Purpose |
|---|---|
| Tableau Public / Desktop | Dashboard design and visualisation |
| Tableau Calculated Fields | KPI tiles (Total Quantity, Total Amount, etc.) |
| Tableau Filters | Interactive Category filter applied across all sheets |
| Mapbox / OpenStreetMap | Geographic map layer for state-level visualisation |

---

## How to Open

1. Download the `.twbx` file from this repository.
2. Open it in **Tableau Desktop** or **Tableau Public Desktop Edition**.
3. The dataset is embedded inside the `.twbx` — no separate CSV needed.
4. Use the **Category** dropdown filter at the top to slice all charts by product category.

---

## Key Insights from the Dashboard

- **Maharashtra, Karnataka, and Tamil Nadu** account for the highest order volumes — together they represent the core of Amazon India's fashion sales geography.
- **94.21% of orders were shipped successfully**, indicating strong fulfilment performance with a very low cancellation rate.
- **Expedited shipping is preferred over Standard** across all top 10 states — suggesting customers prioritise fast delivery.
- **Amazon.in dominates the sales channel** with 99.86% of orders, while Non-Amazon and B2B segments are negligible.
- **M, L, and XL are the most popular size variants**, which is useful for inventory planning and demand forecasting.
- Revenue peaked around **late April to mid-May 2022** across most categories, particularly in the Set category.

---

## Author

Created as part of a Data Analytics learning project using real-world e-commerce data.


