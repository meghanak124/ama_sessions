# AMA Session 6
## 1. How to use debug variable (Django)
- `DEBUG = True` → Used in development
  - Shows detailed error pages
  - Displays stack trace
- `DEBUG = False` → Used in production
  - Hides internal errors
  - Requires proper `ALLOWED_HOSTS`

---

## 2. What is Middleware
- Middleware is a layer between request and response.
- It processes requests before reaching views and responses before returning to client.

Example:
- Authentication
- Logging
- Security checks

---

## 3. What is Jinja
- Jinja is a templating engine used in Python frameworks like Flask.
- Django uses its own template engine (similar to Jinja).

Example:
```
{{ variable }}
{% for item in list %}
```

---

## 4. What is Static File
- Static files are CSS, JS, images.
- Used for frontend styling and behavior.
- Stored in `static/` folder.

---

## 5. Problems faced in SQLite during development
- Not suitable for large-scale applications
- Limited concurrency (multiple users)
- No advanced features like PostgreSQL
- Can cause locking issues

---

## 6. What is need of forms.py
- Used to create forms in Django.
- Handles:
  - Validation
  - Input cleaning
  - Rendering forms

---

## 7. Difference between create and create_user
- `create()`:
  - General object creation
- `create_user()`:
  - Specifically for Django User model
  - Handles password hashing

---

## 8. Difference between annotate and aggregate
- `aggregate()`:
  - Returns single value
- `annotate()`:
  - Adds calculated field to each object

---

## 9. Difference between ASGI and WSGI
- WSGI:
  - Synchronous
  - Handles one request at a time
- ASGI:
  - Asynchronous
  - Supports WebSockets and real-time apps

---

## 10. What is SQL Injection
- A security attack where malicious SQL is inserted.
- Can manipulate database.

Prevention:
- Use ORM
- Use parameterized queries

---

## 11. What is .env file
- Stores environment variables
- Keeps secrets like:
  - API keys
  - DB credentials

---

## 12. What is Dunder Methods
- Special methods in Python starting and ending with `__`

Examples:
- `__init__`
- `__str__`
- `__len__`

---

## 13. Features of Django Admin
- Auto-generated admin panel
- CRUD operations
- Authentication and permissions
- Search and filters
- Easy model management
