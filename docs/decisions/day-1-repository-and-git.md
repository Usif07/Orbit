# Day 1: repository and Git workflow

## Confirmed from Orbit SRS v2 and Data Requirements

- One backend API, two mobile apps, one web dashboard, and a public tracking page.
- Backend: ASP.NET Core (.NET 10), modular monolith, EF Core, SQL Server.
- Merchant and courier apps: Flutter; courier app also uses local SQLite for offline work.
- Operations dashboard: Angular with SignalR for live updates.
- Route optimizer: a Python service using OR-Tools.
- CourierLocation is a latest-position cache; do not persist a GPS history.
- The data model is grouped into five business modules. Keep module boundaries clear inside the backend.

## Repository and Git decisions

- Use one monorepo with separate top-level component folders.
- `main` is the stable shared branch; no direct pushes.
- Work on short-lived `feature/*`, `fix/*`, or `docs/*` branches.
- Merge pull requests after at least one teammate approval and required checks pass.
- Use squash merge.

## Open setup decisions

- The initial scaffold keeps the public tracking page in its own `tracking_page/` folder; confirm this placement with the team before implementation.
- Name module folders to match the team's agreed domain boundaries before creating backend projects.
- Confirm the GitHub organization, repository visibility, component owners, and backup reviewers.
- Enable branch protection in GitHub after the remote repository is created. Local files cannot enforce remote branch rules.

