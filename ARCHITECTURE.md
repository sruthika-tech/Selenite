# Selenite Architecture

Frontend (plain HTML/CSS/JS) → FastAPI REST API → SQLAlchemy → SQLite for local development / PostgreSQL for production.

Modules:
- Identity: registration, login, JWT, profile
- Career intelligence: careers, skills, tools, career relationships
- Learning: roadmaps, progress, skill profile, skill gap
- Opportunities: jobs, internships view, events/CTFs
- Intel: news + market trend data layer
- AI: grounded career assistant endpoint + resume skill-gap analyzer
- Deployment: Docker and Azure App Service reference

Production requirements before public launch:
- PostgreSQL + migrations
- HTTPS
- strong JWT secret stored in Azure Key Vault/App Settings
- restricted CORS
- rate limiting and audit logging
- approved job/news/event APIs or feeds
- privacy/retention policy for resumes
- automated tests and CI/CD
