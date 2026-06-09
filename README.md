# Budget vs Actual Variance Report — Unilever FY2023

## Project Overview
This project constructs a proxy Budget vs Actual (BAT) variance analysis for Unilever PLC (LSE: ULVR.L) for FY2023. Since listed companies do not publish internal budgets, the budget was constructed from Unilever's published FY2023 guidance (Feb 2023 results call), adjusted for underlying sales growth, FX headwinds, and portfolio disposals.
Key finding: EBITDA missed budget by -16.8% despite favourable cost variances. This was a top-line revenue problem — not an operational efficiency failure. A €5,720m revenue shortfall (driven by FX headwinds, volume softness, and portfolio disposals) overwhelmed strong cost discipline across Cost of Revenue and SG&A.

## Tools Used
- **Python** (pandas, matplotlib, seaborn, yfinance) — Jupyter Notebook
- **Excel** — Financial model with conditional formatting *
- **Google Looker Studio** — Interactive dashboard *

## Project Structure
```
budget-vs-actual-unilever/
│
├── data/
│   └── Unilever Financial Analysis.csv       # Cleaned dataset (Phase 1 output)
│
├── notebooks/
│   ├── Financial Analysis Unilever.ipynb  # Phase 1 & 2: Data setup + variance calculations
│   └── 02_Visualisations_Unilever.ipynb   # Phase 3: Python charts
│
├── charts/
│   ├── chart1_budget_vs_actual.png        # Grouped bar chart
│   ├── chart2_variance_waterfall.png      # Variance waterfall
│   └── chart3_variance_heatmap.png        # Variance % heatmap
│
├── excel/
│   └── Unilever Financial Analysis.xlsx            # Excel financial model (Phase 4)
│model
│
└── README.md
```

## Phases
Phase 1 — Data Setup ✅

Pulled real income statement data via yfinance 1.2.1
Extracted 7 P&L line items: Total Revenue, Cost Of Revenue, Gross Profit, SG&A, Operating Income, EBITDA, Net Income
Converted figures to €millions

Phase 2 — Variance Calculations ✅

Constructed proxy budget from published FY2023 guidance
Calculated Variance_Abs, Variance_Pct, and F/A flags
Applied correct sign convention: cost lines flip the favourable/adverse logic

Phase 3 — Python Visualisations ✅

Grouped bar chart: Budget vs Actual across all P&L lines
Variance waterfall chart: F/A colour-coded (green = favourable, red = adverse)
Heatmap: variance intensity with corrected sign convention for cost lines

Phase 4 — Excel Model ✅

Three-sheet workbook: Data, Model (formatted P&L), Dashboard
KPI callout boxes, clustered bar chart, conditional formatting

Phase 5 — Looker Studio Dashboard ✅

Interactive single-page dashboard
KPI scorecards (Revenue, EBITDA, Net Income vs Budget)
Clustered bar chart and variance chart
Live dashboard: https://datastudio.google.com/reporting/2f33d0e9-acea-4d0f-a02b-e28b07d8d392

## Key Findings
- Unilever FY2023 revenue missed budget by **€5,720m (−10.0%)** driven by FX headwinds, volume softness, and portfolio disposals
- Despite the top-line miss, **cost discipline was strong** — Cost of Revenue and SG&A both came in below budget (Favourable)
- **EBITDA missed by −16.8%** — the largest variance percentage, entirely explained by the revenue shortfall, not operational inefficiency
- Conclusion: **This was a top-line problem, not an efficiency problem**

## Budget Methodology
This is a proxy budget, not Unilever's actual internal plan. The budget was constructed from:

Revenue: 2022 actual × 1.04 underlying sales growth × 0.97 FX headwind × 0.97 portfolio disposals
Cost lines: Derived from 2022 cost ratios applied to revised revenue guidance
Margins: Calibrated against Unilever's published FY2023 margin guidance

All variances should be interpreted in this context.

## Data Source
- Financial data: [yfinance](https://github.com/ranaroussi/yfinance) — Unilever PLC (ULVR.L)
- Guidance basis: Unilever FY2022 Full Year Results Presentation (Feb 2023)

## Skills Demonstrated
- Pulling real financial data via API (yfinance)
- Proxy budget construction from published guidance
- Variance analysis with correct F/A sign convention
- Financial data visualisation (matplotlib, seaborn)
- Analytical interpretation — separating top-line vs efficiency issues
