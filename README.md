# 📒 Python Contact Manager

A lightweight, desktop-based Address Book application built with **Python**, **Tkinter**, and **SQLite**. This application allows users to store personal contacts locally, offering a clean graphical interface to add, view, update, and delete entries.

## 🚀 Features

* **GUI Interface:** Built using Tkinter's `Treeview`, `LabelFrame`, and `Toplevel` widgets for a native desktop experience.
* **CRUD Operations:**
    * **Create:** Add new contacts (Name, Email, Phone Number).
    * **Read:** View all contacts in a sortable list.
    * **Update:** Modify phone numbers via a dedicated pop-up window.
    * **Delete:** Remove selected contacts from the database.
* **Data Persistence:** Uses SQLite (`contacts.db`) to save data locally.
* **Input Validation:** Prevents empty entries to ensure data integrity.

## 🛠️ Prerequisites

Before running the application, ensure you have the following:

1.  **Python 3.x** installed.
2.  **Tkinter** (usually included with Python).
3.  **SQLite3** (included with Python).

## 📂 Project Structure

Ensure your directory looks like this for the code to run without errors:

```text
├── icons/
│   └── logo.gif       # Required for the app icon (referenced in code)
├── main.py            # The python script provided
├── contacts.db        # Generated automatically (see Setup below)
└── README.md
```
⚙️ Setup & Installation
1. Database Initialization
Important: The provided Python code assumes the database table already exists. You must create the table before running the app for the first time.

Open your terminal or a SQLite browser and run the following SQL command to create the necessary table:

SQL
CREATE TABLE IF NOT EXISTS contacts_list (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT,
    email TEXT,
    number TEXT
);
Alternatively, you can add a create_table function to the __init__ method in your Python script.

2. Icon Setup
The code looks for an image at icons/logo.gif.
Create a folder named icons in the same directory as your script.
Place a .gif image inside it and name it logo.gif.
(If you don't have an image, you can comment out the create_left_icon method call in the code).

3. Running the App
Run the script using Python:
Bash
python main.py

🖥️ Usage Guide
Add Contact: Fill in the Name, Email, and Number fields in the top right panel and click "Add Contact".
View Contacts: The list updates automatically. You can scroll through the Treeview on the left.
Modify: Select a row, click "Modify Selected", and enter a new phone number in the pop-up window.
Delete: Select a row and click "Delete Selected" to remove the record permanently.

🧩 Technologies Used
Language: Python
GUI Framework: Tkinter (ttk)
Database: SQLite3




