# SaaS M&A Tracker

A live tracker for SaaS mergers and acquisitions from 2022 to present, powered by Google Sheets data.

## Installation & Usage

This is a single-page web application that requires no build process or dependencies. There are several ways to use it:

### Option 1: Open Directly in Browser

The simplest method - just open the file:

```bash
# On Linux
xdg-open index.html

# On macOS
open index.html

# On Windows
start index.html
```

Or simply double-click `index.html` in your file explorer.

### Option 2: Run a Local Web Server

For better performance and to avoid CORS issues, serve it with a local web server:

**Using Python 3:**
```bash
python3 -m http.server 8000
```

**Using Python 2:**
```bash
python -m SimpleHTTPServer 8000
```

**Using Node.js (npx):**
```bash
npx http-server -p 8000
```

**Using PHP:**
```bash
php -S localhost:8000
```

Then open `http://localhost:8000` in your browser.

### Option 3: Deploy to a Web Server

Upload `index.html` to any web hosting service:

- GitHub Pages
- Netlify
- Vercel
- AWS S3 + CloudFront
- Any traditional web host

The app will work immediately - no build process required.

## Features

- **Live Data**: Automatically fetches data from Google Sheets
- **Search**: Filter by target, acquirer, ticker, or description
- **Filters**: Filter by year, deal type, and status
- **Sorting**: Click column headers to sort
- **Responsive**: Works on desktop and mobile

## Data Source

The application pulls live data from a published Google Sheets CSV. The data includes:
- Deal announcement dates
- Target and acquirer companies
- Deal values
- Deal types (PE, Strategic, etc.)
- Deal status
- Press releases and SEC filings

## Requirements

- Any modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection (to fetch live data from Google Sheets)

## Customization

To use your own Google Sheets data:

1. Create a Google Sheet with the following columns:
   - Date
   - Target
   - Acquirer
   - Deal_Value
   - Acquirer_Type
   - Status
   - Ticker
   - Press_Release
   - Proxy
   - Other_Link
   - Description

2. Publish the sheet as CSV (File → Share → Publish to web → CSV)

3. Replace the `CSV_URL` in `index.html` (line 137-138) with your published CSV URL

## License

This project is open source and available for use and modification.
