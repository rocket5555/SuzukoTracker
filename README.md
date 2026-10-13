# SuzukoTracker

**SuzukoTracker** is a fast, zero-dependency web application built to track part-time work hours under Japan's **28-hour weekly student visa limit** alongside detailed **taxable vs. tax-free earnings** calculations.

Designed with a high-contrast **True Black (`#000000`) OLED interface**, it runs entirely in a single `index.html` file with real-time **Firebase Cloud Sync**, **Local Guest Mode**, and full **JSON/CSV** portability.

---

## ✨ Key Features

### 🛡️ Student Visa Compliance Engine
* **True Rolling 7-Day Bottleneck Tracking:** Japanese Immigration evaluates the 28-hour limit across *any* rolling 7-day window, not just Monday–Sunday calendar weeks. SuzukoTracker inspects all **7 intersecting 7-day windows** around your selected shift date and highlights the exact bottleneck window.
* **Daily 8-Hour Cap Enforcement:** Automatically validates shifts against the legal 8-hour daily maximum.
* **🌴 School Holiday Mode (40h/Week):** Configure official school vacation periods (Summer, Winter, Spring break) to automatically expand the rolling weekly limit from **28h to 40h**, or toggle it manually.
* **📊 7-Day Capacity Forecast (Shift Optimizer):** Forecasts your remaining legal work capacity for each of the next 7 days and recommends the best days to pick up shifts. Click any forecast card to jump directly to that date.

### 💰 Earnings, Day Rates & Tax Breakdown
* **Dual Pay Structures:**
  * **⏱ Hourly Wage:** Automatically calculates regular hours and applies the mandatory **+25% Late-Night premium** for hours worked between **22:00 and 05:00**.
  * **📅 Day Rate (Fixed Daily Pay):** Enter a flat daily amount earned without needing to divide by hours worked, while still logging shift times toward your 28-hour visa limit.
* **🧾 Taxable vs. Tax-Free Transportation View:**
  * **Combined Mode (Normal):** Displays your all-in take-home pay (or customize whether net transportation and additional earnings are combined with base wage).
  * **Tax & Breakdown View:** Separates **Base Wage (Taxable)** and **Additional Earnings** from **Tax-Free Transportation Subsidies** and **Out-of-Pocket Transport Costs**—making year-end tax and income checks effortless.

### ⚡ High-Speed Workflow & UX
* **Saved Job Presets:** Save, load, edit (`✎`), and delete (`✕`) presets for recurring shifts, storing location, times, break duration, pay mode (Hourly or Day Rate), wage, transportation, and bonuses.
* **120fps GPU Drum Time Picker:** Hardware-accelerated `translate3d` time picker engineered for desktop mice and trackpads:
  * Smooth mouse wheel velocity scaling, click-and-drag, or direct click selection.
  * Context-aware quick buttons (`:00`, `:15`, `:30`, `:45` for shift times; `0m`, `30m`, `45m`, `1h` for breaks).
  * **Direct Keyboard Typing:** Type 4 digits while the picker is open (e.g., `1730` → `17:30`) and press `Enter` to confirm.
* **Zero-Horizontal-Scroll Table:** Fixed-proportion tabular layout with weekday badges, expandable shift breakdowns, location search, and Year/Month filtering.

### ☁️ Cloud Sync & Data Portability
* **Firebase Authentication & Firestore Sync:** Sign in with Email/Password or Google to sync shifts, presets, and holidays across PC and mobile.
* **Offline Guest Mode:** Use the app 100% offline via browser `localStorage`.
* **JSON & CSV Backups:** Export your entire database to a `.json` backup file (fully backward-compatible with legacy SuzukoTracker backups) or export shift logs to `.csv` for Excel/Google Sheets.
