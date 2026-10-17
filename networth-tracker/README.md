# FinVest Net Worth Tracker

A modern, responsive, local-first web application for tracking personal net worth, balance sheet expansion, and retirement savings pacing over time. Built with **React 18**, **Tailwind CSS**, and **Lucide icons**, running 100% client-side with **zero backend dependencies**.

---

## 🚀 Key Highlights & Architectural Conformance

1. **Pure Frontend Static Delivery**:
   - Single-page static app ready to host directly on `https://finvest.smathur.xyz/networth-tracker` (Cloudflare Pages, Vercel Static, GitHub Pages, Netlify, or AWS S3).
   - No backend, API routes, or databases required.

2. **Local-First & Data Persistence**:
   - Stored strictly in browser `localStorage`.
   - Uses the namespace prefix `finvest_networth_*` (`finvest_networth_accounts`, `finvest_networth_snapshots`, `finvest_theme`).
   - 100% offline-ready & private.

3. **Data Backup & Restore**:
   - **Export**: One-click download of timestamped JSON backup (`finvest-networth-backup-YYYY-MM-DD.json`).
   - **Import**: Validates JSON schema, verifies `app === 'finvest_networth'`, and restores accounts and snapshots.
   - **Reset**: Includes one-click restoration of sample demo balance sheet.

4. **Unified Navigation & Design System**:
   - Sticky top navigation bar linking to all four apps in the suite:
     - 📊 **Budget**: `https://finvest.smathur.xyz/money-manager`
     - 🏖️ **Retirement**: `https://finvest.smathur.xyz/retirement-calculator`
     - 📈 **Investments**: `https://finvest.smathur.xyz/investments-tracker`
     - 🏛️ **Net Worth** (Active): `https://finvest.smathur.xyz/networth-tracker`
   - Dark/Light mode toggle synchronized via `finvest_theme`.
   - Linear/Stripe/Vercel aesthetic: Slate neutral scale, Emerald for assets/surplus, Rose for liabilities/debt, Indigo for primary actions.

5. **Account & Snapshot Management**:
   - **Accounts Directory**: Add/edit custom accounts designated as **Asset** or **Liability**, categorized by cash, retirement, taxable brokerage, real estate, crypto, mortgage, auto loan, credit card, etc.
   - **Retirement Tagging**: Checkbox to tag specific asset accounts as "Retirement Account" (401k, Traditional/Roth IRA, HSA).
   - **Snapshot Recording**: Fast point-in-time balance recorder pre-filled with previous balances and optional memos.

6. **Comprehensive Visualizations**:
   - 📈 **1. Net Worth Over Time**: Smoothed dynamic area/line chart tracking historical net worth across date snapshots with milestone points.
   - 🏖️ **2. Retirement Tracker Trendline**: Dedicated trajectory line tracking the combined balances of all retirement-tagged accounts.
   - 🥧 **3. Asset vs. Liability Split**: Proportional donut/pie split of total assets vs. total liabilities for the latest snapshot, including debt-to-asset solvency metrics.
   - 📊 **4. Bi-Directional Cashflow / Balance Bar Chart**: Assets plotted above the horizontal X-axis (Emerald), Liabilities plotted below the X-axis (Rose).
   - 🗂️ **5. Stacked Percentage Bar Chart (100% Composition Shift)**: Visualizes how asset allocation percentages (Cash, Retirement, Brokerage, Real Estate, Crypto) have shifted across snapshot dates.

7. **Historical Ledger Table**:
   - Filter, sort, inspect, edit, or delete any past snapshot record.
