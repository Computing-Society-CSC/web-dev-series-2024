
- **(5 minutes)** 🤓 **Simpler Example**:
    - Demonstrates how to create and query a SQLite database.

```python
import sqlite3

# Connect to SQLite database
conn = sqlite3.connect("example.db")
cursor = conn.cursor()

# Create a table
cursor.execute("""
CREATE TABLE users (
    id INTEGER PRIMARY KEY,
    name TEXT,
    age INTEGER
);
""")

# Insert data
cursor.execute("INSERT INTO users (name, age) VALUES (?, ?)", ("Alice", 25))
conn.commit()

# Query data
cursor.execute("SELECT * FROM users")
print(cursor.fetchall())

conn.close()
```

- **(15 minutes)** 🏆 **Challenge Example**:
    - Build a simple application with a user interface for data input.

```python
import sqlite3

# Connect to SQLite database
conn = sqlite3.connect("example.db")
cursor = conn.cursor()

# Create a table
cursor.execute("""
CREATE TABLE IF NOT EXISTS users (
    id INTEGER PRIMARY KEY,
    name TEXT,
    age INTEGER
);
""")

# User interface for data input
while True:
    print("1. Add User\n2. View Users\n3. Exit")
    choice = input("Enter your choice: ")

    if choice == '1':
        name = input("Enter name: ")
        age = int(input("Enter age: "))
        cursor.execute("INSERT INTO users (name, age) VALUES (?, ?)", (name, age))
        conn.commit()
        print("User added successfully!")

    elif choice == '2':
        cursor.execute("SELECT * FROM users")
        users = cursor.fetchall()
        for user in users:
            print(f"ID: {user[0]}, Name: {user[1]}, Age: {user[2]}")

    elif choice == '3':
        break

    else:
        print("Invalid choice. Please try again.")

conn.close()
```
