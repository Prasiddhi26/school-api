# 🏫 School Management API

A Node.js + Express.js + MySQL backend project that allows users to add schools and retrieve a list of schools sorted by proximity based on user location.

---
## 🌍 Live API

Base URL:

https://your-render-url.onrender.com
Endpoints:

➕ Add School (POST)

POST /addSchool

📍 List Schools (GET)

GET /listSchools?latitude=19.1&longitude=72.9

---
## 🚀 Features

- Add new school with name, address, latitude, longitude
- Get list of schools sorted by nearest distance
- Distance calculated using Haversine formula
- Input validation for all fields
- REST API using Express.js

---

## 🛠️ Tech Stack

- Node.js
- Express.js
- MySQL
- dotenv
- mysql2

---



## ⚙️ Setup Instructions

### 1. Clone repository

```bash
git clone https://github.com/Prasiddhi26/school-api.git
cd school-api
```

### 2. Install dependencies
```bash
npm install
```

### 3. Setup .env file
Create a .env file in root directory:

```env
PORT=5000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=school_db
```

### 4. MySql setup
Run the following commands in MySQL Workbench or terminal:

```
CREATE DATABASE school_db;
USE school_db;
CREATE TABLE schools (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(255) NOT NULL,
  address VARCHAR(255) NOT NULL,
  latitude FLOAT NOT NULL,
  longitude FLOAT NOT NULL
);
```

### 5. Run project
``` bash
node server.js
```

## 📌 API Endpoints
### ➕ Add School

POST /addSchool

#### Request Body:
``` json
{
  "name": "ABC School",
  "address": "Mumbai",
  "latitude": 19.0760,
  "longitude": 72.8777
}
```
#### Response:
``` json
{
  "message": "School added successfully"
}
``` 
### 📍 List Schools (Sorted by Distance)

GET /listSchools?latitude=19.1&longitude=72.9
``` json
[
  {
    "id": 1,
    "name": "ABC School",
    "address": "Mumbai",
    "latitude": 19.076,
    "longitude": 72.8777,
    "distance": 2.5
  }
]
```
---
### 📬 Postman Collection

You can find the Postman collection in this repo:
``` bash
/postman/school-api.postman_collection.json
```


--- 
### 👨‍💻 Author
 Prasiddhi Shetty