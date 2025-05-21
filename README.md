# DNA Sample Tracking System – Project 4900

This project was completed as part of a research-driven academic initiative at **Brooklyn College’s Bioinformatics Laboratory**. It builds upon a previously developed web application by introducing major backend and frontend improvements. The primary goal was to optimize the **organization, security, and scalability** of DNA sequencing workflows.

---

## 🧬 Key Contributions

- Linked biological sample metadata with a structured database schema.
- Password-protected actions for sensitive operations like deleting experiments.
- CSV upload/download support via the frontend with future cloud integration potential.
- Evolved the system into a secure, scalable, and user-friendly platform for managing genomic datasets.

---

## 🚀 Features

- **Pagination & Search:** Retrieve table data with pagination and search capabilities.
- **Dynamic Table Validation:** Ensures only allowed tables are accessed or modified.
- **CRUD Operations:**
  - `Create` – Add experiments, runs, computers, or minions.
  - `Read` – Fetch records with pagination/search.
  - `Update` – Edit existing records.
  - `Delete` – Admin password required.
- **Error Handling:** Centralized error messaging for API consistency.
- **Environment Config:** `.env` file support to manage sensitive database settings.

---

## 📁 Project Structure

BC_Nanopore_Tracker/
├── controllers/
│ └── dbController.js # DB operations
├── middlewares/
│ └── validateTable.js # Table name validation
├── models/
│ ├── db.js # MySQL connection
│ └── tableModel.js # Query logic
├── routes/
│ └── dataRoutes.js # API endpoints
├── frontend/ # Frontend files (CSV import/export)
├── .env # Environment config
├── app.js # Server entry point
└── package.json # Dependencies and scripts

yaml
Copy
Edit

---

## 💻 Getting Started (for macOS)

### ✅ Prerequisites

- Node.js (v14+ recommended) – Install via [Homebrew](https://brew.sh/):  
  ```bash
  brew install node
MySQL Server – You can install it via Homebrew too:

bash
Copy
Edit
brew install mysql
## ⚙️ Setup Instructions
**1- Download the ZIP archive**
Download from the repo:
BC_Nanopore_Tracker.zip

Download from the repo:
BC_Nanopore_Tracker.zip

Unzip the project

bash
Copy
Edit
unzip BC_Nanopore_Tracker.zip
cd BC_Nanopore_Tracker
Install backend dependencies

bash
Copy
Edit
npm install
Install frontend dependency (PapaParse for CSV)

bash
Copy
Edit
cd frontend
npm install papaparse
cd ..
Set up .env file in the root directory
Create a .env file:

bash
Copy
Edit
touch .env
Paste the following content and update with your local credentials:

ini
Copy
Edit
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=labdatabase
PORT=8000
Set up MySQL database
Create the labdatabase and all necessary tables using your SQL schema.

🧪 Running the Application
Start the backend server:

bash
Copy
Edit
node app.js
Visit the backend at:
http://localhost:8000

📡 API Endpoints
Base URL: /api/data

Method	Endpoint	Description
GET	/:tableName	Fetch paginated table data
DELETE	/delete/:tableName/:id	Delete record (Admin only)
POST	/run	Add new run
POST	/experiment	Add new experiment
POST	/computer	Add new computer
POST	/minion	Add new minion
PUT	/:tableName/:id	Update record by ID

👥 Credits
Areej Fatima

Shabrina @Shabrina99

This project was created for educational purposes under the supervision of Brooklyn College’s Computer and Information Science Department.

.
