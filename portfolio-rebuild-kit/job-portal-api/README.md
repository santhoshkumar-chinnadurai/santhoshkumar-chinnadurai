# Job Portal REST API

A robust, enterprise-ready RESTful backend API for managing job listings, employer organizations, candidate profiles, and job applications. Built with **Java 21** and **Spring Boot 3.4**.

---

## 📌 Overview

The Job Portal API simplifies modern recruitment workflows by providing endpoints for employers to publish job listings, candidates to register and submit applications, and recruitment teams to track application statuses with pagination, sorting, and custom search filters.

---

## ✨ Features

- **Applicant Management**: Full CRUD operations for job seekers including resume tracking and profile search.
- **Employer Directory**: Registration and directory management for hiring organizations with website validation.
- **Job Listings Engine**: Job posting, categorization by job type (Full-time, Part-time, Remote, Contract), location, and salary ranges.
- **Application Tracking**: End-to-end application lifecycle tracking (`APPLIED`, `UNDER_REVIEW`, `ACCEPTED`, `REJECTED`).
- **Pagination & Filtering**: Built-in Spring Data `Pageable` support for high-performance querying across all listing endpoints.
- **Interactive Documentation**: Integrated Springdoc OpenAPI 3 (Swagger UI) for live API exploration and testing.
- **Automated Tests**: Unit and integration test coverage for controller and service layers (`JobListingControllerTest`, `JobApplicationTests`).

---

## 🛠️ Tech Stack

- **Language**: Java 21
- **Framework**: Spring Boot 3.4.4
- **Persistence**: Spring Data JPA / Hibernate
- **Database**: H2 In-Memory Database (MySQL compatible)
- **API Documentation**: Springdoc OpenAPI 2.3.0 / Swagger UI
- **Build Tool**: Apache Maven
- **Utilities**: Project Lombok

---

## 🏛️ Architecture

```
Client / Swagger UI / Postman
            │
            ▼
 ┌────────────────────────────────────────┐
 │       Spring Boot REST Controllers     │
 │  (Applicant, Employer, Job, Application)│
 └──────────────────┬─────────────────────┘
                    │
                    ▼
 ┌────────────────────────────────────────┐
 │       Service Interfaces & Impl        │
 │  (Business Logic & Exception Handling) │
 └──────────────────┬─────────────────────┘
                    │
                    ▼
 ┌────────────────────────────────────────┐
 │       Spring Data JPA Repositories     │
 │     (Custom JPQL Queries & Pageable)   │
 └──────────────────┬─────────────────────┘
                    │
                    ▼
 ┌────────────────────────────────────────┐
 │           H2 / MySQL Database          │
 └────────────────────────────────────────┘
```

---

## 📖 API Documentation & Swagger UI

When the application is running, access the interactive Swagger UI at:  
👉 **`http://localhost:8080/swagger-ui/index.html`**

OpenAPI JSON specification available at:  
👉 **`http://localhost:8080/v3/api-docs`**

### Key REST Endpoints

#### 💼 Job Listings (`/api/jobs`)
| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/jobs` | Retrieve paginated job listings (`page`, `size`, `sort`) |
| `GET` | `/api/jobs/{id}` | Get job listing by ID |
| `POST` | `/api/jobs` | Create a new job listing |
| `PUT` | `/api/jobs/{id}` | Update an existing job listing |
| `DELETE` | `/api/jobs/{id}` | Delete a job listing |
| `GET` | `/api/jobs/search/title?title={title}` | Search job listings by title keyword |
| `GET` | `/api/jobs/search/location?location={loc}` | Filter jobs by geographical location |
| `GET` | `/api/jobs/search/salary?minSalary={min}&maxSalary={max}` | Filter jobs within a salary range |
| `GET` | `/api/jobs/search/jobType?jobType={type}` | Filter by job type (`FULL_TIME`, `REMOTE`) |

#### 📄 Applications (`/api/applications`)
| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/applications` | Retrieve all submitted applications |
| `POST` | `/api/applications` | Submit a candidate application for a job |
| `GET` | `/api/applications/{id}` | Get application details by ID |
| `GET` | `/api/applications/status/{status}` | Filter applications by review status |
| `GET` | `/api/applications/job/{jobId}` | Get all applications for a specific job |
| `GET` | `/api/applications/applicant/{applicantId}` | Get all applications submitted by an applicant |

#### 👤 Applicants (`/api/applicants`)
| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/api/applicants` | Register a new job seeker |
| `GET` | `/api/applicants` | Get all registered applicants (paginated) |
| `GET` | `/api/applicants/{id}` | Get applicant profile |
| `GET` | `/api/applicants/search/email?email={email}` | Find applicant by email |

#### 🏢 Employers (`/api/employers`)
| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/api/employers` | Register a hiring company |
| `GET` | `/api/employers` | Get all employers (paginated) |
| `GET` | `/api/employers/{id}` | Get employer profile |
| `GET` | `/api/employers/search/company?companyName={name}` | Find employer by company name |

---

## 💻 Installation & Local Setup

### Prerequisites
- **JDK 21** or higher
- **Maven 3.9+** (or use included `./mvnw`)

### 1. Clone & Build
```bash
git clone https://github.com/santhoshkumar-chinnadurai/job-portal-api.git
cd job-portal-api
```

### 2. Run the Application
```bash
./mvnw clean spring-boot:run
```

The server starts on port `8080`.

### 3. Access H2 In-Memory Database Console
- **URL**: `http://localhost:8080/h2-console`
- **JDBC URL**: `jdbc:h2:mem:jobdb`
- **Username**: `sa`
- **Password**: `password`

---

## 🧪 Running Automated Tests

```bash
./mvnw test
```

---

## 📁 Project Structure

```
job-portal-api/
├── src/
│   ├── main/
│   │   ├── java/com/example/job/
│   │   │   ├── config/             # Swagger & OpenAPI Config
│   │   │   ├── Controller/         # REST Controllers
│   │   │   ├── Entity/             # JPA Entities (Applicant, Employer, Job, Application)
│   │   │   ├── Exception/          # ResourceNotFoundException & Global Handlers
│   │   │   ├── Repository/         # Spring Data JPA Repositories (JPQL queries)
│   │   │   ├── Service/            # Service Interfaces & Implementations
│   │   │   └── JobApplication.java # Application Main Entry Point
│   │   └── resources/
│   │       └── application.properties # Server & H2 Database Configuration
│   └── test/
│       └── java/com/example/job/   # Unit & Integration Tests
├── pom.xml
└── README.md
```

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

## 👨‍💻 Author

**Santhoshkumar Chinnadurai**  
- **GitHub**: [@santhoshkumar-chinnadurai](https://github.com/santhoshkumar-chinnadurai)  
- **LinkedIn**: [santhoshkumar-chinnadurai](https://www.linkedin.com/in/santhoshkumar-chinnadurai-4b8034344)  
- **Email**: [santhosh2001ramesh@gmail.com](mailto:santhosh2001ramesh@gmail.com)
