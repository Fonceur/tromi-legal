# Privacy Policy

**Last updated:** June 20, 2026

Patrick Roy ("we", "us", or "our") operates the Tromi mobile application ("the App"). This Privacy Policy explains what information the App accesses, how it is used, and your choices.

## Information We Collect

### Location Data

The App requests access to your device's location (precise/GPS or approximate) to:

- Show gas stations and EV charging stations near you on the map
- Calculate distances to stations
- Sort stations by proximity
- Display nearby stations on Android Auto

Location data is processed entirely on your device. It is **not** transmitted to our servers or shared with any third party. If you deny location permission, the App falls back to a default postal code you can configure in Settings.

### Network Requests

The App fetches publicly available data from the following sources:

| Source | Data | What is sent |
|--------|------|-------------|
| Régie de l'énergie du Québec | Gas station prices | Standard HTTP headers only |
| Le Circuit électrique | EV charger locations | Standard HTTP headers only |
| Open Charge Map | EV charger locations | Geographic bounding box (not your exact location) |
| OpenStreetMap (Overpass API) | Station amenities | Geographic bounding box (not your exact location) |
| Société des traversiers du Québec | Ferry schedules (GTFS) | Standard HTTP headers only |
| Ministère des Transports du Québec | Highway rest areas | Standard HTTP headers only |
| Tourisme Québec / Données Québec | Tourist attractions (SIT Québec) | Standard HTTP headers only |
| Ministère des Ressources naturelles et des Forêts du Québec | Parks (TRQ_100k) and per-park polygon geometry | Standard HTTP headers only |
| Wikipedia (REST summary) | Park descriptions | Article title only (e.g. "Parc national de la Gaspésie") plus a contact-bearing User-Agent header per Wikimedia policy |
| OpenRouteService | Driving directions and stop-order optimization for the multi-stop trip planner | Coordinates of the trip stops you have chosen (and only when you tap "Compute"); the request also carries an API key that authenticates the app, not you |
| OpenStreetMap (Nominatim) | Place labels for trip stops, and looking up a contact's address for the trip planner | The coordinates of a trip stop you drop on the map or via GPS (to fetch a readable place name); or the postal address text of a contact you explicitly pick (to convert it to map coordinates). Only sent when you take that specific action, plus a contact-bearing User-Agent header |
| Statistics Canada (WDS) | Monthly average retail gasoline prices (Montréal + Québec) for the in-app Gas Prices chart | Standard HTTP headers only (a request for the public price table) |
| OpenFreeMap | Vector map tiles for the map display | Standard HTTP headers and the map tile coordinates needed to render the area you are viewing |

No personal information, device identifiers, or precise location coordinates are sent to these services. Geographic bounding boxes used in API queries cover broad areas and cannot identify individual users. Trip-planner requests to OpenRouteService include the coordinates of the stops you assembled — these are only sent on explicit "Compute" actions, are not associated with any account or identifier, and are not stored beyond what OpenRouteService logs to operate the service. Requests to Nominatim (OpenStreetMap) are made only when you drop or GPS-locate a trip stop (the stop's coordinates are sent to fetch a readable label) or when you use the trip planner's "Choose a contact" option (the chosen contact's postal address is sent to convert it to coordinates) — they carry no account or identifier. The Wikipedia and Nominatim User-Agent identifies the app and version (e.g. "Tromi/1.0.3") plus a public Google Play Store URL — it does not include any user data.

### Contacts

The trip planner's optional "Choose a contact" feature uses Android's built-in, permission-free contact picker: the system shows your contact list, and only the single postal address you tap is handed back to the App. The App **never** requests the contacts permission and cannot read your contact list — it only receives the one address you choose, which it then forward-geocodes via Nominatim (see above) to place a trip stop. The address is not stored beyond the trip stop's resulting coordinates and label.

### Locally Stored Data

The following data is stored on your device only, using Android's Room database and DataStore:

- Favorites (gas stations, EV chargers, ferry routes, rest areas, tourist attractions, parks)
- App settings and preferences (display mode, language, search radius, default postal code / location)
- Cached station, charger, ferry, rest-area, attraction, and park data
- Cached park boundary polygons fetched on demand
- Cached Wikipedia park descriptions (article snippet + URL)
- Price history snapshots (30 days)
- Saved destinations for route planning
- Saved multi-stop trip plans (stops + computed road polyline + per-leg distance/duration)
- Price alert configurations

This data is **never** transmitted off your device.

## Information We Do Not Collect

- We do not collect personal information (name, email, phone number)
- We do not require account creation or login
- We do not use analytics, crash reporting, or telemetry services
- We do not display advertisements
- We do not use cookies or tracking technologies
- We do not sell, share, or transfer any user data to third parties

## Notifications

The App may request permission to send local notifications for price alerts you configure. These notifications are generated entirely on your device — no push notification service is involved.

## Children's Privacy

The App does not knowingly collect any personal information from anyone, including children under 13. Since the App collects no personal data, it complies with the Children's Online Privacy Protection Act (COPPA) and similar regulations.

## Data Retention

All data is stored locally on your device. Uninstalling the App removes all stored data. Price history snapshots are automatically pruned after 30 days.

## Changes to This Policy

We may update this Privacy Policy from time to time. Changes will be posted within the App or on this page with an updated revision date.

## Contact Us

If you have questions about this Privacy Policy, you can contact us at:

**Email:** patrick.roy07@gmail.com

