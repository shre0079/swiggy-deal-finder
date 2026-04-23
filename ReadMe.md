# 🍔 Swiggy Deal Finder

A web application that tracks real-time pricing, discounts, and high-value deals on Swiggy — powered by Swiggy's MCP APIs.

> Built as part of the **Swiggy Builders Club** program.

---

## 💡 What It Does

Most users miss out on the best deals on Swiggy simply because prices and discounts change constantly. Swiggy Deal Finder solves this by:

- Fetching **live pricing and discount data** from Swiggy's Food & Instamart APIs
- Storing **historical price data** to detect genuine drops vs temporary offers
- Running a **deal-scoring engine** to rank items by real value
- Displaying the **best deals right now** through a clean web interface
- Supporting **AI-powered queries** like *"Best meal under ₹150 near me"*

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Backend | Java (Spring Boot) |
| Database | PostgreSQL |
| Frontend | React |
| APIs | Swiggy MCP (Food, Instamart, Dineout) |
| Auth | OAuth 2.0 via Swiggy |

---

## 🏗️ Architecture Overview

```
User
 │
 ▼
React Frontend
 │  (REST API calls)
 ▼
Spring Boot Backend
 ├── MCP API Integration Layer   → fetches live Swiggy data
 ├── Data Ingestion Service      → scheduled price collection
 ├── Deal Scoring Engine         → computes value scores
 └── PostgreSQL                  → stores historical pricing data
```

---

## ✨ Key Features (Planned)

- [x] Project setup & architecture design
- [ ] Swiggy MCP API integration (Food + Instamart)
- [ ] Historical price tracking with PostgreSQL
- [ ] Deal scoring algorithm
- [ ] React frontend with deal listings
- [ ] AI copilot for natural language deal queries
- [ ] User location-based filtering

---

## 🚀 Getting Started

### Prerequisites

- Java 17+
- Node.js 18+
- PostgreSQL
- Swiggy MCP API credentials

### Backend

```bash
cd backend
./mvnw spring-boot:run
```

### Frontend

```bash
cd frontend
npm install
npm start
```

App runs at `http://localhost:3000`

---

## 📁 Project Structure

```
swiggy-deal-finder/
├── backend/               # Spring Boot application
│   ├── src/
│   │   ├── api/           # Swiggy MCP integration
│   │   ├── engine/        # Deal scoring logic
│   │   ├── scheduler/     # Price ingestion jobs
│   │   └── controller/    # REST endpoints
│   └── pom.xml
│
├── frontend/              # React application
│   ├── src/
│   │   ├── components/    # UI components
│   │   ├── pages/         # App pages
│   │   └── services/      # API calls
│   └── package.json
│
└── README.md
```

---

## 🤝 Built With

- [Swiggy Builders Club](https://builders.swiggy.com) — MCP API access
- Spring Boot — Backend framework
- React — Frontend framework
- PostgreSQL — Data persistence

---

## 📬 Contact

Built by [Your Name] · [your@email.com]

---

> **Status:** 🚧 In Active Development
