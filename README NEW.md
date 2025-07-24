# 📊 Telecom Sales Analytics Dashboard (Power BI + SQL)

An interactive business intelligence dashboard for analyzing telecom product sales, powered by Oracle SQL and Power BI.

This project simulates a real-world telecom sales environment using synthetic data and Oracle SQL procedures. The data is visualized in Power BI dashboards to uncover insights about:

- Product category sales
- Customer purchasing behavior
- Store and employee performance
- Return rates and revenue trends

---

## 📁 Project Structure

```
Telecom-Sales-Dashboard/
├── powerbi/
│   └── TelecomSales.pbix
├── sql/
│   ├── create_tables.sql
│   ├── insert_employees.sql
│   ├── insert_products.sql
│   ├── insert_stores.sql
│   ├── procedures.sql
│   └── sequence_trigger.sql
├── screenshots/
│   ├── dashboard_revenue.png
│   ├── sales_by_category.png
│   ├── customer_activity.png
│   ├── returns_analysis.png
│   └── employee_performance.png
├── LICENSE
└── README.md
```

---

## ⚙️ Technologies Used

- **Power BI Desktop** (.pbix)
- **Oracle SQL / PL/SQL**
- **DAX (Data Analysis Expressions)**

---

## 🧱 Database Design

### Tables

| Table Name      | Description                               |
|------------------|-------------------------------------------|
| `Stores`         | Store information (ID, name, location)    |
| `Products`       | Product catalog with pricing & category   |
| `Customers`      | Customer demographics                     |
| `Employees`      | Staff data by store                       |
| `Orders`         | Orders placed by customers                |
| `OrderItems`     | Products in each order (OrderID + ProductID) |

> **Note:** Data is synthetically generated for demo purposes using `DBMS_RANDOM`.

---

## 🔄 Procedures & Sequences

### ✅ Procedures

- `PopulateOrdersAndItems`: Randomly fills order & item data
- `PopulateCustomers`: Generates random customers

### 🔁 Triggers & Sequences

- `Customers_Seq`: Auto-increments `CustomerID`
- `Customers_Trigger`: Assigns `CustomerID` automatically during insert

---

## 📊 Power BI Dashboards

### Dashboard Pages

- **💰 Total Revenue** – Revenue overview, filterable by store/date/type
- **📦 Sales by Category** – Breakdown by product category, brand, price
- **👥 Customer Insights** – Purchases, frequency, total spend
- **🔁 Returns Analysis** – Product return metrics
- **🏆 Employee Performance** – Orders handled & revenue per staff

---

## 🧮 DAX Measures

| Measure Name         | Description                                              |
|----------------------|----------------------------------------------------------|
| `Total Revenue`       | SUM(Quantity × Price)                                    |
| `Average Price`       | AVERAGE(Price)                                           |
| `Total Orders`        | COUNT of unique OrderIDs                                |
| `Adjusted Revenue`    | Revenue adjusted for dynamic pricing                    |
| `High Ticket Orders`  | Orders exceeding average product price                  |

---

## 🖼️ Screenshots

Below are samples of key dashboard pages included in the `.pbix` file:

| Dashboard View         | Screenshot                                 |
|------------------------|--------------------------------------------|
| Total Revenue          | ![](screenshots/dashboard_revenue.png)     |
| Sales by Category      | ![](screenshots/sales_by_category.png)     |
| Customer Activity      | ![](screenshots/customer_activity.png)     |
| Returns Analysis       | ![](screenshots/returns_analysis.png)      |
| Employee Performance   | ![](screenshots/employee_performance.png)  |

> Make sure to keep screenshots in the `screenshots/` folder for proper rendering.

---

## 🚀 How to Run

1. **Run the SQL Scripts in Order:**
   - `create_tables.sql`
   - `insert_employees.sql`
   - `insert_products.sql`
   - `insert_stores.sql`
   - `procedures.sql`
   - `sequence_trigger.sql`

2. **Open Power BI File**  
   Use Power BI Desktop to open `powerbi/TelecomSales.pbix`.

3. **Connect to Your Data Source**  
   Update the data source connection to match your SQL environment.

4. **Explore the Dashboard**  
   Use filters and slicers to analyze KPIs and business insights.

---

## 👩‍💻 Author

**Aysel Nasibova**  
[LinkedIn](#) • [GitHub](https://github.com/AyselNasibova)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 📎 Disclaimer

This project is for **educational and portfolio** use. All data is artificially generated.
