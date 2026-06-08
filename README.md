# Budget vs Actual Variance Report — Unilever FY2023

## Project Overview
End-to-end financial variance analysis of Unilever PLC (LSE: ULVR.L) FY2023 P&L performance against a proxy budget constructed from published guidance. Built as part of a financial data analysis portfolio.

## Tools Used
- **Python** (pandas, matplotlib, seaborn, yfinance) — Jupyter Notebook
- **Excel** — Financial model with conditional formatting *(Phase 4 — in progress)*
- **Power BI** — Interactive dashboard *(Phase 5 — planned)*

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
│
└── README.md
```

## Phases
| Phase | Description | Status |
|-------|-------------|--------|
| 1 | Data setup — yfinance pull, budget construction | ✅ Complete |
| 2 | Variance calculations — Abs, %, F/A flags | ✅ Complete |
| 3 | Python visualisations — bar chart, waterfall, heatmap | ✅ Complete |
| 4 | Excel financial model | 🔄 In Progress |
| 5 | Power BI dashboard | 🔜 Planned |

## Key Findings
- Unilever FY2023 revenue missed budget by **€5,720m (−10.0%)** driven by FX headwinds, volume softness, and portfolio disposals
- Despite the top-line miss, **cost discipline was strong** — Cost of Revenue and SG&A both came in below budget (Favourable)
- **EBITDA missed by −16.8%** — the largest variance percentage, entirely explained by the revenue shortfall, not operational inefficiency
- Conclusion: **This was a top-line problem, not an efficiency problem**

## Budget Methodology
Unilever does not publish internal budgets. The proxy budget was constructed from FY2023 guidance issued on the February 2023 results call, applying guided USG growth, FX headwinds, and disposal impacts to FY2022 actuals.

## Data Source
- Financial data: [yfinance](https://github.com/ranaroussi/yfinance) — Unilever PLC (ULVR.L)
- Guidance basis: Unilever FY2022 Full Year Results Presentation (Feb 2023)

## Skills Demonstrated
- Pulling real financial data via API (yfinance)
- Proxy budget construction from published guidance
- Variance analysis with correct F/A sign convention
- Financial data visualisation (matplotlib, seaborn)
- Analytical interpretation — separating top-line vs efficiency issues
