# FinVest Personal Finance Suite

A unified suite of four local-first, privacy-focused personal finance web applications designed to run entirely client-side with no backend, database, or server dependencies. Hosted statically across separate subdomains while sharing a cohesive modern SaaS aesthetic (Stripe / Linear / Vercel style).

---

## 🏛️ The 4 Suite Applications

| App | Subdomain URL | Local Port | Key Storage Prefix | Key Highlights |
| :--- | :--- | :--- | :--- | :--- |
| **1. Budget & Cashflow** | `https://budget.yourdomain.com` | `http://localhost:3001` | `finvest_budget_*` | Inflow/outflow tracking, 30+ emoji categories, monthly/annual analytics, category breakdown donut, cashflow trend. |
| **2. Retirement Planner** | `https://retirement.yourdomain.com` | `http://localhost:3002` | `finvest_retirement_*` | 500-run Monte Carlo simulation, 10th/50th/90th percentile curves, Trinity Study safe withdrawal rate (SWR) matrix. |
| **3. Investment Portfolio** | `https://investments.yourdomain.com` | `http://localhost:3003` | `finvest_investments_*` | Stocks/ETFs/Alternatives, interactive squarified Treemap heatmap, Finnhub live market quotes API integration. |
| **4. Net Worth Tracker** | `https://networth.yourdomain.com` | `http://localhost:3004` | `finvest_networth_*` | Point-in-time balance snapshots, bi-directional asset/debt balance bars, retirement tracking, 100% stacked composition shift. |

---

## 🛠️ Global Architectural Standards Followed

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

---

## 🚀 Running the Apps Locally

You can open each `index.html` file directly in your browser, or spin up local test servers:

```bash
# App 1: Budget
cd /Users/sid/.gemini/antigravity/scratch/finvest-budget && python3 -m http.server 3001

# App 2: Retirement
cd /Users/sid/.gemini/antigravity/scratch/finvest-retirement && python3 -m http.server 3002

# App 3: Investments
cd /Users/sid/.gemini/antigravity/scratch/finvest-investments && python3 -m http.server 3003

# App 4: Net Worth
cd /Users/sid/.gemini/antigravity/scratch/finvest-networth && python3 -m http.server 3004
```
