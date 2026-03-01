🏬 Enterprise E-Commerce Management System

A full-featured Enterprise-Level E-Commerce Management System built using ASP.NET MVC with a strong focus on clean architecture, scalability, and professional backend engineering practices.

This project reflects real-world architectural thinking, advanced database handling, and hybrid data access strategies used in production systems.

🚀 Tech Stack

ASP.NET MVC

Entity Framework Core (ORM)

Dapper (Micro-ORM)

SQL Server

ASP.NET Identity

LINQ (Dynamic Querying)

AJAX + Partial Views

Bootstrap

🧠 Architecture Overview

The system follows a clean layered structure:

Presentation (MVC)
    ↓
Service Layer
    ↓
Repository Layer
    ↓
Data Access (EF Core + Dapper + SQL)
Patterns & Principles Applied

Repository Pattern (Generic + Custom)

Unit of Work

Service Layer Pattern

Dependency Injection

DTOs & ViewModels separation

Soft Delete with Global Query Filters

Explicit Transactions

Role-Based Authorization (RBAC)

SOLID Principles

🏗 Engineering Highlights
✅ Clean Separation of Concerns

Controllers handle HTTP only.

Business logic exists exclusively in Services.

Repositories handle data access only.

No DbContext usage inside controllers.

No business logic leakage across layers.

✅ Strong Architectural Discipline

Clear naming conventions.

Structured folder organization.

Enums instead of magic numbers.

Fluent API configurations.

Explicit transaction handling when coordinating Identity and domain logic.

Async/await across repositories and services.

✅ Hybrid Data Access Strategy

This project intentionally combines multiple data access approaches:

1️⃣ Entity Framework Core

Used for:

Standard CRUD

Change tracking

Relationships

Fluent API configurations

Owned entities

Inheritance mapping

2️⃣ Dapper (Micro-ORM)

Used for:

Performance-sensitive queries

Complex read projections

Optimized reporting queries

3️⃣ Advanced SQL Usage

CTE & Recursive CTE

Views

Functions

Triggers

Temp tables

Explicit SQL transactions

This reflects real enterprise systems where performance, flexibility, and control all matter.

📄 Pagination & Filtering System

Full Server-Side Pagination

State-based currentPage logic

Dynamic filtering

Dropdown changes auto-reset page to 1

Clean reusable pagination rendering

Consistent UI action buttons (Bootstrap small buttons)

🔐 Authentication & Authorization

ASP.NET Identity integration

Role-based authorization

Business-layer permission validation

Manual customer registration by authorized users

Coordinated transactions between Identity and business data

🛒 Order Lifecycle System

Structured workflow:

Cart

Checkout

Courier Assignment

Delivery Confirmation

Returns Handling

Status tracking using enums

Soft delete is applied with global query filters to preserve historical integrity.

📂 Project Structure (Simplified)
/Controllers
/Services
/Repositories
/Data
/Models
/DTOs
/ViewModels
/Helpers
/Enums

Clear separation between:

Domain models

View models

Data access

Business logic

🎨 Frontend Note

The frontend implementation focuses primarily on functionality and structure.

Some UI parts were developed with AI assistance to speed up layout and styling.

However, all frontend code was reviewed and fully understood.

The current focus of the project is backend architecture.

Frontend refinement and advanced UI structuring are part of the continuous learning roadmap.

This reflects a pragmatic engineering approach: prioritizing system architecture while continuously improving UI craftsmanship.

🛠 How To Run The Project

Ensure SQL Server is running.

Update the connection string if needed.

Run:

Update-Database

Then run the project normally.

The database will be created using EF Core migrations.

🎯 What This Project Demonstrates

Enterprise-level backend thinking.

Clean architecture discipline.

Hybrid ORM + Micro-ORM usage.

Advanced SQL knowledge.

Performance-aware design decisions.

Structured order lifecycle modeling.

Proper layering and maintainability focus.

📌 Purpose

This project serves as a professional backend architecture reference and portfolio project, demonstrating advanced ASP.NET MVC system design and database engineering practices.
