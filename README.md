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

For cryptocurrency prices the dashboard can use CoinMarketCap. Provide a CoinMarketCap API key in `index.html` via the `CMC_API_KEY` constant:

```javascript
const CMC_API_KEY = '<YOUR_CMC_KEY>'; // optional
```

If this key is not supplied the app will fall back to CoinGecko's public API.

## Running

The dashboard is a static site. Simply open `index.html` in your browser or serve it via any static file server.
