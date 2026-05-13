# FMCG Consumer Analytics & Pricing Strategy
### Dataverse Hackathon — 1st Place Winner | NMIMS, January 2026
Consumer churn analysis on 1,007 FMCG transactions — uncovering two independent market share crises and delivering a winning pricing strategy. Dataverse Hackathon 2026, 1st Place.

---

## The Problem

**Effervesce**, a premium sparkling water brand, faced consecutive sales decline across three 15-day periods (Jan 1 – Feb 15, 2026). A failed marketing campaign and aggressive competition from **Zest-Bio** compounded the crisis. Leadership needed to understand: *who is leaving, where are they going, and why?*

---

## What This Project Does

This analysis goes beyond surface-level sales metrics. Using **1,007 real transactions** across 9 variables, I built a diagnostic framework that:

- Identifies **which consumer segments are churning** and to which competitors
- Distinguishes between two fundamentally different types of loss — a **positioning problem** and a **pricing problem**
- Surfaces a hidden Gen-Z pack-size gap that no one had flagged
- Exposes a critical **promotional misalignment** in digital spend
- Delivers a concrete, data-backed strategic recommendation

---

## Key Findings

| Segment | What's Happening | Magnitude |
|---|---|---|
| Health-Conscious Consumers | Switching to Zest-Bio for functional benefits | +4.26pp Zest-Bio gain |
| Millennials (27–42) | Leaving for health-forward positioning | +9.95pp Zest-Bio gain |
| High-Loyalty Customers | The most valuable segment — actively churning | +10.46pp Zest-Bio gain |
| Value Seekers & Gen-X | Moving to Private Labels on price pressure | +3.67pp Private Label gain |
| Gen-Z | 79% below market average for large pack adoption | Structural gap in pack architecture |

**Core Insight:** This isn't one crisis — it's two independent consumer trends requiring two different solutions. Problem 1 (Zest-Bio) is a positioning problem needing **innovation**. Problem 2 (Private Labels) is a pricing problem needing **optimization**.

---

## Methodology

### 1. Data Cleaning & Hygiene
- Datetime conversion for time-series analysis (`pd.to_datetime`)
- Standardized product name variants (e.g., typos like "Priivatee Labeel")
- Median imputation for pricing anomalies
- Outlier flagging for `Consumer_Age` ({-5, 999})
- 20% missing `Promo_Type` retained as "None" for promo effectiveness analysis

### 2. Feature Engineering
Created 6 behavioral features for segmentation:

| Feature | Description |
|---|---|
| `Period` | P1 / P2 / P3 (15-day windows for churn tracking) |
| `Age_Group` | Gen-Z / Millennial / Gen-X / Boomer+ |
| `Health_Segment` | Health-conscious vs Normal (based on product preference) |
| `Price_Segment` | Value / Mid / Premium (from price-per-unit patterns) |
| `Value_Seeker` | Value Seeker vs Premium Seeker |
| `Brand` | Effervesce / Zest-Bio / Private Label / Sparkle-H2O |

### 3. Analysis
- Market share trend analysis across periods and segments
- Promotional effectiveness by age group and channel
- Pack-size behavior analysis by generation
- Competitive substitution vs value migration segmentation

---

## Strategic Recommendation

**Launch "Effervesce THRIVE"** — a functional line extension targeting health-conscious Millennials.

| Attribute | Detail |
|---|---|
| Positioning | Electrolyte-enhanced, vitamin-fortified, adaptogen-infused |
| Price Point | $3.49 (matches Zest-Bio, justified by functional stack) |
| GLP-1 Friendly | Explicitly marketed |
| Pack Sizes | Single-serve ($1.50) / 4-pack ($5.99) / 12-pack ($10.99) |
| Promo Mix | 40% Social Influencer, 30% Retailer App, 20% Digital Partnerships |

Retro-premiumization was evaluated and rejected — the data shows it would target the wrong segment (Boomer+/Gen-X) against the wrong competitor (Private Labels), not the high-value Millennials being lost to Zest-Bio.

---

## Repository Structure

```
fmcg-consumer-analytics-pricing-strategy/
│
├── Main_Code.ipynb          # Full analysis notebook
├── PPT.pdf                  # Hackathon presentation deck
└── README.md
```

> **Note:** The raw dataset (`Aurora_CPG_Raw_Data_2026.csv`) is not included as it was provided under hackathon terms.

---

## Tools & Libraries

![Python](https://img.shields.io/badge/Python-3.13-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-green)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Analysis-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-red)

---

*If you're a recruiter or collaborator — the notebook walks through every analytical decision, not just the final outputs. It's worth a look.*
