# Indie Maps
Indie Maps is a single‑page, static mapping utility powered by [MapLibre GL JS](https://maplibre.org) and OpenFreeMap styles. It lets you search for a location, optionally add a second destination, and instantly show a route with distance/ETA—everything wrapped in a retro chrome UI inspired by early-2000s web apps.

## How to use it
- Open `index.html` in any modern browser (it just needs static hosting). The primary search box finds places via Nominatim and drops a marker; the second search (revealed via the `+` button) picks a destination and triggers OSRM directions automatically once both markers exist.
- Search results appear in the shared results list with a little badge denoting start vs. destination. Use the history chips below the list to repeat recent primary searches.
- The status bar at the top keeps you informed about zoom/coords and route metrics, while the units dropdown lets you switch between metric and imperial for distance display.
- If you allow location access, Indie Maps draws a live blue dot that follows you around on the map.
- Clear the active route and both markers with the `Clear route` button; collapsing the second search field does the same while keeping the primary finder available.
## Hosting locally
1. Clone or copy this repository to any folder.
2. Serve the directory over HTTP (any static server works). For example, run `npx http-server . -p 8000` or `python -m http.server 8000` and open `http://localhost:8000`.
3. Once the page loads, search for your start location and tap `+` to add a destination (if needed). The app saves your location choices and units in `localStorage`, so reloading restores your last view.

Alternatively, deploy the same `index.html` to any static hosting solution (Netlify, GitHub Pages, etc.)—no build step is required.

You can try Indie Maps right now at https://indie-maps.com.

## Embedding
Add `&embed=1` to the query string when you want to drop just the map canvas into another site, for example `https://indie-maps.com?s=Adelaide&embed=1`. The toolbar, search rows, and status chrome are hidden while the map still honors the `s=`/`d=` location parameters and routes are calculated as usual.
