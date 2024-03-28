# Interaction with the Database using SQLModel

## SQL Inline Code Example

Executing a simple SQL query to fetch all data from the `hero` table:

```
SELECT * FROM hero;
```


This query retrieves the entire `hero` table.

## Mixing SQL with Python

SQL wasn't designed for direct integration with programming languages like Python. Typically, SQL code is embedded within a string and sent to the database for execution:

```python
statement = "SELECT * FROM hero;"
results = database.execute(statement)
```

However, this approach lacks editor support for features like inline errors and autocompletion, as the SQL is treated as a plain text string.

## The Risk of SQL Injection

Using raw user input in SQL queries can lead to vulnerabilities. For instance:

```python
# Warning: Vulnerable to SQL Injection!
user_id = input("Type the user ID: ")
statement = f"SELECT * FROM hero WHERE id = {user_id};"
results = database.execute(statement)
```

An attacker could exploit this by injecting malicious SQL commands, potentially leading to data loss or other security breaches.

## SQL Sanitization and Security

SQLModel mitigates these risks by sanitizing inputs, a process that ensures user-provided data is safe before it's used in SQL queries. This is crucial for preventing SQL Injection attacks.

## Utilizing SQLModel for Database Interactions

SQLModel allows using Python classes and objects to interact with the database, avoiding the direct use of SQL strings:

```python
user_id = input("Type the user ID: ")
session.exec(select(Hero).where(Hero.id == user_id)).all()
```

This method prevents SQL Injection by treating user inputs as literal strings, thus maintaining database security.

## ORMs and SQL

SQLModel is an Object-Relational Mapper (ORM) that facilitates the translation between SQL and object-oriented code:

- **Object:** Represents classes and instances in Object-Oriented Programming.
- **Relational:** Pertains to relational databases, where tables are often referred to as relations.
- **Mapper:** A concept from mathematics, where a function maps elements from one set to another.

### Example of a Mapper Function in Python

Here's a simple function demonstrating the concept of mapping in Python:

```python
def map_lower_to_upper(value: str):
    return value.upper()
```

This function maps lowercase letters to uppercase, illustrating the basic idea of a mapping function.
