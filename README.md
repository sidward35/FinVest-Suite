# FinVest Personal Finance Suite

A unified suite of four local-first, privacy-focused personal finance web applications designed to run entirely client-side with no backend, database, or server dependencies. Hosted statically across separate subdomains while sharing a cohesive modern SaaS aesthetic (Stripe / Linear / Vercel style).

---

## 🏛️ Applications

| App | URL | Key Storage Prefix | Key Highlights |
| :--- | :--- | :--- | :--- |
| **Budget & Cashflow** | [finvest.smathur.xyz/money-manager](https://finvest.smathur.xyz/money-manager/) | `finvest_budget_*` | Inflow/outflow tracking, 30+ categories, monthly/annual analytics, category breakdown, cashflow trend. |
| **Retirement Planner** | [finvest.smathur.xyz/retirement-calculator](https://finvest.smathur.xyz/retirement-calculator/) | `finvest_retirement_*` | 500-run Monte Carlo simulation, 10th/50th/90th percentile curves, Trinity Study safe withdrawal rate (SWR) matrix. |
| **Investment Portfolio** | [finvest.smathur.xyz/investments-tracker](https://finvest.smathur.xyz/investments-tracker/) | `finvest_investments_*` | Stocks/ETFs/Alternatives, interactive squarified Treemap heatmap, Finnhub live market quotes API integration. |
| **Net Worth Tracker** | [finvest.smathur.xyz/networth-tracker](https://finvest.smathur.xyz/networth-tracker/) | `finvest_networth_*` | Point-in-time balance snapshots, bi-directional asset/debt balance bars, retirement tracking, 100% stacked composition shift. |

---

## 🛠️ Architectural Consistency

1. **Pure Frontend Static Delivery**:
   - Each app is completely self-contained in its own directory (`finvest-budget/`, `finvest-retirement/`, `finvest-investments/`, `finvest-networth/`).
   - Zero servers, zero databases, zero Node runtime required in production.
   - Deployable anywhere: GitHub Pages, Cloudflare Pages, Vercel Static, Netlify, or AWS S3.

2. **Storage & Data Sovereignty**:
   - Persisted exclusively in browser `localStorage`.
   - Isolated prefixes per app (`finvest_budget_*`, `finvest_retirement_*`, `finvest_investments_*`, `finvest_networth_*`).
   - Shared theme setting: `finvest_theme` (`light` / `dark`).
   - **Unified Data Backup**: Every app contains an Export to JSON and Import from JSON modal to safely backup and restore state.

3. **Unified Navigation & Design System**:
   - Sticky top navigation bar linking to all four applications via absolute URLs with active pill indicators.
   - Tailwind CSS Slate palette with financial accents: Emerald for positive/gains, Rose for expenses/losses, Indigo for primary actions, Amber for retirement.
   - Dark & Light mode toggle in the header.
