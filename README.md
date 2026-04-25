# 🗳️ Go App - Survey API (MongoDB + Docker)

A simple and clean REST API built with **Go (Golang)** that allows users to submit survey answers and stores them in **MongoDB**.  
The project is fully containerized using **Docker** and designed for learning backend + DevOps basics.

---

## 🚀 Features

- REST API using Gorilla Mux
- MongoDB integration using official Go driver
- Dockerized application
- Environment variable configuration
- Simple survey system (GET + POST)
- Lightweight and fast

---

## 🧰 Tech Stack

- Go 1.22
- MongoDB
- Gorilla Mux
- Docker

---

## 📁 Project Structure

go-app/
├── main.go
├── go.mod
├── go.sum
├── Dockerfile
├── README.md
├── .gitignore
├── handlers/
├── models/
├── database/
└── config/

---

## ⚙️ Environment Variables

| Variable     | Default Value              | Description              |
|--------------|---------------------------|--------------------------|
| SERVER_PORT  | 8080                      | Server port             |
| MONGO_URI    | mongodb://localhost:27017 | MongoDB connection URI  |

---

## ▶️ Run Locally

```bash
go mod tidy
go run main.go
```

---

## 🐳 Run with Docker

```bash id="docker1"
docker build -t go-app .
docker run -d --name go-mongo --network host go-app
```

---
## 🐳 Run with Docker Compose

### Start all services (App + MongoDB)

```bash
docker-compose up --build
## 📡 API Endpoints

### GET /

```bash id="get1"
GET http://localhost:8080/
```

Response:
```json id="res1"
"What is your favorite programming language?"
```

---

### POST /

```bash id="post1"
POST http://localhost:8080/
```

Request:
```json id="req1"
{
  "answer1": "Go",
  "answer2": "Python",
  "answer3": "Java"
}
```

Response:
```json id="res2"
"mongo_object_id"
```

---

## 🗄️ Database

- Database: `surveyDB`
- Collection: `answers`

Example document:

```json id="db1"
{
  "Answer1": "Go",
  "Answer2": "Python",
  "Answer3": "Java"
}
```

---

## 👨‍💻 Author

Built as a DevOps + Backend practice project using Go, MongoDB, and Docker.

---

## 📌 Future Improvements

- JWT Authentication
- Swagger documentation
- docker-compose (Mongo + App)
- Kubernetes deployment
- CI/CD pipeline (GitHub Actions)
# go-app
