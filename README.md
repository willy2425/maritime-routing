# AI‑Powered Container Ship Routing System
Ein intelligentes Routing-System für Containerschiffe, das Echtzeit-Wetter, Strömungen, Hafenstau und Treibstoffpreise kombiniert, 
um dynamische, kraftstoffeffiziente und kosteneffektive Routen zu planen – für nachhaltige, resiliente und transformative globale Logistik.

🚀 Projektübersicht
Echtzeit-Integration von Wetter, Strömungen, Hafenstau und Treibstoffdaten
KI-Optimierung der Routen (TensorFlow.js)
IoT-Simulation von Schiffs- und Sensordaten
Interaktives Frontend-Dashboard (React + Google Maps)

⚙️ Tech Stack
Bereich	Technologien
Frontend	React, Tailwind CSS, Redux/Context
Backend	Node.js, Express, REST APIs
Datenbank	MongoDB (Time-Series + Historie)
AI/ML	TensorFlow.js (In-Browser + Node.js)
Deployment	Docker, Kubernetes, AWS/GCP

📦 Architekturübersicht

Frontend (React)
├─ <MapContainer />       → Google Maps Integration
├─ <KPIWidgets />         → Fuel, Emissions, ETA
├─ <AlertsBanner />       → Congestion Alerts
├─ API Client (axios)     → /api/*

Backend (Node.js + Express)
├─ /api/weather           → OpenWeatherMap
├─ /api/vessels/positions → MarineTraffic AIS
├─ /api/fuel-prices       → Platts BunkerFuel
├─ /api/optimize-route    → TensorFlow.js Predictions

Database (MongoDB)
├─ Weather readings, vessel positions, fuel prices, optimized routes
🔑 Kernfunktionen
Dynamische Routenoptimierung unter Echtzeitbedingungen

Vorhersage von Störungen und Staus

KPI-Dashboard für Verbrauch, Emissionen und ETAs

IoT-Simulationsdaten für Tests und Modelltraining

📅 6‑Wochen-Roadmap

Woche	Fokus	Ziel
1	Research & Architektur	KPIs, API-Auswahl, System-/Datenfluss
2	Backend Core	Express-Server, MongoDB-Modelle
3	Frontend MVP	React Dashboard mit Karten und KPIs
4	AI/ML Modellierung	TensorFlow.js-Modelle trainieren
5	IoT-Simulation und Tests	Mock-Sensordaten, E2E Tests
6	Deployment & Demo	Containerisierung, Cloud Deployment, CI/CD
📡 Genutzte APIs

Domäne	API/Dataset	Zweck
AIS/Vessel Tracking	MarineTraffic AIS	Positionsdaten in Echtzeit
Wetter & Strömung	OpenWeatherMap One Call	Vorhersagen & Ozean-Daten
Hafenstau	PortXchange, Sinay	Liegeplatz-Prognosen
Treibstoffpreise	Platts BunkerFuel, Ship & Bunker	Spot-/Vertragspreise
🎯 Nachhaltigkeits-KPIs

4–7 % weniger Kraftstoffverbrauch
10–15 % kürzere Verzögerungen
15–25 % weniger CO₂-Emissionen (IMO CII-konform)
10 % geringere Hafenleerlaufzeit

📂 Projektstruktur
/client
├─ components
│   ├─ Dashboard.jsx
│   ├─ Upload.jsx
│   └─ Quiz.jsx
└─ App.js

/server
├─ routes
│   ├─ weather.js
│   ├─ vessels.js
│   ├─ fuelPrices.js
│   └─ optimizeRoute.js
├─ models/
├─ services/
└─ app.js

# Backend
cd server
npm install
npm run dev

# Frontend
cd client
npm install
npm start
