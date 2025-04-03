# 🌍 TravelSmile – Full Stack Travel Booking App

TravelSmile is a full-stack web application built with Angular and Spring Boot. It is fully containerized using Docker and Docker Compose for easy local development and deployment.

---

## 📦 Tech Stack

| Layer       | Technology         |
|-------------|--------------------|
| Frontend    | Angular 19 (SPA)   |
| Backend     | Spring Boot + JWT  |
| Database    | H2 (in-memory)     |
| Containers  | Docker + NGINX     |
| Orchestration | Docker Compose  |

---


---

## ⚙️ Prerequisites

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- [Java 17+](https://adoptium.net/)
- [Node.js 18 or 20+](https://nodejs.org/)
- [Maven](https://maven.apache.org/)

---

## 🚀 Getting Started

### 1. Build Angular App (Browser Folder)

In the frontend directory:

```bash
cd travel-smile-frontend
npm install
ng build --configuration=production

cd ../TravelSmile
mvn clean package -DskipTests

docker-compose down -v
docker-compose up --build

🌐 Access the App
Service	URL
Frontend	http://localhost:4200
Backend API	http://localhost:8086/travel-smile/api/swagger-ui/index.html#/
H2 Console	http://localhost:8086/travel-smile/api/h2-console

