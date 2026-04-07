# Privacy Policy

**Last updated:** April 7, 2026

Patrick Roy ("we", "us", or "our") operates the Tromi mobile application ("the App"). This Privacy Policy explains what information the App accesses, how it is used, and your choices.

## Information We Collect

### Location Data

The App requests access to your device's precise location (GPS) to:

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

No personal information, device identifiers, or precise location coordinates are sent to these services. Geographic bounding boxes used in API queries cover broad areas and cannot identify individual users.

### Locally Stored Data

The following data is stored on your device only, using Android's Room database and DataStore:

- Favorite stations
- App settings and preferences (display mode, language, search radius, postal code)
- Cached station data and price history (30 days)
- Saved destinations for route planning
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
