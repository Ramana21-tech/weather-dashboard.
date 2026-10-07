# Weather Dashboard

A weather dashboard that shows live data for Chennai, Tiruchirappalli, Mumbai and Delhi, deployed automatically with GitHub Actions.

**Live site:** https://YOUR-USERNAME.github.io/weather-dashboard/

## How it works

OpenWeatherMap API → GitHub Actions (key in Secrets) → weather.json → GitHub Pages

1. A GitHub Actions workflow runs on every push and every 3 hours.
2. It calls the OpenWeatherMap API using a key stored in GitHub Secrets.
3. The results are saved as `weather.json` and deployed with `index.html` to GitHub Pages.
4. The page reads `weather.json` and displays one card per city.

## Security

The API key is stored as the repository secret `WEATHER_API_KEY`. It never appears in the source code or on the website.

## Tech

HTML, CSS, JavaScript, GitHub Actions, GitHub Pages, OpenWeatherMap API

## Setup

1. Get a free API key from openweathermap.org
2. Add it under Settings → Secrets and variables → Actions as `WEATHER_API_KEY`
3. Set Settings → Pages → Source to GitHub Actions
4. Push to `main`, or run the workflow manually from the Actions tab
