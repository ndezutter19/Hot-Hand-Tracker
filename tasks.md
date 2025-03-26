# 🏀 NBA Hot Hand Tracker – Project Tasks

## ✅ Phase 1: Project Setup
- [x] Initialize GitHub repo and WSL project
- [x] Set up Git + SSH
- [x] Create tasks.md for tracking
- [ ] Set up project folder structure (`backend/`, `frontend/`, `scripts/`)
- [ ] Initialize backend FastAPI app
- [ ] Initialize frontend Next.js app

---

## 🔁 Phase 2: Data Pipeline
- [ ] Install and test `nba_api` Python package
- [ ] Write script to pull game logs (last X games per player)
- [ ] Store pulled data into PostgreSQL (game stats, players, teams)
- [ ] Schedule daily data sync (manual first, automate later)
- [ ] Track season averages per player for baseline comparisons

---

## 🔥 Phase 3: Heat Score Logic
- [ ] Define what counts as a "hot streak" (rolling average vs season average)
- [ ] Compute heat scores for each player based on last N games
- [ ] Save scores into DB for easy querying
- [ ] Write unit tests to validate calculations

---

## ⚙️ Phase 4: FastAPI Backend
- [ ] Set up endpoints:
  - [ ] `/players` – list players + filter options
  - [ ] `/players/{id}` – player details
  - [ ] `/players/{id}/heat-score` – heat score data
- [ ] Add pagination, filtering (team, position, etc.)
- [ ] Enable CORS for frontend access
- [ ] Document API with OpenAPI docs

---

## 🖼️ Phase 5: Frontend – Next.js Dashboard
- [ ] Display hot players list with filter by team/position
- [ ] Player detail page with heat score trend chart
- [ ] Visualizations for performance (charts or graphs)
- [ ] Implement caching or debounce on player filters
- [ ] Mobile responsiveness

---

## 📦 Phase 6: Containerization & Deployment
- [ ] Dockerize FastAPI backend
- [ ] Dockerize frontend
- [ ] Set up Docker Compose for local dev
- [ ] Deploy backend (Railway / Render / Fly.io)
- [ ] Deploy frontend (Vercel)
- [ ] Write README with usage instructions & screenshots

---

## ✅ Bonus (Optional Polish)
- [ ] Add cron job or GitHub Action to auto-update game data daily
- [ ] Add player comparison feature
- [ ] Add loading states and error messages to UI
- [ ] Add analytics (e.g. most improved players)

