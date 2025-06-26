# Dashboard

This project contains a simple analytics dashboard that pulls economic data from the [FRED](https://fred.stlouisfed.org/) API along with other informational widgets.

## Setup

To fetch data from FRED, the application requires a FRED API key. The key is referenced in `index.html` via the `FRED_API_KEY` constant:

```javascript
const FRED_API_KEY = '<YOUR_FRED_KEY>'; // replace with your key
```

Provide your key in one of the following ways:

1. **Manual edit** – replace `<YOUR_FRED_KEY>` in `index.html` with your actual key.
2. **Environment variable** – set an environment variable named `FRED_API_KEY` and inject it into `index.html` during your build or deploy process.

If you use an automated build, create a script that reads `FRED_API_KEY` from the environment and replaces the placeholder before serving the page.

### Sports Page

The original sports widget has been replaced with a dedicated
`sports.html` page that loads football, NFL and tennis data from open
APIs via a CORS proxy. The page falls back to mock data if the requests
fail, so no API key is required to view scores.

### Exchange Rate API

Costa Rica economy data requires access to the free
[exchangerate.host](https://exchangerate.host/) service. The dashboard uses this
API to pull the USD to CRC conversion rate via client-side requests.


## Running

The dashboard is a static site. Simply open `index.html` in your browser or serve it via any static file server.
