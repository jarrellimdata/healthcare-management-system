# 🏥 Hospital Management System

A simple database-backed backend system to simulate a hospital management platform. Built with Python + PostgreSQL.

---

## 📘 Introduction

This project helps manage patients, doctors, and appointments in a hospital system using a PostgreSQL database and Python scripts.

---

## 🔧 Features

- Patient & Doctor registration
- Appointments and Diagnoses
- SQL schema & ER diagram

---

## ▶️ How to Use

1. **Set up PostgreSQL DB**
   ```bash
   createdb hospital_db
   psql -d hospital_db -f sql/schema.sql
   psql -d hospital_db -f sql/insert_sample_data.sql
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure DB connection**

   Edit your DB credentials in `python/db_connection.py`.

4. **Run the app**
   ```bash
   python python/main.py
   ```

5. *(Optional)* Launch the UI:
   ```bash
   streamlit run python/streamlit_app.py
   ```

---

## 🧩 Modules

| File/Module           | Purpose                        |
|----------------------|---------------------------------|
| `db_connection.py`   | Connect to PostgreSQL database |
| `patient.py`         | Handle patient operations      |
| `doctor.py`          | Handle doctor operations       |
| `appointment.py`     | Manage appointments            |
| `crud_operations.py` | Shared CRUD logic              |
| `main.py`            | Main entry point               |

---

## 🗂️ Folder Structure

```
hospital-management-system/
├── sql/
│   ├── schema.sql              # SQL schema setup
│   ├── insert_sample_data.sql # Populate sample data
│   ├── queries.sql            # Reusable or testing SQL queries
│   └── er_diagram.png         # ERD image (exported or hand-drawn)
│
├── python/
│   ├── db_connection.py       # Centralized DB connection logic
│   ├── crud_operations.py     # Shared generic insert/update/delete
│   ├── patient.py             # Patient-specific functions
│   ├── doctor.py              # Doctor-specific functions
│   ├── appointment.py         # Appointment handling
│   ├── queries.py             # Python-side SQL queries if needed
│   ├── main.py                # CLI or entry point
│   └── (optional: streamlit_app.py or cli.py) # UI
│
├── README.md                  # Project intro, setup, usage, etc.
└── requirements.txt           # List of Python libraries
```

---

## 📦 Requirements

- Python 3.x
- PostgreSQL
- Python packages in `requirements.txt`
