# 🏬 Enterprise E-Commerce Management System

A production-oriented **Enterprise-Level E-Commerce Management System** built with ASP.NET MVC.

This project focuses on backend architecture discipline, scalable system design, and hybrid data access strategies that reflect real-world enterprise practices.

---

## 🚀 Tech Stack

- ASP.NET MVC
- Entity Framework Core (ORM)
- Dapper (Micro-ORM)
- SQL Server
- ASP.NET Identity
- LINQ (Dynamic Querying)
- AJAX + Partial Views
- Bootstrap

---

# 🧠 Architecture Overview

The system follows a clean layered architecture:

```
Presentation (MVC)
    ↓
Service Layer
    ↓
Repository Layer
    ↓
Data Access (EF Core + Dapper + SQL)
```

## Implemented Patterns

- Repository Pattern (Generic + Custom)
- Unit of Work
- Service Layer Pattern
- Dependency Injection
- DTOs & ViewModels Separation
- Soft Delete with Global Query Filters
- Explicit Transactions
- Role-Based Authorization (RBAC)
- SOLID Principles

---

# 🏗 Engineering Discipline

## Clean Separation of Responsibilities

- Controllers handle HTTP concerns only.
- Business logic exists exclusively inside Services.
- Repositories are responsible only for data access.
- No direct DbContext usage inside controllers.
- No business logic leakage across layers.

## Maintainability & Code Quality

- Clear and descriptive naming conventions.
- Strong typing using enums (no magic numbers).
- Fluent API configurations for relationships and constraints.
- Structured folder organization.
- Async/await implemented across services and repositories.
- Explicit transaction handling when coordinating Identity and domain operations.

---

# 🗄 Hybrid Data Access Strategy

This project intentionally combines multiple data access approaches.

## 1️⃣ Entity Framework Core (ORM)

Used for:
- Standard CRUD operations
- Change tracking
- Navigation properties & relationships
- Fluent API configurations
- Owned entities
- Inheritance mapping

## 2️⃣ Dapper (Micro-ORM)

Used for:
- Performance-sensitive queries
- Complex read projections
- Optimized reporting scenarios

## 3️⃣ Advanced SQL

Used when full control or performance tuning is required:

- CTE & Recursive CTE
- Views
- Functions
- Triggers
- Temp tables
- Explicit SQL transactions

This hybrid approach reflects realistic enterprise systems where abstraction and control must coexist.

---

# 📄 Pagination & Filtering System

- Fully implemented Server-Side Pagination
- State-based `currentPage` management
- Dynamic filtering using LINQ
- Dropdown changes auto-reset page to 1
- Reusable pagination rendering logic
- Consistent Bootstrap small action buttons (Edit / Manage)

---

# 🔐 Authentication & Authorization

- ASP.NET Identity integration
- Role-based access control
- Business-layer permission validation
- Manual customer registration by authorized users
- Transaction coordination between Identity and business data

---

# 🛒 Order Lifecycle Design

Structured and modeled to reflect real systems:

1. Cart creation
2. Checkout process
3. Courier assignment
4. Delivery confirmation
5. Returns handling
6. Status tracking via enums

Soft delete is implemented using global query filters to preserve data history.

---

# 📂 Simplified Project Structure

```
/Controllers
/Services
/Repositories
/Data
/Models
/DTOs
/ViewModels
/Helpers
/Enums
```

Clear separation between:
- Domain models
- View models
- Business logic
- Data access layer

---

# 🎨 Frontend Note

The primary focus of this project is backend architecture and system design.

Some UI components were implemented with AI assistance to accelerate layout and styling.  
However:

- All generated code was reviewed and fully understood.
- No code was blindly integrated.
- Backend architecture and system behavior were designed and implemented manually.

Frontend refinement and advanced UI structuring remain part of the continuous learning roadmap.

This reflects a pragmatic engineering approach: prioritizing architecture while steadily improving UI craftsmanship.

---

# 🛠 How To Run The Project

1. Ensure SQL Server is running.
2. Update the connection string if necessary.
3. Run the following command:

```
Update-Database
```

4. Start the application.

The database will be created automatically via EF Core migrations.

---

# 🎯 What This Project Demonstrates

- Enterprise-level backend thinking
- Clean architecture discipline
- Hybrid ORM + Micro-ORM usage
- Advanced SQL knowledge
- Performance-aware design decisions
- Structured order lifecycle modeling
- Maintainable and scalable codebase design

---

# 📌 Purpose

This project serves as a professional backend architecture reference and portfolio project, demonstrating advanced ASP.NET MVC system design and database engineering practices.
