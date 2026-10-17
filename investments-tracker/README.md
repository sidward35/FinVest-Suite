# FinVest Investments

A modern, responsive, local-first web application for point-in-time investment portfolio tracking, interactive treemap heatmaps, and live market quotes via the Finnhub API. Built with **React 18**, **Tailwind CSS**, and **Lucide icons**, running 100% client-side with **zero backend dependencies**.

---

## 🚀 Key Highlights & Architectural Conformance

1. **Pure Frontend Static Delivery**:
   - Single-page static app ready to host directly on `https://finvest.smathur.xyz/investments-tracker` (Cloudflare Pages, Vercel Static, GitHub Pages, Netlify, or AWS S3).
   - No backend, API routes, or databases required.

2. **Local-First & Data Persistence**:
   - Stored strictly in browser `localStorage`.
   - Uses the namespace prefix `finvest_investments_*` (`finvest_investments_assets`, `finvest_investments_finnhub_key`, `finvest_theme`).
   - 100% offline-ready & private.

3. **Data Backup & Restore**:
   - **Export**: One-click download of timestamped JSON backup (`finvest-investments-backup-YYYY-MM-DD.json`).
   - **Import**: Validates JSON schema, verifies `app === 'finvest_investments'`, and restores positions and settings.
   - **Reset**: Includes one-click restoration of sample demo portfolio.

4. **Unified Navigation & Design System**:
   - Sticky top navigation bar linking to all four apps in the suite:
     - 📊 **Budget**: `https://finvest.smathur.xyz/money-manager`
     - 🏖️ **Retirement**: `https://finvest.smathur.xyz/retirement-calculator`
     - 📈 **Investments** (Active): `https://finvest.smathur.xyz/investments-tracker`
     - 🏛️ **Net Worth**: `https://finvest.smathur.xyz/networth-tracker`
   - Dark/Light mode toggle synchronized via `finvest_theme`.
   - Linear/Stripe/Vercel aesthetic: Slate neutral scale, Emerald for gains, Crimson/Rose for losses, Indigo for primary actions.

5. **Multi-Asset Management**:
   - Categorized by **Stocks**, **ETFs**, and **Alternative Assets** (Crypto, Physical Gold, Private Real Estate).
   - Fields: Ticker symbol, custom asset name, quantity (shares/units), cost basis per share, current price, and notes.
   - Modal to add, edit, or delete holdings.

6. **Interactive Treemap Heatmap**:
   - Proportional squarified binary-space partitioning (BSP) treemap where rectangle sizes scale by current asset value.
   - Dynamically color-coded by unrealized percentage gain/loss vs. cost basis (Deep Emerald for +40% gains to Deep Crimson for -25%+ drawdowns).
   - Category filtering: Isolate *All Assets*, *Stocks Only*, *ETFs Only*, or *Alternatives Only*.
   - Interactive hover overlay showing complete breakdown (quantity, cost basis, current price, total value, unrealized P&L).
   - One-click tile editing.

7. **Finnhub Live Market Quotes API Integration**:
   - Connect your own free Finnhub API token via the navbar settings dialog.
   - One-click "Fetch Live Quotes" batch queries Finnhub (`https://finnhub.io/api/v1/quote`) with polite rate throttling to update real-time stock/ETF prices and calculate portfolio change.
   - Includes an offline/simulated tick generator for testing without an active API key.
   