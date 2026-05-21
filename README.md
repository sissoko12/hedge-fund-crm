# Argent Capital — Hedge Fund CRM

A professional, fully client-side Investor Relations CRM built as a single HTML file. Designed for hedge funds and alternative asset managers to manage LP relationships, fundraising pipelines, and fund reporting — with zero dependencies, no backend, and no setup required.

## Demo

Open `hedge_fund_crm.html` in any modern browser and it works instantly.

> **Live site (if hosted on GitHub Pages):**
> `https://YOUR_USERNAME.github.io/hedge-fund-crm/hedge_fund_crm.html`

---

## Features

### Investor Management
- **LP Directory** — searchable, filterable, sortable roster of 16+ investors with status badges and tier classification
- **Detail Panel** — click any LP to open a slide-in panel with full profile, interaction history, and a log interaction button
- **Add Investor** — modal form to onboard new LPs with type, geography, commitment size, pipeline stage, and notes

### Fundraising
- **Pipeline View** — track prospects across stages (Initial Intro → First Meeting → Due Diligence → Soft Circle → Close) with target size, probability, and expected close date
- **Capital Pipeline Widget** — visual bar chart of committed capital by stage

### Operations
- **Interaction Log** — chronological record of all calls, emails, and meetings across all investors
- **Fund Overview** — 4-fund dashboard with AUM, net IRR, TVPI, deployment progress, and close timelines
- **Document Vault** — categorized document library (PPM, DDQ, legal, reports) with access controls
- **Roadshows** — global event tracker with meeting count and AUM potential per city
- **Reporting** — scheduled report tracker with due dates, recipients, and status

### UX & Design
- Dark / Light theme toggle
- Live search across all investors
- Status filter tabs (All / Active / Prospects / Soft Circle / Inactive)
- Column sorting (Type, Commitment, Status)
- CSV export of the full LP roster
- Toast notifications for all actions
- Fully responsive layout

---

## Tech Stack

| Layer | Choice |
|---|---|
| Framework | Vanilla HTML / CSS / JavaScript |
| Icons | Tabler Icons (CDN) |
| Fonts | DM Sans + DM Mono (Google Fonts) |
| Backend | None |
| Database | None (in-memory JS array) |
| Dependencies | None (besides CDN fonts/icons) |

---

## Getting Started

### Run locally

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/hedge-fund-crm.git
cd hedge-fund-crm

# Open in browser (macOS)
open hedge_fund_crm.html

# Open in browser (Windows)
start hedge_fund_crm.html

# Open in browser (Linux)
xdg-open hedge_fund_crm.html
```

No npm install. No build step. No server needed.

### Deploy to GitHub Pages

1. Go to your repo → **Settings** → **Pages**
2. Under *Source*, select `main` branch → **Save**
3. Your CRM will be live at:
   ```
   https://YOUR_USERNAME.github.io/hedge-fund-crm/hedge_fund_crm.html
   ```

---

## Project Structure

```
hedge-fund-crm/
├── hedge_fund_crm.html   # Entire application (HTML + CSS + JS)
└── README.md
```

---

## Customization

All investor data lives in the `lpData` array at the top of the `<script>` block inside `hedge_fund_crm.html`. Edit it to replace the sample data with real investors:

```js
const lpData = [
  {
    initials: 'OT',
    avClass:  'av-green',
    name:     "Ontario Teachers' Pension",
    sub:      'Canada',
    type:     'Pension',
    aum:      '$220M',
    status:   'Active',       // Active | Prospect | Soft Circle | Inactive
    geo:      'North America',
    last:     'May 13',
    tier:     'Tier 1',       // Tier 1 | Tier 2 | Tier 3
  },
  // ...
];
```

To persist data across sessions, the array can be replaced with `localStorage` or connected to a backend API.

---

## Roadmap

- [ ] Persistent storage via `localStorage`
- [ ] REST API integration (Airtable / Supabase)
- [ ] LP portal login + role-based access
- [ ] Charts for AUM over time and geographic breakdown
- [ ] Calendar integration for roadshow scheduling
- [ ] PDF export for LP reports
- [ ] Email integration (send directly from CRM)

---

## License

MIT — free to use, modify, and distribute.

---

*Built with Claude · Argent Capital CRM v1.0*
