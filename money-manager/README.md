# FinVest Budget (App 1 of 4)

A modern, responsive, local-first web application for personal budgeting and cashflow management. Built with **React 18**, **Tailwind CSS**, and **Lucide icons**, running 100% client-side with **zero backend dependencies**.

---

## 🚀 Key Highlights & Architectural Conformance

1. **Pure Frontend Static Delivery**:
   - Single-page static app ready to host directly on `https://budget.yourdomain.com` (Cloudflare Pages, Vercel Static, GitHub Pages, Netlify, S3, or any static web host).
   - No backend, API routes, or databases required.

2. **Local-First & Data Persistence**:
   - Stored strictly in browser `localStorage`.
   - Uses the namespace prefix `finvest_budget_*` (`finvest_budget_transactions`, `finvest_budget_categories`, `finvest_theme`).
   - 100% offline-ready & private.

3. **Data Backup & Restore**:
   - **Export**: One-click download of timestamped JSON backup (`finvest-budget-backup-YYYY-MM-DD.json`).
   - **Import**: Validates JSON schema, confirms overwrite with user, and restores transaction ledger & categories.
   - **Demo Mode**: Includes one-click demo data repopulation or data purge.

4. **Unified Navigation & Design System**:
   - Sticky top navigation bar with links across the suite:
     - 📊 **Budget** (Active): `https://budget.yourdomain.com`
     - 🏖️ **Retirement**: `https://retirement.yourdomain.com`
     - 📈 **Investments**: `https://investments.yourdomain.com`
     - 🏛️ **Net Worth**: `https://networth.yourdomain.com`
   - Dark/Light mode toggle with persistence in `finvest_theme`.
   - Linear/Stripe/Vercel aesthetic: Slate neutral scale, Emerald inflows, Rose outflows, Indigo primary accents.

5. **Financial Analytics & Management**:
   - **Metrics**: Total Income, Total Expenses, Net Cashflow (+/-), and Savings Rate %.
   - **Visualizations**: 
     - Income vs. Expenses monthly trend chart (Jan–Dec 2026).
     - Spending by category donut & proportional breakdown with emojis and percentages.
     - Interactive time periods (Monthly & Full Year 2026).
   - **Transaction Management**: Filter by type (All, Expenses, Income), search description/notes, filter by category, sort by date/amount, edit, and delete entries.
   - **Category Customizer**: Custom category builder with 30+ financial emojis and curated color swatches.

---

## 💻 Local Testing & Preview

You can open `index.html` directly in any web browser, or run a local static server:

```bash
cd /Users/sid/.gemini/antigravity/scratch/finvest-budget
python3 -m http.server 3001
```

Then visit:
[http://localhost:3001](http://localhost:3001)
