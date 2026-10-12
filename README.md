# Privacy Policy

**Last updated:** October 10, 2026

Patrick Roy ("we", "us", or "our") operates the Tromi mobile application ("the App"). This Privacy Policy explains what information the App accesses, how it is used, and your choices.

## Information We Collect

### Location Data

The App requests access to your device's location (precise/GPS or approximate) to:

- Show gas stations and EV charging stations near you on the map
- Calculate distances to stations
- Sort stations by proximity
- Display nearby stations on Android Auto
- Start a new trip in the trip planner from where you are

Location data is processed on your device and is **not** transmitted to our servers. It leaves your device only through the trip planner, as described under Network Requests below: a new trip starts from your current position, whose coordinates are sent to OpenStreetMap Nominatim to fetch a readable place name, and the coordinates of your trip stops are sent to OpenRouteService when you tap "Compute". If you deny location permission, the App falls back to a default postal code you can configure in Settings.

### Network Requests

The App fetches publicly available data from the following sources:

| Source | Data | What is sent |
|--------|------|-------------|
| Régie de l'énergie du Québec | Gas station prices | Standard HTTP headers only |
| Le Circuit électrique | EV charger locations | Standard HTTP headers only |
| Open Charge Map | EV charger locations | Geographic bounding box (not your exact location); the request also carries an API key that authenticates the app, not you |
| OpenStreetMap (Overpass API) | Station amenities and park entry points (welcome/visitor-center nodes) | Geographic bounding box (not your exact location) |
| Société des traversiers du Québec | Ferry schedules (GTFS) | Standard HTTP headers only |
| Transports et Mobilité durable Québec | Highway rest areas | Standard HTTP headers only |
| Tourisme Québec / Données Québec | Tourist attractions (SIT Québec) | Standard HTTP headers only |
| Ministère des Ressources naturelles et des Forêts du Québec | Parks (TRQ_100k) and per-park polygon geometry | Standard HTTP headers only |
| Wikipedia (REST summary) | Park descriptions | Article title only (e.g. "Parc national de la Gaspésie") plus an app-identifying User-Agent header, as Wikimedia policy requires |
| OpenRouteService | Driving directions and stop-order optimization for the multi-stop trip planner | Coordinates of the trip stops you have chosen (and only when you tap "Compute"); the request also carries an API key that authenticates the app, not you |
| OpenStreetMap (Nominatim) | Place labels for trip stops, and looking up a contact's address for the trip planner | The coordinates of a trip stop placed from a location — one you drop on the map or place via GPS, including the automatic starting stop of a new trip, which uses your current position when location is enabled (to fetch a readable place name); or the postal address text of a contact you explicitly pick (to convert it to map coordinates). Sent only for those trip-stop actions, plus an app-identifying User-Agent header |
| Statistics Canada (WDS) | Monthly average retail gasoline prices (Montréal + Québec for regular, premium and diesel, plus the Canada average for regular) for the in-app Gas Prices chart | Standard HTTP headers only (a request for the public price table) |
| OpenFreeMap | Vector map tiles for the map display | Standard HTTP headers and the map tile coordinates needed to render the area you are viewing |

No personal information or device identifiers are sent to these services, and your location is sent only as trip-stop coordinates to Nominatim and OpenRouteService, as described here. Geographic bounding boxes used in API queries cover broad areas and cannot identify individual users. Trip-planner requests to OpenRouteService include the coordinates of the stops you assembled — these are only sent on explicit "Compute" actions, are not associated with any account or identifier, and are not stored beyond what OpenRouteService logs to operate the service. Requests to Nominatim (OpenStreetMap) are made only when a trip stop is placed from a location — when you drop or GPS-locate a stop, and automatically for a new trip's starting stop when location is enabled (the stop's coordinates are sent to fetch a readable label) — or when you use the trip planner's "Choose a contact" option (the chosen contact's postal address is sent to convert it to coordinates). They carry no account or identifier. The Wikipedia, Nominatim, and Overpass User-Agent identifies the app and its current version (e.g. "Tromi/1.x") plus a public Google Play Store URL — it does not include any user data.

To keep cached data, price alerts, and the home-screen widget current, the App also repeats these public-data requests periodically in the background (by default about every 12 hours, adjustable in Settings) using Android's WorkManager. Background refreshes fetch only the public datasets for the layers you have enabled — they send no location.

### Contacts

The trip planner's optional "Choose a contact" feature uses Android's built-in, permission-free contact picker: the system shows your contact list, and only the single postal address you tap is handed back to the App. The App **never** requests the contacts permission and cannot read your contact list — it only receives the one address you choose, which it then forward-geocodes via Nominatim (see above) to place a trip stop. The address is not stored beyond the trip stop's resulting coordinates and label.

### External Links and Navigation Apps

Some screens open external web pages in a browser tab (Chrome Custom Tab) — for example the Québec 511 road-conditions map, EV incentive program pages, Statistics Canada, park, attraction and scenic-route web pages, and the data-source credits. Those pages are loaded by your browser and governed by the respective site's own privacy policy; the App passes them nothing beyond the link itself. When you choose to navigate to a station, park, or trip stop, the App hands that destination's coordinates and name to the navigation app you use (e.g. Google Maps or Waze), which applies its own privacy policy.

### Locally Stored Data

The following data is stored on your device only, using Android's Room database and DataStore:

- Favorites (gas stations, EV chargers, ferry routes, rest areas, tourist attractions, parks)
- App settings and preferences (display mode, language, search radius, default postal code / location)
- Cached station, charger, ferry, rest-area, attraction, and park data
- Cached park boundary polygons fetched on demand
- Cached park entry points (welcome/visitor-center locations from OpenStreetMap)
- Cached Wikipedia park descriptions (article snippet + URL)
- Price history snapshots (30 days)
- Saved multi-stop trip plans (stops + computed road polyline + per-leg distance/duration, plus any non-routed places you keep on the trip)
- Price alert configurations
- Cached Statistics Canada gas-price chart data
- The last OpenRouteService quota reading (the shared daily request budget shown in the trip planner)
- The station chosen for each home-screen price widget

This data is **never** transmitted off your device, apart from the trip-stop coordinates sent for routing and place names as described under Network Requests.

## Information We Do Not Collect

- We do not collect personal information (name, email, phone number)
- We do not require account creation or login
- We do not use analytics, crash reporting, or telemetry services
- We do not display advertisements
- We do not use cookies or tracking technologies
- We do not sell, share, or transfer any user data to third parties

## Notifications

The App may request permission to send local notifications for price alerts you configure. These notifications are generated entirely on your device — no push notification service is involved.

## Android Auto

The App declares the `androidx.car.app.MAP_TEMPLATES` permission so it can display nearby stations and your active trip on an Android Auto screen. This permission grants access to car-screen templates only — it does not collect any data from you or your vehicle.

## Children's Privacy

The App does not knowingly collect any personal information from anyone, including children under 13. Since the App collects no personal data, it complies with the Children's Online Privacy Protection Act (COPPA) and similar regulations.

## Data Retention

All data is stored locally on your device. Uninstalling the App removes all stored data. Price history snapshots are automatically pruned after 30 days.

## Changes to This Policy

We may update this Privacy Policy from time to time. Changes will be posted within the App or on this page with an updated revision date.

## Contact Us

If you have questions about this Privacy Policy, you can contact us at:

**Email:** patrick.roy07@gmail.com
