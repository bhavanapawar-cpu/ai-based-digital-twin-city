<<<<<<< HEAD
# ai-based-digital-twin-city
=======
# Mumbai Digital Twin AI Risk Engine
>>>>>>> ee5678f (refactor: reorganise project structure for clarity and modularity)

An AI-powered urban disaster management system for Mumbai — combining a FastAPI backend with a React frontend to simulate, predict, and respond to multi-hazard scenarios in real time.

## Project Structure

```
DIGITAL_TWIN_AI_RISK_ENGINE/
├── backend/                  # FastAPI Python backend
│   ├── api/                  # Route handlers (17 endpoints)
│   ├── core/                 # AI engine modules (digital twin, disaster engines, XAI, etc.)
│   ├── data_loaders/         # Data ingestion utilities
│   ├── database/             # DB models and session management
│   ├── evacuation_system/    # A* pathfinding evacuation engine
│   ├── services/             # Background services
│   ├── static/               # Static file serving
│   ├── config.py             # App configuration
│   ├── dependency_container.py
│   └── main.py               # Entry point
│
├── frontend/                 # React 18 + Vite frontend
│   ├── src/
│   │   ├── components/       # Shared UI components
│   │   ├── context/          # React context (WardContext)
│   │   ├── pages/            # Page-level components (19 pages)
│   │   ├── services/         # API and AI engine service clients
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── package.json
│   └── vite.config.js
│
├── data/
│   └── mumbai/
│       ├── static/           # Ward and infrastructure CSVs
│       ├── realtime/         # Sensor data CSVs
│       ├── historical/       # Historical disaster data
│       └── outputs/          # AI output logs
│
├── docs/
│   ├── guides/               # Setup, usage, and feature guides
│   ├── implementation/       # Phase summaries and technical notes
│   └── troubleshooting/      # Fix guides and debug notes
│
├── scripts/                  # Shell scripts and utility Python scripts
├── tests/                    # Test and validation scripts
├── demo_checkpoints/         # Saved demo state snapshots
│
├── .env                      # Environment variables
├── requirements.txt          # Python dependencies
├── docker-compose.yml        # Local dev orchestration
└── Dockerfile
```

## Quick Start

**Backend** (Python 3.10+):
```bash
pip install -r requirements.txt
uvicorn backend.main:app --reload --port 8000
```

**Frontend** (Node 18+):
```bash
cd frontend
npm install
npm run dev
```

Or use Docker:
```bash
docker-compose up
```

- Backend API: http://localhost:8000
- Frontend: http://localhost:5173
- API Docs: http://localhost:8000/docs

## Documentation

- `docs/guides/` — setup instructions, feature guides, demo scripts
- `docs/implementation/` — phase summaries, AI module notes
- `docs/troubleshooting/` — fix guides and known issues
