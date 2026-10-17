# FinVest Retirement

A modern, responsive, local-first web application for retirement planning, probabilistic Monte Carlo simulation, and safe withdrawal rate (SWR) longevity modeling. Built with **React 18**, **Tailwind CSS**, and **Lucide icons**, running 100% client-side with **zero backend dependencies**.

---

## 🚀 Key Highlights & Architectural Conformance

1. **Pure Frontend Static Delivery**:
   - Single-page static app ready to host directly on `https://finvest.smathur.xyz/retirement-calculator` (Cloudflare Pages, Vercel Static, GitHub Pages, Netlify, or AWS S3).
   - No backend, API routes, or databases required.

2. **Local-First & Data Persistence**:
   - Stored strictly in browser `localStorage`.
   - Uses the namespace prefix `finvest_retirement_*` (`finvest_retirement_profile`, `finvest_theme`).
   - 100% offline-ready & private.

3. **Data Backup & Restore**:
   - **Export**: One-click download of timestamped JSON backup (`finvest-retirement-backup-YYYY-MM-DD.json`).
   - **Import**: Validates JSON schema, verifies `app === 'finvest_retirement'`, and restores simulation profile.
   - **Reset**: Includes one-click restoration of standard assumptions.

4. **Unified Navigation & Design System**:
   - Sticky top navigation bar linking to all four apps in the suite:
     - 📊 **Budget**: `https://finvest.smathur.xyz/money-manager`
     - 🏖️ **Retirement** (Active): `https://finvest.smathur.xyz/retirement-calculator`
     - 📈 **Investments**: `https://finvest.smathur.xyz/investments-tracker`
     - 🏛️ **Net Worth**: `https://finvest.smathur.xyz/networth-tracker`
   - Dark/Light mode toggle synchronized via `finvest_theme`.
   - Linear/Stripe/Vercel aesthetic: Slate neutral scale, Emerald for success/growth, Amber for warnings/drawdowns, Indigo for primary actions.

5. **Monte Carlo Simulation Engine (500 Iterations)**:
   - **Inputs**:
     - Asset allocation split: Stocks %, Bonds %, Cash % (auto-balancing sliders).
     - Timeline: Current Age, Target Retirement Age, End/Life Expectancy Age.
     - Cash flows: Current portfolio balance, annual savings and wage growth rate, annual retirement expenses, and inflation rate.
   - **Outputs**:
     - Success probability (%) under simulated market conditions.
     - Median (50th percentile) estimated nest egg at retirement.
     - Interactive multi-curve SVG chart displaying **Optimistic (90th %)**, **Median (50th %)**, and **Pessimistic (10th %)** trajectories with confidence cone shading and retirement milestone marker.
     - Interactive hover tooltip to inspect balances at any age.

6. **Withdrawal Rate & Longevity Matrix**:
   - Compares withdrawal rates (3.0%, 3.5%, 4.0%, 4.5%, 5.0%, 6.0%) against Trinity Study benchmarks.
   - Dynamic slider to test any custom withdrawal rate (2.5% to 8.0%).
   - Calculates exact fund longevity in years, depletion age, and annual cash outflow.

7. **Preset Scenarios**:
   - 🚀 **FIRE (Aggressive Early)**: Retire at age 45 with 85% equities.
   - ⚖️ **Standard Balanced**: Age 62 retirement with 75/20/5 allocation.
   - 🛡️ **Conservative Wealth Preservation**: Higher bond allocation for stability.
