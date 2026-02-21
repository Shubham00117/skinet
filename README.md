# 🛍️ Skinet — E-Commerce Application

A full-stack **e-commerce application** built with **Clean Architecture** using **.NET** on the backend and **Angular** on the frontend. Features a layered architecture with Core, Infrastructure, and API projects.

---

## 📖 Overview

Skinet is a modern e-commerce platform following Clean Architecture / Onion Architecture principles. It demonstrates building a production-grade .NET application with proper separation of concerns, repository pattern, specification pattern, and a full Angular client.

---

## 📂 Project Structure

```
skinet/
├── skinet.sln                          # .NET Solution
├── docker-compose.yml                  # Docker services
├── API/                                # Presentation layer
│   ├── Controllers/                    # API endpoints
│   ├── DTOs/                           # Data Transfer Objects
│   ├── Errors/                         # Error handling
│   ├── Extensions/                     # Service extensions
│   ├── Middleware/                      # Custom middleware
│   ├── RequestHelpers/                 # Pagination, sorting
│   ├── SignalR/                        # Real-time notifications
│   └── Program.cs
├── Core/                               # Domain layer
│   ├── Entities/                       # Domain entities
│   ├── Interfaces/                     # Repository contracts
│   └── Specifications/                 # Specification pattern
├── Infrastructure/                     # Data access layer
│   ├── Config/                         # EF Core configurations
│   ├── Data/                           # DbContext & seed data
│   ├── Migrations/                     # Database migrations
│   └── Services/                       # External service integrations
└── client/                             # Angular frontend
    ├── angular.json
    ├── tailwind.config.js
    ├── package.json
    └── src/                            # Angular source code
```

---

## 🏗️ Architecture

```
┌─────────────┐
│   Angular    │  ← Frontend (client/)
│   Client     │
└──────┬───────┘
       │ HTTP
┌──────▼───────┐
│   API Layer  │  ← Controllers, DTOs, Middleware
└──────┬───────┘
       │
┌──────▼───────┐
│  Core Layer  │  ← Entities, Interfaces, Specifications
└──────┬───────┘
       │
┌──────▼───────┐
│Infrastructure│  ← EF Core, Data, Services
└──────────────┘
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Backend** | .NET, C#, ASP.NET Core |
| **Frontend** | Angular, TypeScript, TailwindCSS |
| **Database** | SQL (via EF Core) |
| **Real-time** | SignalR |
| **DevOps** | Docker Compose |
| **Architecture** | Clean Architecture / Specification Pattern |

---

## 🚀 Getting Started

### Prerequisites
- .NET 8 SDK
- Node.js 18+
- Docker (optional)

### Running with Docker
```bash
docker-compose up -d
```

### Running Manually
```bash
# Backend
cd API
dotnet restore
dotnet run

# Frontend
cd client
npm install
ng serve
```

---

## 📜 License

This project is open source and available for educational purposes.
