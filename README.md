# 🗳️ Elections Decoded — India Electoral Participation Intelligence Dashboard

> **🏆 1st Place — Data-Dash: Turning Data Into Decisions | IIM Shillong, 2026**  
> Team **Data Bashers**: Aaditya Sharma · Anshal Chauhan · Aashima

---

## The Problem

India's national voter turnout averages **72%** — a number that looks healthy until you look underneath it. A **36-point gap** separates Tripura (92%) from Bihar (56%). Nearly **1-in-3 assembly elections** between 2009–2021 were decided by margins under 5%. Urban constituencies in Maharashtra and Bihar routinely deliver sub-40% turnout across consecutive election cycles.

The average is hiding a crisis.

---

## What We Built

An **interactive single-page dashboard** analysing **10,572 constituency-year observations** across **32 states and UTs**, **4,041 unique constituencies**, and **1,734 parties** — covering Indian assembly elections from 2009 to 2021.

The dashboard surfaces three structural drivers of low participation and ranks every constituency by intervention urgency using a composite **Constituency Priority Index (CPI)**.

---

## Key Findings

| Finding | Stat |
|---|---|
| Electorate size → turnout correlation | **r = -0.49** (strongest predictor in dataset) |
| Constituencies >5L voters avg turnout | **52%** vs 80% for sub-1L seats |
| Candidate count → turnout correlation | **r = -0.38** |
| Constituencies with 20+ candidates | avg **63%** vs 81% for under-5 |
| Elections decided by <5% margin | **28%** of all contests (2,990 seats) |
| Women candidates share (2021) | **10.4%** — only 3pp gain over 13 years |
| Urban Bihar/Maharashtra turnout | **<40%** across 3+ consecutive cycles |

### Three Structural Failures

1. **Scale Suppression** — Mega-constituencies suppress turnout. Every 1 lakh additional voters reduces turnout by ~2.8pp.
2. **Fragmentation Drag** — More candidates paradoxically suppress participation (choice paralysis + legitimacy diffusion).
3. **Urban Apathy** — Low-turnout urban seats (Bankipur, Colaba, Versova) show stable declining trends — structural, not attitudinal.

---

## The Constituency Priority Index (CPI)

A composite score that ranks every constituency by how urgently it needs electoral intervention:

```
CPI = 0.35 × Low Turnout Score
    + 0.25 × Volatility Score (CV)
    + 0.20 × Electorate Size Score
    + 0.20 × Declining Trend Score
```

Constituencies are tiered into four quadrants: **Critical → High → Structural → Benchmark**.

If the **top 50 priority seats** reached national average turnout (72%):
- Estimated additional votes: **~5.9M per election cycle**
- Across 3 cycles: **~18 million reclaimed votes**

---

## Three Proposed Interventions

| # | Intervention | Target | Projected Impact |
|---|---|---|---|
| 01 | Constituency Delimitation Reform | Bihar, UP, Maharashtra (>3L seats) | +6–10pp turnout lift |
| 02 | Urban Constituency Mobilisation Programme | Top 50 CPI priority seats | +8–15pp in ultra-low seats |
| 03 | Predictive Participation Monitoring Dashboard | National Electoral Authority | Proactive vs reactive — ROI multiplied |

---

## Dashboard Features

- **National Turnout Trend** (2009–2021) — line chart with reference line
- **State Choropleth Map** — 32 states colour-coded by turnout intensity
- **Top 5 / Bottom 5 States** — bar chart of participation extremes
- **Electorate Size vs Turnout** — grouped bar (5 size buckets)
- **Candidate Count vs Turnout** — grouped bar (5 brackets)
- **Reservation Type Analysis** — GEN / SC / ST turnout comparison
- **Contest Closeness & Participation** — ultra-close vs landslide comparison
- **Margin of Victory Distribution** — 10,572 contests colour-coded by competitiveness
- **Gender Participation Funnel** — candidacy → wins trend (2009–2021)
- **CPI Priority Matrix** — 4-quadrant scatter (Critical / Monitor / Structural / Benchmark)
- **Top 20 Highest-Priority Constituencies** — ranked intervention targets table

---

## Files

```
.
├── india_election_dashboard.html   # Fully self-contained interactive dashboard
├── presentation.pdf                # Competition slide deck (Data Bashers)
└── README.md
```

The dashboard is **entirely self-contained** — no server, no dependencies to install. Just open `india_election_dashboard.html` in any browser.

---

## Tech

- **Vanilla HTML/CSS/JS** — zero frameworks, zero build steps
- **Chart.js 4.4.1** — all visualisations
- **Syne + Space Mono** (Google Fonts) — typography
- Data embedded directly in the HTML

---

## Dataset

Assembly Elections Dataset 2009–2021  
32 States · 10,572 Constituency-Year Observations  
Source: Election Commission of India (via structured case dataset provided by IIM Shillong for Data-Dash 2026)

---

## Competition Context

**Data-Dash: Turning Data Into Decisions** — IIM Shillong  
Two-round competition: online data analytics quiz → data-driven case challenge  
Prize pool: ₹50,000 | **We won the ₹30,000 first prize.**

---

*"Democracy's strength is measured not by who wins, but by how many participate. The data shows where we are failing — and exactly how to fix it."*
