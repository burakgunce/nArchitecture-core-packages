# nArchitecture Core Packages

This is a core packages solution implementing **Clean Architecture** principles with various **cross-cutting concerns** for enterprise-level .NET applications. It provides reusable components and implementations to help build scalable, maintainable, and secure backend systems.

---

## 📐 Architecture & Patterns

### 1. Clean Architecture

A layered structure with clear separation of concerns, including:

- **Core.Application** – Application-level logic and use cases  
- **Core.Persistence** – Data access and database-related infrastructure  
- **Core.Security** – Security and authentication modules  
- **Core.CrossCuttingConcerns** – Logging, caching, transaction management, etc.

### 2. Design Patterns

- **Repository Pattern**  
  - `IRepository<T>` – Generic repository interface  
  - `IAsyncRepository<T>` – Async repository abstraction  
  - `EfRepositoryBase` – Entity Framework Core implementation  

- **Unit of Work Pattern**  
  - Transaction management and context lifetime handling  

- **CQRS Pattern** (Command Query Responsibility Segregation)  
  - Separate command and query operations  
  - Implemented using MediatR  

- **Mediator Pattern**  
  - MediatR used for decoupling request/response communication  
  - Integrated with pipeline behaviors  

- **Pipeline Pattern**  
  - Pipeline behaviors for:  
    - Validation  
    - Caching  
    - Logging  
    - Transaction Management  

---

## ⚙️ Cross-Cutting Concerns

### ✅ Caching

- Distributed caching infrastructure  
- Cache key management and invalidation  
- Sliding expiration configuration  

### 🛡️ Security

- **JWT (JSON Web Token)** authentication  
- **OTP (One-Time Password)** authentication  
- Email-based authentication support  
- Secure password handling  

### 📄 Logging

- Integrated **Serilog** logging  
- Support for multiple logging targets:  
  - File logging  
  - SQL Server logging  
- Customizable log levels and output formats  

### 🔁 Transaction Management

- Ensures atomic operations across database and services  
- Automatic rollback on failure  

---

## 🧰 Technologies & Libraries

### Core Dependencies

- **.NET 7.0** – Target framework  
- **Entity Framework Core** – Database ORM  
- **MediatR (v12.4.1)** – For mediator pattern implementation  
- **FluentValidation (v11.11.0)** – For model and request validation  
- **Serilog** – Structured logging  
- **Microsoft.Extensions.Configuration** – App configuration handling  

### Security Packages

- **System.IdentityModel.Tokens.Jwt (v7.7.1)** – JWT token operations  
- **Microsoft.IdentityModel.Tokens (v7.7.1)** – Token generation and validation  
- **Otp.NET (v1.4.0)** – OTP authentication handling  

---

## 🌟 Key Features

### 1. Dynamic Query Support

- Build flexible queries at runtime  
- Supports dynamic filtering, sorting, and pagination  

### 2. Entity Management

- Base entity includes creation/update timestamps  
- Soft delete implementation  
- Audit trail support  

### 3. Advanced Repository Features

- Fully async repository operations  
- **Specification pattern** support  
- Eager loading with Include expressions  
- Dynamic query building capabilities  

### 4. Security Features

- JWT token generation and validation  
- OTP-based authentication  
- Secure password hashing and verification  

### 5. Caching Infrastructure

- Distributed caching support  
- Custom cache keys and bypass strategies  
- Sliding expiration support  

### 6. Logging Infrastructure

- Structured logs using Serilog  
- File and SQL logging support  
- Customizable logging pipeline  

---

## ✅ Conclusion

**nArchitecture Core Packages** delivers a solid, reusable foundation for enterprise-grade .NET applications. It combines clean architectural practices with modern tools and patterns to help developers build secure, maintainable, and scalable systems with minimal friction.

---
