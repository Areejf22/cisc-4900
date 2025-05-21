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

```
BC_Nanopore_Tracker/
├── controllers/
│   └── dbController.js       # DB operations  
├── middlewares/
│   └── validateTable.js      # Table name validation  
├── models/
│   ├── db.js                 # MySQL connection  
│   └── tableModel.js         # Query logic  
├── routes/
│   └── dataRoutes.js         # API endpoints  
├── frontend/                 # Frontend files (CSV import/export)  
├── .env                      # Environment config  
├── app.js                    # Server entry point  
└── package.json              # Dependencies and scripts  
```
---

## 💻 Getting Started (for macOS)

### ✅ Prerequisites

- Node.js (v14+ recommended) – Install via [Homebrew](https://brew.sh/):  
  ```bash
  brew install node
- MySQL Server – You can install it via Homebrew too:

brew install mysql
## ⚙️ Setup Instructions

**1- Download the ZIP archive**

Download from the repo:

BC_Nanopore_Tracker.zip

**2- Unzip the project**

unzip BC_Nanopore_Tracker.zip

cd BC_Nanopore_Tracker

**3-Install backend dependencies**

npm install

**4-Install frontend dependency (PapaParse for CSV)**

cd frontend
npm install papaparse
cd ..


**5-Set up .env file in the root directory**

Create a .env file:

touch .env

Paste the following content and update with your local credentials:

```
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=labdatabase
PORT=8000
```

**6-Set up MySQL database**

Create the labdatabase and all necessary tables using your SQL schema.

## 🧪 Running the Application

Start the backend server:

node app.js

Visit the backend at:

http://localhost:8000

## 📡 API Endpoints

**Base URL:** `/api/data`

| Method | Endpoint                  | Description                 |
|--------|---------------------------|-----------------------------|
| GET    | `/:tableName`             | Fetch paginated table data |
| DELETE | `/delete/:tableName/:id`  | Delete record (Admin only) |
| POST   | `/run`                    | Add new run                 |
| POST   | `/experiment`             | Add new experiment          |
| POST   | `/computer`               | Add new computer            |
| POST   | `/minion`                 | Add new minion              |
| PUT    | `/:tableName/:id`         | Update record by ID         |

## 👥 Credits
Areej Fatima

Shabrina (https://github.com/Shabrina99)

This project was created for educational purposes under the supervision of Brooklyn College’s Computer and Information Science Department.

## 🔒 License
This project is for academic/research use only and may be extended for open-source contribution in future iterations.

.
