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


- **Blind SQL Injection Attack**
- **Time-Based Blind SQL Injection**
- **Error-Based SQL Injection**
- **Out-of-Band SQL Injection**
- **Second-Order SQL Injection**