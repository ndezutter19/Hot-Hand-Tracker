# NBA Hot Hand Tracker – Project Tasks

## Phase 1: Core Dashboard MVP – Hottest Players Today

### 1.1 Data Collection and Storage
- [ ] Set up PostgreSQL schema for players, games, and stats
- [ ] Write script to fetch last 5 games per player using nba_api
- [ ] Write script to fetch and store season averages per player
- [ ] Store game logs and season averages in the database

### 1.2 Heat Score Calculation
- [ ] Define and implement initial heat score formula (based on points)
- [ ] Calculate 5-game rolling average for each player
- [ ] Compare to season average to produce heat score
- [ ] Save computed scores to the database

### 1.3 Backend API (FastAPI)
- [ ] Set up FastAPI project and connect to PostgreSQL
- [ ] Create endpoint: GET /players/hottest
  - [ ] Return player name, team, position, heat score, rolling avg, season avg
  - [ ] Support query filters: team, position, min_games

### 1.4 Frontend Dashboard (Next.js)
- [ ] Set up Next.js project
- [ ] Create landing page: pages/index.tsx
- [ ] Fetch and display list of hottest players
- [ ] Add filter controls: team, position, min_games

---

## Phase 2: Player Detail View

### 2.1 Backend
- [ ] Create endpoint: GET /players/{id}
  - [ ] Return player info, recent game stats, season averages
  - [ ] Include heat score history

### 2.2 Frontend
- [ ] Create player detail page: pages/player/[id].tsx
- [ ] Display line graph of selected stat (e.g. points) over recent games
- [ ] Display season averages and 5-game rolling average
- [ ] Display recent performance table

---

## Phase 3: Stat-Based Filtering and Multi-Metric Hotness

### 3.1 Backend Support
- [ ] Track all relevant metrics: points, rebounds, assists, PRA, PR, RA, PA
- [ ] Update /players/hottest endpoint to accept a stat filter (e.g. ?stat=pra)

### 3.2 Frontend Integration
- [ ] Add dropdown or tab selector for stat type on dashboard
- [ ] Update player detail chart to reflect selected stat
- [ ] Ensure filters apply consistently across API and UI

---

## Phase 4: Advanced Features and Enhancements

### 4.1 Hot Teams View
- [ ] Aggregate team-level heat scores based on players
- [ ] Create new API endpoint: GET /teams/hottest
- [ ] Display hot team rankings on frontend

### 4.2 Predictive Analysis (Stretch Goal)
- [ ] Build simple trend predictor based on heat score trajectory
- [ ] Add predictive marker to player detail view

### 4.3 UI/UX and Visual Polish
- [ ] Add player photos, team logos, and color coding
- [ ] Improve mobile responsiveness and styling
- [ ] Add tooltips and loading states

---

## Phase 5: DevOps and Deployment

- [ ] Dockerize backend (FastAPI) and frontend (Next.js)
- [ ] Write docker-compose.yml to run both services locally
- [ ] Deploy backend to Railway or Render
- [ ] Deploy frontend to Vercel
- [ ] Add a production-ready README with instructions and screenshots

---

## Optional: Automation and Monitoring
- [ ] Add daily data update script using cron or GitHub Actions
- [ ] Add logging and error alerts for data jobs
- [ ] Add optional unit and integration tests for core functions

