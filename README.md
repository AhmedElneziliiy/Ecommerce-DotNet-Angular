# E-Commerce API — .NET Clean Architecture

A **RESTful e-commerce API** built with ASP.NET Core following **Clean Architecture** principles — featuring product and category management designed to pair with an Angular frontend.

## Tech Stack

- **ASP.NET Core Web API** (.NET 8)
- **Entity Framework Core** — Code-First with SQL Server
- **Clean Architecture** — API / Core / Infrastructure layers
- **Repository Pattern + Unit of Work**
- **Swagger / OpenAPI**

## Project Structure

| Layer | Project | Responsibility |
|---|---|---|
| API | `Ecom.API` | Controllers, routing, Swagger |
| Core | `Ecom.Core` | Entities, interfaces, DTOs |
| Infrastructure | `Ecom.Infrastructure` | EF Core DbContext, migrations, repositories |

## Key Features

- Product catalog with categories and photos
- Generic repository with Unit of Work pattern
- EF Core Fluent API configuration per entity
- DTO pattern for clean data contracts
- Seed data via migrations

## Getting Started

1. Set your connection string in `appsettings.json`.
2. Apply migrations: `dotnet ef database update --project Ecom.Infrastructure --startup-project Ecom.API`
3. Run: `dotnet run --project Ecom.API`
