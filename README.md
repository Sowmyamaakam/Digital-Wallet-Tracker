# UPI Payments Dashboard
A web app to track UPI transactions by uploading PhonePe transaction screenshots. It uses OCR to extract details (amount, date, time, sender/receiver) and stores them in Firebase Firestore. Features a financial dashboard with spending insights, cash flow analysis, and savings suggestions.
![Dashboard Screenshot](https://github.com/VaishnaviVadla33/DigitalWalletTracker02/raw/main/Dashboard_image.png)

## Features

* **Transaction Screenshot Upload:** Upload images (screenshots) of UPI transaction confirmations.
* **OCR Data Extraction:** Automatically extracts transaction details (amount, date, time, status - credited/debited, sender/receiver) from the uploaded image using Pytesseract.
* **Manual Data Entry/Edit:** Allows users to review and edit extracted details or manually input transaction data via a form.
* **Transaction Categorization:** Classify transactions as Personal, Regular Bills, or Business, and add personal references (Family, Friends, Others).
* **Priority Rating:** Rate transactions based on necessity (Necessary, Moderate, Not Necessary).
* **Firebase Firestore Integration:** Securely stores credit and debit transaction data in separate Firestore collections.
* **Transaction History:** View a detailed history of all recorded credit and debit transactions in tabular format.
* **Financial Dashboard:**
    * Visualize credit and debit transaction history over time (Line Chart).
    * Compare monthly spending across different years (Bar Chart).
    * Analyze cash flow with an Inflow vs. Outflow summary (Doughnut Chart).
    * Identify peak transaction times (Bar Chart).
    * Receive potential savings suggestions based on spending categories.
    * Get alerts for significant spending amounts.

## Technologies Used

* **Backend:** Python, Flask
* **Database:** Google Firebase Firestore
* **OCR:** Pytesseract, Pillow (PIL Fork)
* **Data Analysis:** Pandas, NumPy, Scikit-learn
* **Frontend:** HTML, CSS, JavaScript
* **Charting:** Chart.js
* **Environment Variables:** python-dotenv
* **Deployment (Implied):** Gunicorn (listed in requirements)


## Prerequisites

- **Hardware**:
  - Computer with 4GB+ RAM, 2GB free disk space.
  - Internet connection.

- **Software**:
  - OS: Windows, macOS, or Linux.
  - Python 3.6+ (`python --version`).
  - Tesseract OCR:
    - Windows: Install from [Tesseract at UB Mannheim](https://github.com/UB-Mannheim/tesseract/wiki).
    - Linux: `sudo apt-get install tesseract-ocr`.
    - macOS: `brew install tesseract`.
  - Git (`git --version`): Install from [git-scm.com](https://git-scm.com/downloads).
  - Modern web browser (e.g., Chrome).

- **Development Tools**:
  - Code editor (e.g., VS Code).
  - Virtual environment: `python -m venv venv`.

- **Firebase Account**:
  - Firebase project with Firestore enabled.
  - Service Account JSON key.

- **Python Dependencies** (via `requirements.txt`):
  - Flask, Pytesseract, Pillow, Pandas, NumPy, Scikit-learn, Firebase-Admin, python-dotenv, Gunicorn.

- **Setup**:
  - Firebase config: Set `FIREBASE_CREDENTIALS` in `.env`.
  - PhonePe transaction screenshots (clear, full).

- **Optional (Deployment)**:
  - Gunicorn for production.
  - Hosting platform supporting Python/Tesseract.
 
  ## Live Demo & Conclusion

This application provides a practical way to digitize and analyze your PhonePe transaction history.

You can access a live preview of the website hosted on Render here:

**[Website Preview](https://digitalwallettracker02.onrender.com/)**

**Important Demo Limitation:** Please note that the **OCR/image extraction functionality does not work** in this hosted preview version due to deployment environment limitations (likely related to Tesseract dependencies). The demo primarily showcases the frontend interface, form structure, and dashboard layout.

To experience the full application, including the transaction data extraction, please follow the given setup--installation steps to run it on your local machine.



