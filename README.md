# NYC walk-radius map: 620 Avenue of the Americas

An interactive map of where you can live within a **15-minute walk (as Google Maps shows it)** of 620 Avenue of the Americas (6th Ave between W 18th & W 19th St), Manhattan.

Open `index.html` in a browser.

## What it shows

- **Walk-time bands** (≤5, 6–10, 11–15 min) and a bold **qualifying line** where Google Maps flips from 15 to 16 min.
- **32 spot checks**: dots labelled with the actual Google Maps walking time to each intersection, collected Nov 20, 2026.
- **Address checker**: type an address or click the map. It estimates the Google Maps walking time (faster of the two directions) and links to Google Maps to confirm.
- **StreetEasy link**: [rentals inside the 15-minute shape](https://streeteasy.com/for-rent/nyc/boundary:Custom%20Boundary-kuuwFn%7BqbMCfElI~p%40dItk%40nAvBtCdAzs%40oOrHRfEyAvHeLwHwj%40ToKs%40oKgDgEcE_XeBgBgBy%40wj%40pL%7D%60%40nO%7Cin_rect:40.728,40.753,-74.010,-73.980). StreetEasy saves a drawn search area in the URL as a Google-encoded polyline, so the shape is simplified to 18 points and encoded the same way. It still puts all 32 spot checks on the right side.
- Neighborhood recommendations and the nearby areas that fall just outside.

## How it's calibrated

Routes come from the [Valhalla](https://github.com/valhalla/valhalla) router on OpenStreetMap data, via the public FOSSGIS server. Google Maps walks about 10% slower than a generic 3 mph. So the router's walking speed is set to 4.3 km/h (about 2.7 mph), which matched Google's displayed minutes at 32 test intersections (RMSE ≈ 0.4 min). The 15-minute line puts all 32 on the same side of the limit as Google. Near the line, always confirm a specific building in Google Maps.

## Data & credits

- Map tiles and data © [OpenStreetMap](https://www.openstreetmap.org/copyright) contributors
- Routing: Valhalla (valhalla1.openstreetmap.de); geocoding: Nominatim
- Map library: [Leaflet](https://leafletjs.com)
