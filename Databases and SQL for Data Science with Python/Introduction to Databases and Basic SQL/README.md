### 🔹 Module 1: Introduction to Databases and Basic SQL

This module was the foundation for understanding how databases work and why SQL is essential for data science. Instead of jumping into advanced queries, it built a strong base with the structure of databases and the logic behind relational models.  

---

#### 🛠️ Tools and Technologies
- **SQL (Structured Query Language)** for querying databases  
- **DB2 on Cloud** (IBM’s database service) for hands-on practice  
- **Jupyter Notebook + SQL Magic Commands** (`%sql`) for interactive querying  
- **Pandas** to convert SQL query results into DataFrames  

---

#### 📊 Key Topics Covered
- **Database Basics**  
  - Difference between relational and non-relational databases  
  - Tables, rows, and columns structure  
  - Primary keys and foreign keys for unique identification and relationships  

- **Basic SQL Queries**  
  ```sql
  SELECT * FROM Customers;
  SELECT Name, Age FROM Employees WHERE Age > 30;
  ````
  Learned how to retrieve data using SELECT, filter with WHERE, and order     results with ORDER BY.
- **Using Operators**  
  ```sql
  SELECT Name, Salary
  FROM Employees
  WHERE Department = 'IT' AND Salary > 60000;
  ````
  Practiced logical operators (AND, OR, NOT) and comparison operators (=,     <, >).
- **Sorting and Limiting Results**
  - ORDER BY for sorting results in ascending/descending order
  - LIMIT (or FETCH FIRST N ROWS) to control the number of results returned
- **Introduction to Functions**
  Learned to use simple SQL functions like COUNT(), AVG(), MAX(), and MIN().

### 🧑‍💻 My Experience
Coming from a Python background, I initially thought SQL would be rigid, but it turned out to be very intuitive. I loved how concise SQL queries could fetch exactly what I wanted. Using DB2 on Cloud in Jupyter Notebook felt like real industry practice — I could run SQL queries directly inside the notebook and instantly convert the results into Pandas DataFrames for further analysis.

It was also interesting to see how relational databases enforce data integrity through primary and foreign keys. That structure gave me a sense of why SQL has survived decades and is still dominant. One challenge I faced was remembering the syntax differences between DB2 and MySQL (like FETCH FIRST instead of LIMIT), but the course guided me well with examples.

✅ What I Learned
- How relational databases store and manage data
- Writing SQL queries to filter, sort, and select data
- Using aggregate functions like COUNT() and AVG()
- Integrating SQL queries inside Jupyter notebooks
- Importance of primary/foreign keys for linking data

🎯 Final Takeaway
After this module, I realized SQL is not just a supporting skill — it’s a core superpower for any data scientist. Instead of loading CSVs blindly, I can now directly query large datasets stored in databases. The integration with Pandas made it even more powerful, bridging the gap between database management and data analysis.

This module gave me the confidence that I could step into any organization, connect to their database, and start pulling meaningful insights without depending on pre-cleaned files. 🚀
