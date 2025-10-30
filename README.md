# Task7-mysql-python-analysis
A Python and MySQL integration project for internship Task 7 ,connecting MySQL with Python using mysql-connector, performing SQL analysis, and visualizing results with pandas and matplotlib.
# Task 7 — MySQL and Python Integration (Internship Project)

## 🎯 Objective
This project demonstrates how to connect **MySQL** with **Python**, extract data using SQL queries, analyze it with **pandas**, and visualize insights using **matplotlib**.  
It was completed as part of **Internship Task 7** focusing on database connectivity and data analysis.

---

## 🧰 Tools & Technologies
- **MySQL** – Database used to store and manage sales data  
- **Python** – Programming language for analysis and visualization  
- **mysql-connector-python** – To connect Python with MySQL  
- **pandas** – For data manipulation and aggregation  
- **matplotlib** – For creating charts and visual reports  
- **Jupyter Notebook / VS Code** – For running and documenting the code  

---

## 🧩 Project Workflow
1. **Create Database & Table** in MySQL:
   ```sql
   CREATE DATABASE task7_db;
   USE task7_db;

   CREATE TABLE sales (
       id INT AUTO_INCREMENT PRIMARY KEY,
       product VARCHAR(50),
       quantity INT,
       price DECIMAL(10,2),
       order_date DATE
   );

   INSERT INTO sales (product, quantity, price, order_date) VALUES
   ('Notebook', 10, 2.5, '2025-10-01'),
   ('Pen', 50, 0.5, '2025-10-02'),
   ('Notebook', 5, 2.5, '2025-10-03'),
   ('Pencil', 30, 0.25, '2025-10-03'),
   ('Pen', 20, 0.5, '2025-10-04');

2. Connect Python to MySQL using mysql.connector.

3. Run SQL Query inside Python:
   ```sql
   SELECT
    product,
    SUM(quantity) AS total_qty,
    SUM(quantity * price) AS revenue
   FROM sales
   GROUP BY product
   ORDER BY revenue DESC;

4.Analyze and Visualize with pandas + matplotlib.
Output: Sales summary table and Revenue by Product bar chart.

💡 Key Learnings
- How to connect MySQL with Python using mysql-connector-python
- Writing and executing SQL queries inside Python
- Fetching results into pandas DataFrames for analysis
- Visualizing data using matplotlib
- Understanding end-to-end data flow: Database → Python → Visualization

