# AMA Session

## 1. Difference between DELETE, DROP and TRUNCATE
- **DELETE**
  - Removes specific rows (can use WHERE)
  - Can be rolled back

- **TRUNCATE**
  - Removes all rows
  - Cannot use WHERE
  - Cannot be rolled back 

- **DROP**
  - Deletes entire table structure
  - Table is removed completely

---

## 2. What are Static Files in Django?
- Static files = CSS, JS, Images
- Used for frontend styling and behavior
- Stored in `static/` folder
- Served using Django static configuration

---

## 3. What is ORM?
- ORM = Object Relational Mapping
- allows you to connect to database with python without SQL
- Converts Python objects ↔ Database tables
- Example:
```python
Question.objects.all()
```
- No need to write SQL manually

---

## 4. Difference between GROUP BY and Window Functions
- **GROUP BY**
  - Groups rows
  - Reduces rows
  - Example: total sales per year
```sql
SELECT batting_team, SUM(total_runs) AS total_runs
FROM deliveries
GROUP BY batting_team;
```
Output
| batting_team |	total_runs |
| ----- | ----- |
MI |	25000
CSK |	24000

- **Window Function**
  - Does NOT reduce rows
  - Works over a "window" of rows
  - Example: rank within a group
```sql
SELECT batsman,
       batsman_runs,
       SUM(batsman_runs) OVER (PARTITION BY batsman) AS total_runs
FROM deliveries;
```
Output
|batsman|	batsman_runs|	total_runs|
|----|----|------|
Kohli	|4	|6400
Kohli	|6	|6400
Rohit|	2	|5800

---

## 5. Features of Django
- Fast development
- Built-in admin panel
- ORM
- Security (CSRF, SQL injection protection)
- Scalable
- MTV architecture

---

## 6. Difference between makemigrations and migrate
- **makemigrations**
  - Creates migration files
- **migrate**
  - Applies changes to database

---

## 7. What is URL Routing?
- is the process of mapping URLs to views so that when a user requests a URL, the corresponding view function is executed and a response is returned.
- Mapping URL → view function
- Defined in `urls.py`

---

## 8. Benefits of PostgreSQL
- Open source
- Supports complex queries
- ACID compliant
- Highly scalable
- Supports JSON
- compared to Mysql and sqlite, postgres is more secure and scalable
---

## 9. Use of urls.py
- Defines URL patterns
- Connects URLs to views

---

## 10. What is DOM Tree?
- Tree structure of HTML elements
- Browser converts HTML → DOM
- JS can manipulate DOM

---

## 11. What is MVT?
- django follows MVT architecture where
- Model → Data
- View → Logic
- Template → UI

---

## 12. Inbuilt DB in Django
- SQLite (default)
- Lightweight and easy setup
- applicable for small applications

---

## 13. What is Middleware?
- Runs between request and response
- Used for authentication, logging, etc.

---

## 14. What is a Model in Django?
- Represents database table
- Defined using Python class

Example:
```python
class Question(models.Model):
    question_text = models.CharField(max_length=200)
```
