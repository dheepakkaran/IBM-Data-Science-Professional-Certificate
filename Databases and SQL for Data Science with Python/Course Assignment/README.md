### 🔹 Module 4: Course Assignment

The final module of this course was a **hands-on project** where I had to apply everything I learned in SQL and Python to solve real-world database problems. Unlike quizzes, this was a structured notebook assignment that tested both technical accuracy and clarity of explanation.

---

#### 🛠️ Tools and Technologies
- **IBM DB2 on Cloud** for hosting and querying the database  
- **SQL** for retrieving and analyzing data  
- **Python (Pandas + SQLAlchemy + ibm_db)** for running queries and refining results  
- **Jupyter Notebook** for presenting code, results, and explanations in one place

---

#### 📊 Assignment Tasks

1. **Database Connection**
   - Connect to the IBM DB2 instance using `ibm_db` or `%sql` magic in Jupyter.

     ```python
     %sql ibm_db_sa://username:password@hostname:50000/BLUDB
     ```
2. **Exploring the Tables**
   - Write queries to list all tables in the database.
   - Inspect schema to understand available columns and data types.
3. **Basic Queries**
   - Use `SELECT` statements to retrieve data.
   - Apply `WHERE` conditions and sorting to answer specific business questions.
4. **Advanced Queries**
   - Perform `INNER JOIN` and `LEFT JOIN` to combine data from multiple tables.
   - Use subqueries to find values above averages or within certain thresholds.

     ```sql
     SELECT Name, Salary
     FROM Employees
     WHERE Salary > (SELECT AVG(Salary) FROM Employees);
     ```
5. **Aggregate Analysis**
   - Apply functions like `AVG()`, `COUNT()`, `MAX()`, and `SUM()` to generate summary statistics.
6. **Advanced Queries**
   - Convert SQL outputs into Pandas DataFrames and perform further analysis.

     ```python
     import pandas as pd
     df = %sql SELECT Department, AVG(Salary) AS AvgSalary FROM Employees GROUP BY Department
     pd.DataFrame(df, columns=['Department', 'AvgSalary'])
     ```
7. **Final Report**
   - Document queries, results, and insights in Markdown.
   - Summarize findings clearly as if presenting to a stakeholder.

### 🧑‍💻 My Experience
This assignment was the perfect capstone challenge. It wasn’t just about writing SQL; it was about understanding the business questions and structuring queries logically. The most rewarding part was using joins to combine employee and department data into one dataset and then analyzing salary distribution across departments.

Working in Jupyter made the process seamless. I could run SQL queries, immediately see the results, and then transform them with Pandas for further insights. Writing explanations in Markdown alongside the queries gave the notebook a professional touch — it looked like a real data analysis report.

The only challenge I faced was ensuring queries were efficient. Some subqueries initially took too long to run, but optimizing them with `JOIN` instead of nested queries improved performance. This taught me that query design matters as much as query logic.

✅ What I Learned
- End-to-end database analysis: connect → query → refine → present
- Combining SQL joins and aggregates to answer complex questions
- Exporting SQL results to Pandas for extended analysis
- Documenting work professionally in Jupyter
- Thinking like a data analyst solving real business problems

🎯 Final Takeaway
Completing this assignment made me realize that I could now handle a full SQL workflow in a real job setting. From connecting to databases to producing stakeholder-ready reports, I felt equipped with skills that go beyond theory.

This final project gave me a sense of closure — proving that I can not only write SQL queries but also integrate them into a Python-powered data science pipeline. It was the ultimate confidence booster and the perfect ending to the SQL course 💪🐍📊
