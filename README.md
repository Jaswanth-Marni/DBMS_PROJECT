# Diagnostic Lab Management System (DLM)

## Overview
The **Diagnostic Lab Management System (DLM)** is a database-driven project designed to manage diagnostic lab operations efficiently. It includes functionalities for managing admins, tests, and patient records, ensuring smooth operations and secure data handling.

## Database Schema
The database consists of the following tables:

1. **`adm` (Admin Table)**
   - Stores admin credentials.
   - Fields:
     - `u_name` (VARCHAR, Primary Key) - Unique username.
     - `pwd` (VARCHAR) - Unique password.

2. **`test` (Test Table)**
   - Maintains test information.
   - Fields:
     - `t_id` (INT, Primary Key) - Unique test ID.
     - `test_name` (VARCHAR) - Name of the test.
     - `test_charge` (INT) - Cost of the test.

3. **`patient` (Patient Table)**
   - Stores patient records.
   - Fields:
     - `p_id` (INT, Primary Key) - Unique patient ID.
     - `t_id` (INT, Foreign Key) - References `test(t_id)`.
     - `p_name` (VARCHAR) - Patient's name.
     - `age` (INT) - Patient's age.
     - `address` (VARCHAR) - Address of the patient.
     - `ph_no` (BIGINT) - Contact number.
     - `gender` (VARCHAR) - Gender of the patient.

## Features
- Secure admin authentication.
- Test management with test name and charges.
- Patient record management, including test associations.
- Foreign key constraints for data integrity.

## How to Use
1. Import the SQL file into MySQL:
   ```sh
   mysql -u your_username -p < dlm.sql
   ```
2. Use the `dlm` database:
   ```sql
   USE dlm;
   ```
3. Start managing records as per requirements.

## Future Enhancements
- Web-based interface for data entry.
- Advanced reporting and analytics.
- Role-based access control.

## License
This project is open-source. Feel free to modify and improve it!

