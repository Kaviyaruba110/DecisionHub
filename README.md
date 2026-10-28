# DecisionHub 🗳️
> **Collaborative Decision-Making & Community Polling Platform**  
> *Developed as part of Infosys Springboard Virtual Internship 7.0*

DecisionHub is a modern full-stack web application designed for structured group decision-making, consensus building, and community polling. It combines multi-criteria decision models, interactive voting mechanisms, threaded discussions, community moderation, and real-time analytics into a unified platform.

---

## 🚀 Key Features

### 1. 👥 Role-Based Access Control (RBAC)
* **User:** Create public/community decisions, cast votes, post comments, join communities, and view personal stats.
* **Moderator:** Community-scoped moderation — manage members, review reported content, pin priority polls, and lock threads.
* **Platform Admin:** Platform-wide oversight — view system analytics, manage all users/communities, and moderate reported content.

### 2. 📊 Multi-Mechanism Decision & Voting
* **Decision Types:** Public decisions (accessible platform-wide) and Community decisions (scoped to members).
* **Voting Models:** 
  * Single-Choice Voting
  * Multiple-Choice Voting
  * Rating & Factor-Based Comparison Scoring
* **Lifecycle Management:** `DRAFT` ➔ `ACTIVE` ➔ `CLOSED` with automated deadline enforcement.

### 3. 🏢 Community Collaboration & Moderation
* Public and Private communities with membership approval workflows.
* Threaded discussions and replies attached to each decision.
* Content moderation: Reporting inappropriate comments, auto-routing alerts to admins.

### 4. 🔔 Real-Time Notification Center
* Live unread notification badge on the navigation bar.
* 30-second automated background polling.
* Paginated Notification Center with "All" and "Unread" tabs and single/bulk actions.

### 5. 📈 Comprehensive Analytics Dashboard
* **Decision Analytics:** Real-time vote distributions, candidate rankings, and option popularity.
* **Community Analytics:** Member growth, activity rate, and engagement.
* **Platform Analytics (Admin):** Total users, active polls, participation rates, and discussion metrics.

---

## 🛠️ Technology Stack

| Layer | Technology |
| :--- | :--- |
| **Frontend** | React 18, Vite, React Router v6, Axios, React Icons, Vanilla CSS |
| **Backend** | Java 21, Spring Boot 3, Spring Security 6, JWT, Spring Data JPA, Hibernate, MapStruct, Lombok |
| **Database** | PostgreSQL |
| **Build Tools** | Maven, npm |
| **API Testing** | Postman / Swagger Open-API |

---

## 🏗️ System Architecture

```text
               ┌────────────────────────┐
               │   React Frontend (SPA) │
               │     Vite + Axios       │
               └───────────┬────────────┘
                           │ HTTP / REST (JWT)
               ┌───────────▼────────────┐
               │   Controller Layer     │
               │  (Spring Boot REST)    │
               └───────────┬────────────┘
                           │ DTOs
               ┌───────────▼────────────┐
               │    Service Layer       │
               │    (Business Logic)    │
               └───────────┬────────────┘
                           │
               ┌───────────▼────────────┐
               │   Repository Layer     │
               │   (Spring Data JPA)    │
               └───────────┬────────────┘
                           │ Hibernate ORM
               ┌───────────▼────────────┐
               │   PostgreSQL Database  │
               └────────────────────────┘
```

---

## ⚡ Getting Started

### Prerequisites
* **Java:** JDK 21+
* **Node.js:** v18+ & npm
* **Database:** PostgreSQL (running locally or remotely)
* **Maven:** 3.8+

---

### Backend Setup
1. Navigate to the backend directory:
   ```bash
   cd backend
   ```
2. Configure database credentials in `src/main/resources/application.properties`:
   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/decisionhub
   spring.datasource.username=postgres
   spring.datasource.password=your_password
   ```
3. Build and run the Spring Boot application:
   ```bash
   mvn clean install -DskipTests
   mvn spring-boot:run
   ```
   *The backend will start at `http://localhost:8080`.*

---

### Frontend Setup
1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Launch the development server:
   ```bash
   npm run dev
   ```
   *The frontend will run at `http://localhost:5173`.*

---

## 📄 License
This project was developed for educational and portfolio purposes as part of the Infosys Springboard Internship program.
