# AHD Dashboard

AHD Dashboard is a single-page HTML application that aggregates economic, climate, crypto, sports, and news data in one place. It uses public APIs including FRED for economic indicators, CoinGecko for cryptocurrency prices, Open-Meteo for weather, and various news sources. The dashboard is meant for quick personal reference and experimentation.

## Requirements

* Modern web browser with JavaScript enabled.
* A valid FRED API key. The current `index.html` ships with a demo key but you may override it with your own.

## Usage

1. Clone the repository.
2. Optionally replace the value of `FRED_API_KEY` in `index.html` with your own key or expose a global `FRED_API_KEY` variable before loading the page.
3. Serve the project using a simple web server and open the dashboard in your browser.

### Running locally

You can use Python's built-in web server:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000/index.html` in your browser.

The `news.html` page can also be viewed directly from the same server for a simplified news-only view.

## Environment Variables

Only the FRED API currently requires authentication. Replace the placeholder key in `index.html` or expose a global `FRED_API_KEY` variable if you prefer not to edit the file.

---

This project is intentionally lightweight and does not require a build step or any dependencies.
