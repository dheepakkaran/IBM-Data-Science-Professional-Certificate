### 🔹 Module 2: Advanced SQL for Data Science

This module took SQL to the next level, moving beyond basic queries to advanced techniques that allow complex data manipulation and analysis. It felt like the point where SQL truly became a powerful analytical tool.

---

#### 🛠️ Tools and Technologies
- **SQL (IBM DB2 on Cloud)** for advanced querying  
- **Jupyter Notebook with SQL Magic Commands** for interactive work  
- **Pandas** for converting complex SQL query outputs into DataFrames  

---

#### 📊 Key Topics Covered

- **Joins in SQL**
  Learned how to combine data from multiple tables:
  ```sql
  SELECT c.Name, o.OrderDate
  FROM Customers c
  INNER JOIN Orders o
  ON c.CustomerID = o.CustomerID;
  ```
  - `INNER JOIN` → only matching records
  - `LEFT JOIN` → all from left table, plus matches
  - `RIGHT JOIN` → all from right table, plus matches
  - `FULL OUTER JOIN` → all records with matches where possible
- **Subqueries**
  Nested queries to refine results:
  ```sql
  SELECT Name
  FROM Employees
  WHERE Salary > (SELECT AVG(Salary) FROM Employees);
  ```
  This allowed filtering data based on dynamic conditions.
- **Set Operations**
  - `UNION` → combine results from multiple queries
  - `INTERSECT` → return common rows
  - `EXCEPT` → return rows in first query not in second
- **String and Date Functions**
  - `UPPER()`, `LOWER()`, `LENGTH()` for strings
  - `CURRENT_DATE`, `YEAR()`, `MONTH()` for handling dates
- **CASE Statements**
  Creating conditional logic within queries:
  ```sql
  SELECT Name,
       CASE WHEN Score >= 90 THEN 'A'
            WHEN Score >= 75 THEN 'B'
            ELSE 'C'
       END AS Grade
  FROM Students;
  ```

### 🧑‍💻 My Experience
This module was a real game-changer. Joins in particular opened my eyes to how relational databases actually shine — combining multiple tables to get richer insights. I enjoyed writing queries that brought together customers, orders, and product data into a single table.

The subqueries were a bit challenging at first, especially remembering when to use them in `WHERE` vs `FRO`M clauses. But after practicing with examples like finding employees above average salary, it clicked.

Another favorite was using `CASE` to create new categorical columns directly in SQL — it felt like feature engineering without leaving the database. Working in Jupyter made it even better, since I could visualize results in Pandas right after querying.

✅ What I Learned
- Writing different types of SQL joins for multi-table analysis
- Creating dynamic filters with subqueries
- Using set operations to combine or compare results
- Applying string and date functions for richer data cleaning
- Embedding logic into SQL with CASE statements

🎯 Final Takeaway
After this module, I stopped seeing SQL as just a query tool. It’s a mini analytics engine. Instead of exporting raw tables to Python, I can pre-clean and reshape data within SQL, saving massive time.

This was the module that made me feel confident about handling real business databases — where data is scattered across multiple tables. It proved that SQL is not optional; it’s essential.
