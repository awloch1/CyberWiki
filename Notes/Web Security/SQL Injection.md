SQL injection (SQLi) is a web security vulnerability that allows an attacker to interfere with the queries that an application makes to its database.

### systematic set of tests against SQLi:
-  single quote character `'`
-  Compare application responses using SQL syntax with original and altered values.
-  Boolean conditions such as `OR 1=1` and `OR 1=2`
-  Payloads designed to trigger time delays
-  OAST(**Out-of-Band Application Security Testing**) payloads

**SQL injection can occur anywhere user input is included in a query.**
**Common locations:**
    - `SELECT` → `WHERE`, table/column names, `ORDER BY`
    - `UPDATE` → values or `WHERE`
    - `INSERT` → inserted values
**Test all dynamic SQL parts, not only filters.**

### SQL injection types
- **Classic SQL Injection Attack** - injecting malicious SQL syntax into user inputs to manipulate queries, often using techniques like **authentication bypass**, **commenting out query parts (`--`)**, or **altering query logic (`OR 1=1`)**.

- **Union-Based SQL Injection** - injecting `UNION` into SQL query to get information from other table. When you are using `UNION` you have to have the same amount of columns. to check the amount of columns you can use order by 1, 2, 3, ... until it returns error or write null columns until it fits.

- **Blind SQL Injection Attack** - SQL injection where the application does not show query results or database errors. Instead, you can extract information by triggering different responses with `TRUE` or `FALSE` conditions, e.g. `AND 1=1` vs `AND 1=2`.

- **Time-Based Blind SQL Injection** - SQL injection where the application does not reveal query results or database errors. Instead, information is inferred by causing **conditional time delays** and measuring the server's response time, e.g. `IF(condition, SLEEP(10), 0)`.

- **Error-Based SQL Injection** - SQL injection where database errors are used to extract information. There are two common types: **conditional errors**, where an error is triggered only when a condition is true, and **verbose error messages**, where the database directly reveals useful information in the error response.

- **Out-of-Band SQL Injection**

- **Second-Order SQL Injection** - Second-order SQL injection occurs when the application takes user input from an HTTP request and stores it for future use

### How to prevent SQL injection
SQL injection can be prevented by using **parameterized queries (prepared statements)** instead of building SQL queries with string concatenation. This keeps user input separate from the SQL code and treats it only as data.

### SQL injection cheat sheet:
https://portswigger.net/web-security/sql-injection/cheat-sheet