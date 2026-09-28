# Employee Database Manager

A Python and PostgreSQL learning project that demonstrates how to create, read, update, and delete employee records. The project also includes salary filtering, summary calculations, transaction handling, and safe database operations.

## Features

- Connects Python to PostgreSQL using `psycopg2`
- Creates an `employees` table when it does not already exist
- Adds six sample employee records without duplicating existing IDs
- Lists all employees
- Filters employees by minimum salary
- Adds, updates, and deletes employee records
- Calculates employee count, total salary, average salary, minimum salary, and maximum salary
- Uses `commit()` and `rollback()` for transaction safety
- Requests the database password securely instead of storing it in the notebook

## Technologies Used

- Python
- PostgreSQL
- SQL
- Jupyter Notebook
- `psycopg2-binary`

## Project File

- `employee_database_manager.ipynb` — contains the database setup, CRUD functions, queries, reports, and optional practice commands

## Database Schema

| Column | Type | Rules |
|---|---|---|
| `id` | Integer | Primary key |
| `name` | Text | Cannot be null |
| `salary` | Numeric | Must be zero or greater |

## Setup

1. Install PostgreSQL and create a database named `company_db`.
2. Open `employee_database_manager.ipynb` in Jupyter Notebook or VS Code.
3. Install the required package:

   ```bash
   pip install psycopg2-binary
   ```

4. Update the PostgreSQL connection details if your username, host, or port is different.
5. Run the notebook cells from top to bottom.
6. Enter your PostgreSQL password when prompted.

## Example Operations

```python
list_employees()
get_employees_above(60000)
add_employee(99, "Test Employee", 4000)
update_salary(99, 4500)
delete_employee(99)
salary_summary()
```

The optional data-changing commands are commented out in the notebook so records are not changed accidentally.

## Sample Salary Summary

Using the six sample employee records, the project returns:

- Employees: 6
- Total salaries: 356000
- Average salary: 59333.33
- Lowest salary: 50000
- Highest salary: 68000

## What I Learned

This project strengthened my understanding of connecting Python to PostgreSQL, writing reusable CRUD functions, using parameterized SQL queries, handling transactions, validating data, and organizing a notebook for a GitHub portfolio.

## Security Note

The PostgreSQL password is requested with `getpass` and is not saved in the notebook. Never upload passwords, credentials, or private connection strings to GitHub.
