# 🌙 SELENITE — Complete Career Intelligence OS

A full local MVP for cybersecurity career intelligence: careers, skills, tools, roadmaps, progress, jobs, internships, events/CTFs, cyber news, market intel, AI career guidance and resume analysis.

## 1. Start backend (Windows)
Open this folder in VS Code, then:

```powershell
cd backend
python -m venv .venv
.venv\\Scripts\\activate
pip install -r requirements.txt
uvicorn app.main:app --reload
```

Open `http://127.0.0.1:8000/docs`.

## 2. Start frontend
Install the VS Code **Live Server** extension. Open `frontend/index.html` with Live Server.

The frontend defaults to `http://127.0.0.1:8000`. If your API is elsewhere, use Settings inside Selenite and change the API endpoint.

## 3. What works now
- Account registration/login with password hashing + JWT
- Dashboard and profile
- Career explorer + career details
- Skill explorer + user skill tracking
- Tool explorer
- Roadmap engine + synced progress
- Skill-gap calculation
- Jobs and internship UI backed by API data layer
- Hackathons/CTFs events module
- Cyber news module + RSS refresh endpoint
- Market Intel with transparent source/sample metadata
- CyberCareer AI grounded MVP
- Resume analyzer with skill-gap/project suggestions
- SQLite local database seeded automatically
- Docker + Azure deployment references
- OpenAPI/Swagger docs

## 4. Important production data note
The package includes clearly labelled demo job/event/news/market records so the UI works immediately. Do not present those demo records as real current opportunities. Before public launch, connect approved live sources and preserve the original listing/source URL, date, geography and sample size.

## 5. News refresh
Set `NEWS_RSS_URLS` in `.env` to permitted RSS feeds, then call `POST /api/admin/news/refresh` from the API docs.

## 6. Production database
Use PostgreSQL by setting `DATABASE_URL` to a PostgreSQL SQLAlchemy URL and installing the matching PostgreSQL driver. Add migrations before production deployment.

## 7. Resume privacy
Resumes can contain personal information. Do not store or process them in production without an explicit privacy/retention design and appropriate access controls.
