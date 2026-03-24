# Docker PostgreSQL Setup

## 📌 Overview

This project sets up a PostgreSQL database using Docker Compose with environment variables and persistent storage.

---

## ⚙️ Prerequisites

* Docker Desktop installed
* DBeaver (DB client)

---

## 📁 Project Structure

* docker-compose.yaml → Defines PostgreSQL container
* .env → Stores database credentials
* README.md → Instructions

---

## 🔐 Environment Variables (.env)

```
POSTGRES_USER=myuser
POSTGRES_PASSWORD=mypassword
POSTGRES_DB=mydb
POSTGRES_PORT=5432
```

---

## 🚀 How to Run

1. Navigate to project folder:

```
cd docker-postgres-setup
```

2. Start container:

```
docker-compose up -d
```

3. Stop container:

```
docker-compose down
```

---

## 🔗 Database Connection Details

* Host: localhost
* Port: 5432
* Database: mydb
* Username: myuser
* Password: mypassword

---

## 💾 Data Persistence

Docker volume is used to persist data:

* Volume: postgres_data
* Ensures data is not lost after container restart

---

## 🧪 Verification

Run SQL query:

```
SELECT 1;
```

Create table:

```
CREATE TABLE test_table (
    id SERIAL PRIMARY KEY,
    name TEXT
);
```

Insert data:

```
INSERT INTO test_table (name) VALUES ('hello');
```

---

## 🧠 Key Learnings

* Docker containerization
* Docker Compose usage
* Environment variable management
* Port mapping
* Persistent storage using volumes
* Connecting database using DBeaver

---
## Merge Request Update
Added Docker Compose setup with volume and environment configuration.
