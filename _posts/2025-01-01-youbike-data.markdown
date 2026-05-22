---
layout: post
title: YouBike Live
date: 2025-01-01
type: main
featured: true
project_url: https://tunglinn.github.io/youbike-data
category: Data Engineering, Live Maps
description: Real-time YouBike station tracker for Taipei — scraper pipeline, SQLite database, REST API, and Leaflet map frontend.
---

YouBike Live tracks the availability of Taipei's public bike-sharing stations in real time. A Python scraper polls the YouBike API on a schedule, persists records to a SQLite database, and exposes the data through a lightweight REST API. The frontend renders all active stations on an interactive Leaflet map with live counts.

## Components

- **Scraper** — Python script polling the YouBike TDX feed, writing deltas to SQLite
- **Database** — SQLite with time-series records per station
- **API** — lightweight endpoint layer serving current station state
- **Frontend** — Leaflet map with per-station markers, availability counts, and Chart.js history sparklines

## Tech Stack

- Python (scraper, API)
- SQLite
- Cloudflare Workers (edge deployment)
- Leaflet.js + Chart.js
