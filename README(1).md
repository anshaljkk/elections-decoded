# india election dashboard

won 1st place at IIM Shillong's Data-Dash 2026 with this. built it with my team (Aaditya and Aashima) in about 2 weeks.

the case was basically — here's 10 years of indian assembly election data, figure out why voter turnout is so uneven and what can be done about it.

---

## what it does

its a single html file dashboard. open it in browser, thats it. no setup, no npm install, nothing.

covers assembly elections from 2009 to 2021 — 32 states, ~4000 constituencies, ~10k data points. has like 10+ charts and an interactive priority ranking table.

---

## what we actually found

the main thing we kept coming back to — india's 72% average turnout sounds fine until you see that tripura is at 92% and bihar is at 56%. thats a 36 point gap. the average is basically lying.

three things that actually drive low turnout:

**1. constituency size** — bigger the electorate, lower the turnout. r = -0.49, strongest correlation in the whole dataset. seats with 5L+ voters average 52% turnout vs 80% for sub-1L seats. every extra lakh voters = ~2.8pp drop.

**2. too many candidates** — sounds counterintuitive but more candidates = lower participation. 20+ candidate seats average 63% vs 81% for under-5. probably choice paralysis + nobody takes the result seriously.

**3. urban apathy** — places like mumbai's colaba, versova, patna's bankipur have been under 40% for 3+ consecutive elections. its not a one-off, its structural.

also — 28% of all elections were decided by under 5% margin. so the apathy is literally changing who wins.

---

## the CPI thing

we made a score to rank which constituencies need attention most:

```
CPI = 0.35 × how far below national avg
    + 0.25 × how volatile turnout is
    + 0.20 × electorate size
    + 0.20 × declining trend
```

if the top 50 worst seats just reached national average, thats ~6 million extra votes per election cycle.

---

## charts in the dashboard

- national turnout trend 2009–2021
- state-level choropleth map
- turnout by electorate size
- turnout by no. of candidates
- margin of victory distribution (all 10k contests)
- gender candidacy vs wins trend
- CPI priority matrix (4 quadrant scatter)
- top 20 priority constituencies table

---

## files

```
india_election_dashboard.html  — the whole thing, open this
presentation.pdf               — the slide deck we presented
README.md                      — you're reading it
```

---

## stack

html + css + js, chart.js for the charts, google fonts (syne + space mono). everything is in one file, no external dependencies except those two CDN links.

---

## dataset

assembly elections 2009–2021, provided by IIM Shillong as part of the case. ECI data.
