# Sales & Revenue Analytics Dashboard

An interactive, browser-based sales intelligence dashboard built with vanilla HTML, CSS, and Chart.js. No build tools or frameworks required — open `index.html` directly in any browser.

## Live Demo

Open `index.html` in your browser — no server needed.

## Features

- **KPI Cards** — Total revenue, order volume, average order value, top category, each with inline sparklines and growth badges
- **Revenue Trend** — Multi-category line chart across 12 months with area fill
- **Category Mix** — Donut chart with percentage breakdown
- **Regional Performance** — Bar chart comparing North / South / East / West
- **Top Products** — Ranked list with inline progress bars and growth indicators
- **Activity Feed** — Real-time-style event log
- **Interactive Filters** — Year, category, and region slicers update all charts simultaneously
- **CSV Export** — Download filtered product data as a CSV
- **Import** — Hook to load your own CSV/Excel data (see Customization)

## Tech Stack

| Layer | Tool |
|---|---|
| Markup | HTML5 |
| Styling | CSS3 (CSS variables, Grid, Flexbox) |
| Charts | [Chart.js 4.4](https://www.chartjs.org/) via CDN |
| Icons | [Tabler Icons](https://tabler-icons.io/) via CDN |
| Fonts | DM Sans + DM Mono (Google Fonts) |

## Getting Started

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/sales-dashboard.git
cd sales-dashboard

# Open in browser (no server needed)
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

## Project Structure

```
sales-dashboard/
├── index.html      # Complete dashboard (self-contained)
└── README.md       # This file
```

## Customization

To plug in real data, replace the `RAW` object inside `index.html`:

```js
const RAW = {
  2024: {
    trend: { Electronics:[...], Apparel:[...], Home:[...], Sports:[...] },
    region: { North:0, South:0, East:0, West:0 },
    products: [{ n:'Product Name', r:100, g:15, c:'Electronics' }, ...]
  }
};
```

For CSV/Excel import support, integrate [PapaParse](https://www.papaparse.com/) (CSV) or [SheetJS](https://sheetjs.com/) (Excel).

## Screenshots

> KPI cards, trend chart, category donut, regional bars, top products table, and activity feed — all updating live with filters.

## Learning Outcomes

- Data visualization fundamentals with Chart.js
- KPI tracking and business metrics design
- Interactive filtering with vanilla JS
- Responsive dashboard layout with CSS Grid
- Business insight generation from sales data

## License

MIT — free to use, modify, and distribute.
