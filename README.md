Book2Travel
AI‑powered travel assistant that finds multi‑modal routes (train + flight) and saves up to 70% compared to tour operators.

📌 Overview
Book2Travel is a travel platform that combines:

AI Travel Agent — natural language search with DeepSeek

Complex route planning — automatically includes closed airports (e.g. Rostov → Sochi by train → Istanbul → Bangkok)

Flight search — White Label via Travelpayouts / Aviasales

Hotel search — White Label (Ostrovok, Trip.com, Planet of Hotels)

B2B corporate travel — legal entity bookings with full accounting documents (via Bronevik.com)

The user describes a trip in plain text, and the AI returns a complete route with real prices, hotels, and money‑saving recommendations.

🚀 Key Features
Feature	Description
🤖 AI Travel Agent	DeepSeek parses user requests, builds optimal routes, suggests alternatives
🗺️ Multi‑modal routes	Combines trains, buses, flights — accounts for closed airports
✈️ Flight search	White Label subdomain avia.book2travel.ru (Travelpayouts / Aviasales)
🏨 Hotel search	White Label for hotels (Ostrovok, Trip.com, Planet of Hotels)
📈 SEO‑ready	10,000+ static pages for cities and destinations (Thailand, Turkey, UAE, Egypt)
🏢 B2B travel	Corporate trips with VAT invoices, contracts, and accounting documents
💳 Russian cards	Mir, Visa, Mastercard issued in Russia are accepted
📱 Mobile‑friendly	Fully responsive web app (React Native mobile app planned)
🛠️ Tech Stack
Frontend
Next.js 15 — React framework, static generation for SEO pages

Tailwind CSS — styling

TypeScript — type safety

Backend
Node.js + Express — API server

PostgreSQL — user data, bookings, travelers

Redis — caching for city data and API responses

BullMQ — job queue for async city generation

AI & APIs
DeepSeek API — natural language parsing and route formatting

Travelpayouts API — flights (Aviasales) and hotels

Ostrovok API — hotels (affiliate contract)

Bronevik.com API — B2B corporate travel

GeoNames — 11M+ cities database (free)

OpenStreetMap — POI, hotels, restaurants (free)

Wikipedia API — city descriptions and attractions (free)

Infrastructure
VPS — Ubuntu 22.04, Nginx, PM2

Docker — isolated environments for development

GitHub — version control

📁 Project Structure (simplified)
text
book2travel/
├── frontend/               # Next.js app
│   ├── pages/              # Main pages + 10,000+ SEO city pages
│   ├── components/         # React components (search, hotels, flights)
│   └── public/             # Static assets
├── backend/                # Node.js API
│   ├── services/           # External API integrations
│   ├── models/             # PostgreSQL models
│   ├── workers/            # BullMQ workers (city generation)
│   └── routes/             # API endpoints
├── data/                   # Static city data (GeoNames import)
└── docker/                 # Docker configs for isolated development
💰 Business Model
Source	Commission	Notes
Flights (Aviasales)	1.1–1.3% of ticket price	via Travelpayouts White Label
Hotels (Trip.com)	up to 5.5% of booking	via Travelpayouts White Label
Hotels (Ostrovok)	5% of booking	direct affiliate contract
B2B travel	negotiable	corporate clients with VAT
Mobile app ads	—	planned (AdMob / Yandex Ads)
Payment flow: Client pays the partner (Ostrovok, Trip.com, Aviasales) directly. Partner pays commission to Book2Travel. Zero capital tied up in transactions.

🗺️ SEO Strategy
10,000+ static pages for cities (generated from GeoNames and OpenStreetMap data)

83 landing pages for popular destinations (Thailand, Turkey, UAE, Egypt)

Dynamic content — when a user requests a city not yet in the static set, the system:

Fetches data from Wikipedia, OpenStreetMap, and GeoNames
Caches it in Redis + file system
Returns the page to the user
All subsequent visitors get it instantly
Automated indexing — sitemap.xml + IndexNow + Yandex.Webmaster API

📈 Roadmap
Flight search White Label (Aviasales / Travelpayouts)

83 SEO landing pages for Thailand, Turkey, UAE, Egypt

Google Search Console + Yandex.Webmaster integration

API integration for B2B travel (Bronevik.com)

CNAME setup for hotel White Label (Ostrovok)

Mobile app (React Native) with offline guides

AI‑generated city descriptions (DeepSeek)

10,000+ dynamic city pages from GeoNames / OSM

Flight + hotel package deals

Cashback program for repeat customers

🤝 Partners & Affiliates
Partner	Service	Commission	Status
Travelpayouts	Flights (Aviasales)	40% of their revenue	✅ Active
Ostrovok	Hotels (RU & global)	5%	⏳ Awaiting White Label activation
Bronevik.com	B2B corporate travel	negotiable	✅ API access granted
Trip.com	Hotels (global)	up to 5.5%	⏳ Needs 50k monthly visits
Planet of Hotels	Hotels (global)	via Travelpayouts	✅ Available
Tutu.ru	Trains, buses, flights	up to 6%	⏳ Awaiting reply
🛡️ Legal & Safety
Russian legal entity — Individual Entrepreneur (ИП Вирабов Г.С.)

Affiliate agreements with Ostrovok, Travelpayouts, Bronevik.com

User data protection — GDPR + 152‑FZ compliant

All bookings are processed by partners — Book2Travel never handles client payments

📄 License
This project is proprietary. All rights reserved.
For partnership inquiries, contact: baltazzar009@gmail.com

🙏 Acknowledgements
Travelpayouts — affiliate platform

DeepSeek — AI language model

GeoNames — free city database

OpenStreetMap — free map data

Next.js — React framework

Book2Travel — Smart travel, smarter savings. ✈️🚂🏨
