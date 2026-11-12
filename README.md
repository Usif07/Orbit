# Orbit

Orbit is a shipment operations platform. This repository follows the Orbit SRS v2: one ASP.NET Core backend, two Flutter mobile apps, an Angular operations dashboard, a public tracking page, and a Python OR-Tools optimizer service.

## Repository layout

- `backend/` - ASP.NET Core (.NET 10) modular monolith and EF Core data access for SQL Server.
- `merchant_app/` - Flutter app for merchants.
- `courier_app/` - offline-capable Flutter app for couriers, using local SQLite.
- `dashboard/` - Angular operations dashboard; live updates use SignalR.
- `tracking_page/` - public, no-login tracking page opened through the emailed tracking link.
- `optimizer/` - Python OR-Tools route optimizer called by the backend.
- `docs/` - shared decisions and project documentation.

The SRS requires a cache for the latest courier location. The team plans Redis for this cache; no location history belongs in the main database.

## Getting started

This is the initial repository skeleton. Add component-specific setup commands to each component README as its first runnable slice is agreed.

## Team workflow

Read [CONTRIBUTING.md](CONTRIBUTING.md) before creating a branch or opening a pull request.
