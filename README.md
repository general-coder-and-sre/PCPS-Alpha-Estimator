# Civil Service Pension Estimator

An interactive, client-side web application designed to help UK Civil Service employees estimate and visualize their pension benefits. It supports the legacy **PCPS** (Classic, Premium, Classic Plus) schemes, the modern **Alpha** scheme, and calculates **Combined Total Benefits** if you have service across both schemes.

## 🚀 Live Demo / Getting Started
Since this project is built entirely using standard HTML5, CSS3, and JavaScript, there are no backend servers, database configurations, or build steps required.

To run the estimator:
1. Clone or download this repository.
2. Open `combi/index.html` in any modern web browser.

---

## 🌟 Key Features

### 1. Comprehensive Scheme Support
*   **PCPS Schemes**: Estimate benefits for **Classic**, **Premium**, or **Classic Plus** configurations.
    *   **Classic**: Calculates pension based on $1/80\text{th}$ of final pensionable earnings per year of service, with an automatic $3/80\text{ths}$ tax-free lump sum.
    *   **Premium**: Calculates pension based on $1/60\text{th}$ of final pensionable earnings per year of service.
    *   **Classic Plus**: Handles the split service model, automatically applying Classic rules to service before 1 October 2002 and Premium rules to service on or after that date.
*   **Alpha Scheme**: Simulates Alpha's career average revalued earnings (CARE) structure.
    *   Accrues at $2.32\%$ of pensionable earnings each year.
    *   Allows inputting your last Annual Benefit Statement (ABS) balance as a baseline.
    *   Supports entering pensionable earnings and custom Consumer Price Index (CPI) revaluation rates for up to three future years to model near-term projections.

### 2. Precise Early Retirement Adjustments
*   Calculates reductions using factors derived from the Government Actuary's Department (GAD) Consolidated Tables (Table 1-406 & 1-407).
*   Early retirement is calculated using your age in **complete years and completed months** (part months are discarded), matching official scheme calculation methodologies.

### 3. Flexible Pension Commutation
*   **PCPS (Premium / Classic Plus)**: Adjust your pension using a dynamic slider to exchange pension for an additional lump sum up to the maximum permitted scheme limit, using the standard £1 pension to £12 lump sum rate.
*   **Alpha**: Adjust your lump sum using a percentage slider (0% to 25% of total benefit value) to commute annual pension at a £1:£12 exchange rate.
*   Both results dynamically update the projected values and visual charts in real time.

### 4. Combined Total Benefits Dashboard
*   Aggregates both PCPS and Alpha benefits into a single unified summary.
*   **Monthly Income Breakdown**: Calculates your Gross Monthly Pension and estimates your **Net Monthly Pension** under the standard UK **1257L tax code** (taking into account personal allowance and tax bands).
*   **Visualizations**: Automatically generates clean, interactive doughnut and stacked-bar charts (powered by Chart.js) comparing PCPS and Alpha pension and lump sum components.

### 5. Smart Math Expression Inputs
*   Earnings and pay input fields accept both standard numbers and custom mathematical expressions (e.g. `(30000*(2/12)) + (32000*(10/12))` or `2500*12`).
*   This makes it easy to calculate pro-rata salary adjustments or mid-year pay raises.
*   Input parsing automatically handles various multiplication operators (`*`, `x`, `X`, `×`) for ease of use across mobile and desktop virtual keyboards.

### 6. Privacy & Offline-First Design
*   **No Server Transmissions**: All calculations are executed locally in your web browser. No data ever leaves your device.
*   **Auto-Save Progress**: Uses `localStorage` to save your inputs so you can refresh or revisit the page later without re-entering your numbers.

---

## 📂 Project Structure

*   📁 **`combi/`**
    *   `index.html`: The main, production-ready combined PCPS & Alpha Pension Estimator.
*   📁 **`PCPS/`**
    *   `index.html`: Focused legacy PCPS scheme calculator.
*   `alpha.html`, `alpha2.html`, etc.: Specific standalone iterations for the Alpha scheme.
*   📁 **`combiOld/`**
    *   Archive containing previous developer iterations and testing layouts.

---

## 🛠️ Technology Stack
*   **Structure & Layout**: Semantic HTML5.
*   **Styling**: Custom CSS3, responsive flexbox layout, and CSS variables for a clean, professional aesthetic.
*   **Logic**: Vanilla JavaScript (ES6+).
*   **Charts**: [Chart.js](https://www.chartjs.org/) (loaded via CDN).

---

## ⚠️ Disclaimer
This tool is entirely unofficial and is intended for illustrative and educational purposes only. The estimates produced are not a guarantee of benefits. Users should check their official Annual Benefit Statements (ABS) or consult the official Civil Service Pension Scheme calculators/modellers for verified figures. This tool does not constitute financial advice.
