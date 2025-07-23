# 📒 Contact Book – Python + MySQL Project

A simple command-line Contact Book application built in Python that uses a MySQL database for persistent storage. Users can add, view, and search for contacts by name.

---

## 🧰 Features

* ➕ Add new contacts (name, phone, email)
* 📃 View all saved contacts
* 🔍 Search for a contact by name
* 💾 Persistent storage with MySQL
* 🔐 Graceful connection handling and cleanup

---

## 🗃️ Project Structure

```bash
.
├── contact.py             # Defines the Contact class
├── contact_book.py        # Handles all database operations
├── mains.py               # Main CLI application
```

---

## 🐍 Requirements

* Python 3.x
* MySQL server
* Python packages:

  * `mysql-connector-python`

Install dependencies:

```bash
pip install mysql-connector-python
```

---

## 🛠️ Setup Instructions

1. **Create the MySQL database**:

```sql
CREATE DATABASE contact_book;
USE contact_book;

CREATE TABLE contacts (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    phone VARCHAR(20),
    email VARCHAR(100)
);
```

2. **Update MySQL credentials** in `contact_book.py`:

```python
connection = mysql.connector.connect(
    host='localhost',
    database='contact_book',
    user='your_username',
    password='your_password'
)
```

3. **Run the application**:

```bash
python mains.py
```

---

## 📂 Code Overview

### `contact.py`

Defines the `Contact` class with attributes: `name`, `phone`, and `email`.

### `contact_book.py`

Handles:

* Database connection
* Adding, displaying, and searching contacts
* Managing connection lifecycle

### `mains.py`

CLI-driven user interface:

* Provides a menu to interact with the app
* Calls methods from `ContactBook`

---

## 🚀 Example Usage

```bash
Contact Book Menu:
1. Add Contact
2. Display All Contacts
3. Search Contact
4. Exit
```

---

## 🙌 Contribution

Feel free to fork the repository, raise issues, or suggest features!


