# NYC walk-radius map: 620 Avenue of the Americas or 18 W 18th St

An interactive map of where you can live within a **15-minute walk (as Google Maps shows it)** of either office: 620 Avenue of the Americas (6th Ave between W 18th & W 19th St) or 18 W 18th St (just west of 5th Ave), Manhattan. Either one counts, so the area is the union of the two walks.

Open `index.html` in a browser.

## What it shows

- **Walk-time bands** (≤5, 6–10, 11–15 min) and a bold **qualifying line** where Google Maps flips from 15 to 16 min, to whichever office is closer.
- **48 spot checks** at 32 intersections: dots labelled with the actual Google Maps walking time to the closer office, collected Nov 20–21, 2026.
- **Address checker**: type an address or click the map. It estimates the Google Maps walking time (fastest of both directions to both offices) and links to Google Maps to confirm.
- **StreetEasy link**: [rentals inside the 15-minute shape](https://streeteasy.com/for-rent/nyc/boundary:Custom%20Boundary-meuwFjtqbMRmExJyFvQqCnd%40mLpCv%40%7CAzDzBnP%7CBfE%5EfEfBlDjChLIzCqBtAjAlPnBnK_GbCrBjOa%40lAiEdEkApCgExAsHScHvBmSdCyIfDoKhBgEoBqTc%60BBgEl%40g%40nM%7BD%7Cin_rect:40.729,40.751,-74.008,-73.980). StreetEasy saves a drawn search area in the URL as a Google-encoded polyline, so the shape is simplified to 32 points and encoded the same way. It still puts all 32 intersections on the right side.
- Neighborhood recommendations and the nearby areas that fall just outside.

## How it's calibrated

Routes come from the [Valhalla](https://github.com/valhalla/valhalla) router on OpenStreetMap data, via the public FOSSGIS server. Google Maps walks about 10% slower than a generic 3 mph. So the router's walking speed is set to 4.3 km/h (about 2.7 mph), which matched Google's displayed minutes at 48 checks (typically within ±0.5 min). The 15-minute line puts every check on the same side of the limit as Google. Near the line, always confirm a specific building in Google Maps.

## Data & credits

- Map tiles and data © [OpenStreetMap](https://www.openstreetmap.org/copyright) contributors
- Routing: Valhalla (valhalla1.openstreetmap.de); geocoding: Nominatim
- Map library: [Leaflet](https://leafletjs.com)
