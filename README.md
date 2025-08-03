# 🏥 Hospital Data Analysis (SQL Project)

This project demonstrates a complete SQL-based analysis on hospital data, including patient records, treatments, billing, and doctor statistics.  
Designed as a portfolio project for **Data Analyst roles**.

---

## 📄 Project Structure

- **`hospital_schema.sql`** → Table creation scripts
- **`hospital_data_inserts.sql`** → Sample data (100+ rows)
- **`analytics_queries.sql`** → Analytical queries for insights
- **`README.md`** → Project overview

---

## 🗺️ ER Diagram


### Visual ER Diagram:

```plaintext
+---------------+          +----------------+          +------------------+
|   Departments |          |    Doctors     |          |     Patients     |
+---------------+          +----------------+          +------------------+
| department_id |◄────┐    | doctor_id      |◄────┐    | patient_id       |
| name          |     └───▶| name           |     └───▶| name             |
+---------------+          | department_id  |          | age              |
                           +----------------+          | gender           |
                                                        +------------------+

+----------------+         +----------------+
|   Treatments   |         |     Billing     |
+----------------+         +----------------+
| treatment_id   |         | billing_id      |
| patient_id     |────────▶| patient_id      |
| doctor_id      |────────▶| treatment_id    |
| treatment_date |         | amount          |
+----------------+         | payment_date    |
                           +----------------+
