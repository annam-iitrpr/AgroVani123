# 🌾 AgroVani

<div align="center">

  <img src="https://img.shields.io/badge/AI%20for%20Agriculture-Enabled-22c55e?style=for-the-badge&logo=vercel&logoColor=white" alt="AI for Agriculture" />
  <img src="https://img.shields.io/badge/Sustainability-Residue%20Reduction-16a34a?style=for-the-badge" alt="Sustainability" />

  <h3>Smart farming. Sustainable decisions. Better livelihoods.</h3>

  <p>
    AgroVani is an AI-powered agricultural ecosystem that helps farmers make better crop, market, and residue-related decisions while connecting them with trusted machinery and service providers.
  </p>

</div>

[![Next.js](https://img.shields.io/badge/Next.js-14-black?style=flat&logo=next.js)](https://nextjs.org/)
[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat&logo=python)](https://python.org/)
[![Supabase](https://img.shields.io/badge/Supabase-PostgreSQL%20%26%20Auth-3ECF8E?style=flat&logo=supabase)](https://supabase.com/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS-38B2AC?style=flat&logo=tailwindcss)](https://tailwindcss.com/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

> 🚀 Live app: https://agro-vani.vercel.app

---

## ✨ At a glance

| Focus area | Value delivered |
| --- | --- |
| 🌱 Farmer support | Better crop, yield, and residue decisions |
| 🤖 AI intelligence | Recommendations, advisory, and scoring models |
| 🚜 Equipment access | Machinery booking and marketplace discovery |
| 📍 Localized insights | Maps, mandi data, and regional context |
| ♻️ Sustainability | Lower stubble burning and smarter residue reuse |

AgroVani connects farmers, machinery sellers, and agri-service providers through a single digital ecosystem designed to reduce crop residue burning, improve decision quality, and drive more sustainable agricultural outcomes.

---

## 🧭 Why AgroVani?

Agriculture in many regions still faces a combination of four major problems:

- Stubble burning and air pollution caused by crop residue disposal challenges
- Limited access to affordable farm equipment and rental services
- Lack of trusted, localized agronomic advice in usable formats
- Fragmented supply chains between farmers, sellers, and logistics partners

AgroVani addresses these challenges with an AI-enabled platform that brings together:

- Crop and residue recommendations
- Farm and machinery marketplace workflows
- AI-generated advisory experiences
- Geo-aware, data-backed recommendations
- Multilingual farmer accessibility

---

## 🚀 What this project includes

### Farmer-facing experience
- Guided onboarding for farm profile, crops, and land details
- Advisory dashboards for yield, mandi prices, and MSP comparisons
- Recommendations for crop choices and residue management
- Machinery discovery and booking workflows
- Maps and localized data views for field-level context

### AI and decision systems
- Gemini-powered voice advisory and response layer
- Crop and residue recommendation engines
- Matching and ranking logic for logistics / buyer-farmer alignment
- ML-based scoring for agricultural suitability and assignment quality

### Business and operations layer
- Machinery seller dashboard
- Booking and inventory workflows
- Admin verification and moderation views
- Market intelligence and sustainability metrics

---

## 🧠 AI-first architecture

```text
User / Farmer / Seller
        |
        v
   Next.js Application
        |
        +--> UI + multilingual UX
        +--> Dashboard + advisory flows
        +--> Maps + booking experience
        |
        v
  AI & Decision Services
        |
        +--> Gemini voice advisory + speech generation
        +--> Crop recommendation engine
        +--> Residue management engine
        +--> Matching / optimization model
        |
        v
  Data & Infra Layer
        |
        +--> Supabase / PostgreSQL
        +--> Weather and agronomic adapters
        +--> Python ML / scoring APIs
        +--> Storage, auth, and deployment services
```

---

## 🛠️ Tech stack

| Area | Stack |
| --- | --- |
| Frontend | Next.js 14, React, Tailwind CSS, Shadcn UI |
| Backend | Next.js app routes, Python APIs, FastAPI-style server integration |
| Database & auth | Supabase, PostgreSQL |
| Mapping | Leaflet / React-Leaflet |
| AI / ML | Gemini, LightGBM, Python model pipelines |
| Testing | Pytest, project-level test orchestration |
| Deployment | Vercel, Render, Docker |

---

## 📁 Repository structure

```bash
AgroVani/
├── api/                     # Python API layer for matching and scoring
├── apps/                   # App workspaces / runtime packages
├── backend/                # Core backend services and adapters
├── contracts/              # Shared contract definitions
├── data/                   # Synthetic / reference data and generated artifacts
├── docs/                   # Documentation and guides
├── engine/                 # Core operational logic and orchestration
├── infra/                  # Infrastructure and deployment setup
├── ml/                     # ML training and model artifacts
├── packages/               # Shared libraries and workspace packages
├── science/                # Agricultural calculation and scoring logic
├── services/               # Service runtimes and specialized modules
├── shared/                 # Cross-runtime utilities
├── scripts/                # Automation and operational scripts
├── tests/                  # Automated tests
├── web/                    # Frontend application
├── .env.example            # Example environment file
├── docker-compose.yml      # Docker orchestration
├── package.json            # Root workspace scripts
├── requirements.txt        # Python dependencies
├── render.yaml             # Render deployment config
├── README.md               # Project overview and onboarding
└── LICENSE                 # Project license
```

---

## ⭐ Key capabilities

### 1) Crop and residue advisory
The platform recommends crops and residue-handling strategies using agricultural logic, field data, and contextual models. This helps farmers choose options that improve sustainability and reduce harmful burning practices.

### 2) Mandi and market insights
The farmer dashboard provides pricing trends, MSP comparison, and market overview with data-driven reporting. It is designed to make agricultural decision-making more accessible and transparent.

### 3) Voice and conversational AI
The app includes a voice advisory flow where a farmer question is captured in the browser, processed by a server-side Gemini assistant, and optionally converted to speech. This makes the experience more natural and accessible for rural users.

### 4) Logistics matching engine
The matching service uses LightGBM-based scoring and a capacity-aware assignment process to match farmers with buyers while respecting tonnage and compatibility constraints.

### 5) Multilingual accessibility
AgroVani is designed with English, Hindi, and Punjabi support so the experience can better serve diverse farmer communities.

---

## ⚡ Quick start

### Prerequisites
- Node.js >= 18.18
- npm
- Python >= 3.10
- Optional: Docker for local container workflows

### Frontend setup

```bash
npm install
cp .env.example .env.local
npm run dev
```

This starts the primary web experience for the AgroVani app.

### Python ML / matching setup

Install Python dependencies:

```bash
python -m pip install -r requirements.txt
```

Generate synthetic training data and train the model:

```bash
python data/generate_synthetic_data.py
python ml/train_model.py
```

Start the matching API:

```bash
uvicorn api.main:app --host 0.0.0.0 --port 8000
```

Available endpoints include:
- `GET /health`
- `POST /score`
- `POST /match`
- Interactive docs at `/docs`

---

## 📝 Important API and product notes

### Farmer advisory MVP
Open `/farmer/advisory` to access the yield and mandi dashboard.

Core API routes include:
- `POST /api/yield-prediction`
- `GET /api/mandi`
- `GET /api/msp`
- `POST /api/report/pdf`
- `POST /api/report/whatsapp`

These routes provide yield forecasts, price signals, and farmer-friendly summaries designed for practical use.

### Matching engine behavior
The Python matching engine:
- scores farmer-buyer compatibility using machine learning
- enforces capacity-aware assignments
- avoids invalid unstable allocations
- rejects oversized batch requests safely
- returns `409 Conflict` for unresolved assignment cycles

### Demo data caution
Mandi demo data is explicitly intended for demo use and should be replaced with verified production data before launch.

---

## 🔐 Environment variables

Use `.env.example` as the reference baseline. Typical variables may include:

- `GEMINI_API_KEY` for Gemini-powered advisory flows
- `GEMINI_TTS_MODEL` and `GEMINI_TTS_VOICE` for speech generation tuning
- `MATCH_API_KEY` for protected model endpoints
- Supabase or service credentials required by the app environment

---

## ✅ Testing

Run Python tests:

```bash
pytest
```

Run frontend workspace checks if needed:

```bash
npm run lint
npm run build
```

---

## 🚀 Deployment

This repository is set up for:
- Vercel deployment for the web frontend
- Render deployment for Python services
- Docker-based local or cloud orchestration

See:
- `vercel.json`
- `render.yaml`
- `docker-compose.yml`

---

## 🌍 Project impact

AgroVani supports several practical sustainability and development goals:

- Reduced stubble burning and related environmental damage
- Lower barriers to access for small and marginal farmers
- Better market visibility and crop planning via AI guidance
- More efficient farm equipment circulation and logistics
- Stronger rural digital inclusion through multilingual access

---

## 👥 Contributors

- Debayan Paul
- Annesha Chakraborty
- Ayan Chatterjee
- Nikita Bose

Built with the goal of creating a more resilient, intelligent, and sustainable agriculture ecosystem.

---

## License

This project is licensed under the MIT License.

build trains the demo models before starting Uvicorn, and `/health` is its
health check. The service generates a `MATCH_API_KEY` in Render. Send it as
`X-API-Key` on `/score` and `/match`; keep this value in server-side
configuration and never expose it in browser code. Locally, the key is
optional unless `MATCH_API_KEY` is set.

The committed generation recipe currently produces **synthetic** labels. The
model and its validation metrics are for pipeline verification only. Before
using recommendations for purchasing or logistics decisions, train on
representative, consented, quality-checked historical transactions and review
the matching policy with marketplace operators.
