### 🔹 Module 3: Accessing Databases using Python

This module was all about bridging SQL with Python — combining the querying power of SQL with the analytical flexibility of Python. It showed how to connect to databases directly from Python, run SQL queries, and manipulate results using Pandas.

---

#### 🛠️ Tools and Technologies
- **Python Libraries**
  - `ibm_db` and `ibm_db_sa` for connecting to IBM DB2 databases  
  - `SQLAlchemy` for handling SQL in Python  
  - **Pandas** for converting query results into DataFrames  
- **Jupyter Notebook** with `%sql` magic for interactive queries

---

#### 📊 Key Topics Covered

- **Connecting to a Database**
  ```python
  import ibm_db
  dsn = "DATABASE=BLUDB;HOSTNAME=hostname;PORT=50000;PROTOCOL=TCPIP;UID=user;PWD=password;"
  conn = ibm_db.connect(dsn, "", "")
  ```
  Learned how to establish a secure connection to a DB2 instance on IBM Cloud
- **Running SQL Queries in Python**
  ```python
  import pandas as pd
  import ibm_db_dbi
  conn = ibm_db_dbi.Connection(conn)
  df = pd.read_sql("SELECT * FROM Employees", conn)
  ```
  Directly pulled SQL results into a Pandas DataFrame.
- **Using SQLAlchemy for Abstraction**
  SQLAlchemy made queries easier to manage:
  ```python
  from sqlalchemy import create_engine
  engine = create_engine("ibm_db_sa://user:password@hostname:50000/BLUDB")
  df = pd.read_sql("SELECT Name, Salary FROM Employees", engine)
  ```
- **SQL Magic in Jupyter**
  Magic commands like:
  ```python
  %sql SELECT Name, Age FROM Employees WHERE Age > 30
  ```
  allowed inline querying without leaving the notebook.
- **Data Wrangling After Querying**
  Once queries returned DataFrames, I could immediately apply Pandas methods:
  ```python
  df['AnnualSalary'] = df['Salary'] * 12
  df.describe()
  ```
### 🧑‍💻 My Experience
This module felt very close to industry workflows. I loved how I could query the database and immediately start analyzing results in Pandas — no need for manual exports.

Setting up the DB2 connection was a bit tricky the first time, especially handling the connection string. But once it worked, the integration was smooth. The %sql magic in Jupyter was a game-changer: it made switching between Python and SQL effortless.

What stood out most was how I could combine SQL and Python power. For example, I used SQL to filter data heavily, then Pandas to do feature engineering. It felt like I had the best of both worlds.

✅ What I Learned
- Establishing database connections from Python
- Running SQL queries directly in Jupyter with `%sql`
- Using Pandas to analyze query outputs
- Automating data pipelines: query → DataFrame → analysis
- Practical use of `SQLAlchemy` for clean, reusable code

🎯 Final Takeaway
After this module, I stopped thinking of SQL and Python as separate tools. Together, they form a seamless data science workflow: SQL for powerful queries, Python for flexible analysis.

I walked away confident that I could connect to real databases in a workplace, extract insights, and build pipelines that run smoothly. This module made me feel like I had stepped into the professional zone of data science 🚀🐍📊
