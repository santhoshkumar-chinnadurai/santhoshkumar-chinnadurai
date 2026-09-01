# CrowdFunding Platform

A full-stack, secure crowdfunding and campaign management platform built with **Java 21**, **Spring Boot 3**, **Spring Security (JWT)**, **React**, and **Tailwind CSS**.

---

## 📌 Overview

The CrowdFunding Platform enables creators to launch fundraising initiatives, receive financial contributions, track digital wallets, and interact with supporters via threaded discussions. The application uses a stateless JWT authentication model with decoupled React SPA client architecture.

---

## ✨ Features

- **Stateless JWT Security**: Secure user registration, authentication, password reset, and role-based route authorization.
- **Campaign Lifecycle Engine**: Create, update, and monitor campaigns with goal targets, current funding tallies, and categories.
- **Donation Processing**: Real-time donation workflow linked with contributor histories and wallet balances.
- **Digital Wallet Management**: Wallet balance tracking and transaction management for donors and project creators.
- **Community Commenting & Media**: Threaded discussions on campaign pages with media attachment support.
- **Responsive Modern UI**: Built with React, Vite, Tailwind CSS, Lucide icons, and Axios HTTP client.
- **Containerized Deployment**: Ready for multi-environment deployments via Docker and Render blueprint.

---

## 🛠️ Tech Stack

### Backend
- **Language**: Java 21
- **Framework**: Spring Boot 3
- **Security**: Spring Security, JJWT (JSON Web Token)
- **Data Persistence**: Spring Data JPA / Hibernate
- **Database**: H2 In-Memory (Dev) / MySQL (Prod)
- **Build Tool**: Maven

### Frontend
- **Framework**: React 19
- **Build Tool**: Vite
- **Styling**: Tailwind CSS
- **HTTP Client**: Axios
- **Icons**: Lucide React

---

## 🏛️ Architecture

```
 ┌─────────────────────────────────────────────────────────┐
 │               React Frontend (SPA Client)               │
 └────────────────────────────┬────────────────────────────┘
                              │
                              │ (HTTPS / REST + JWT Token)
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │            Spring Security Filter Chain                 │
 │            (JwtAuthenticationFilter)                    │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │             Spring Boot REST API Layer                  │
 │ (Auth, Campaign, Donation, Wallet, Comment Controllers) │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │           Service Layer & DTO Validation                │
 │       (CampaignService, DonationService, etc.)          │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │               Spring Data JPA Repositories              │
 └────────────────────────────┬────────────────────────────┘
                              │
                              ▼
 ┌─────────────────────────────────────────────────────────┐
 │                   H2 / MySQL Database                   │
 └─────────────────────────────────────────────────────────┘
```

---

## 💻 Installation & Setup

### Prerequisites
- JDK 21+
- Node.js v18+
- Maven 3.9+

### 1. Backend Setup
```bash
# Navigate to backend directory
cd demo

# Run with Maven wrapper
./mvnw clean spring-boot:run
```
Backend runs at `http://localhost:8080`.

### 2. Frontend Setup
```bash
# Navigate to frontend directory
cd Frontend

# Install dependencies
npm install

# Start development server
npm run dev
```
Frontend runs at `http://localhost:5173`.

---

## 🔐 Environment Variables

Create `.env` inside the `Frontend/` folder:
```env
VITE_API_BASE_URL=http://localhost:8080/api
```

---

## 📄 License

This project is open-source under the [MIT License](LICENSE).

---

## 👨‍💻 Author

**Santhoshkumar Chinnadurai**  
- **GitHub**: [@santhoshkumar-chinnadurai](https://github.com/santhoshkumar-chinnadurai)  
- **LinkedIn**: [santhoshkumar-chinnadurai](https://www.linkedin.com/in/santhoshkumar-chinnadurai-4b8034344)
