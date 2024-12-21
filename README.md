# UPI Payments Dashboard

This project is a web-based UPI Payments Dashboard designed to fetch and display user-specific details such as personal information, transactions, income, and more. The dashboard interacts with a MySQL database to retrieve and display data dynamically.

## Features
- **User Authentication**: Allows users to log in and fetch their details using a unique `User ID`.
- **Personal Information Display**: Displays user's name, email, phone number, address, date of birth, gender, and occupation.
- **Transaction Analysis**:
  - Total number of transactions.
  - Maximum expenditure in a single transaction.
  - Most used transaction platform.
  - Most common transaction (location, date, and time).
- **Financial Details**:
  - Total income from salary and other sources.
  - Remaining money after expenditure.
  - Credit and debit details.
- **Dynamic and Responsive Design**: A user-friendly interface styled with modern CSS.

## Technologies Used
- **Backend**: PHP for server-side scripting.
- **Database**: MySQL for storing and retrieving user and transaction data.
- **Frontend**: HTML, CSS, and JavaScript for creating a responsive user interface.

## Prerequisites
Before running this project, ensure you have the following installed:
- PHP 7.0 or higher
- MySQL 5.7 or higher
- Web server (e.g., Apache or Nginx)
- A browser for testing the interface

## Database Setup
1. Create a database named `upi_payments` in MySQL.
2. Import the database schema and sample data using the SQL file provided in the project directory (e.g., `upi_payments.sql`).
3. Ensure the database contains the following tables:
   - `user_details`: Stores personal information.
   - `transactions_details`: Stores details of each transaction.
   - `income_sources`: Stores user income details.
   - `credit_details`: Stores credit information.
   - `debit_details`: Stores debit information.
   - `transaction_methods_platform_details`: Stores transaction platform usage data.

## Project Setup
1. Clone the repository or download the project files.
2. Place the project folder in your web server's root directory (e.g., `htdocs` for XAMPP).
3. Open the `config.php` file and update the database connection details:
   ```php
   $host = "127.0.0.1";
   $user = "root";
   $password = "";
   $dbname = "upi_payments";

upi-payments-dashboard/
│
├── index.php              # Main entry point for the dashboard
├── stylesheet.css         # Stylesheet for the frontend design
├── upi_payments.sql       # Database schema and sample data
├── README.md              # Project documentation
