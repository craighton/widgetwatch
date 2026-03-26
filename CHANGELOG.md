# Changelog

All notable changes to Widget Watch are documented here.

Format based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), versioned per [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.3.0] - 2026-03-26

### Added
- Hub health navigation links in hub health panel

### Changed
- Flight popup restructured: phase badge now appears inline right of the callsign; Watch and Share buttons moved to a dedicated row below the external links
- Busiest hub badge unbolded

### Fixed
- Hub labels on the map no longer render in incorrect positions on first load (deferred `drawHubs()` to `map.whenReady()` so permanent tooltips are positioned after Leaflet completes its initial layout)
- Terminal and gate values from FlightAware API now escaped before injection into popup HTML (XSS fix)

### Removed
- Unused `planePos` variable in route drawing
- Unused `bmacInteractions` counter
- Dead `splitAtAntimeridian` legacy wrapper function

---

## [1.2.0] - 2026-03-25

### Added
- FlightRadar24 link in flight popup (`flightradar24.com/DAL{flight}`)
- IROPS hub-awareness — IROPS alerts now scoped per hub

### Changed
- Watch and Share buttons moved to sit inline right of the popup callsign
- Popup links row centered horizontally and locked to a single line (no wrap, no clip)
- UI theme refresh with updated CSS color variables
- Busiest hub badge now uses a red gradient
- Cruise phase color updated to `#0077cc`
- Refresh button default and hover colors swapped
- Live-fleet and schedule active styles simplified
- Analytics bar colors updated
- Heatmap route label removed; heatmap color updated
- Control buttons forced visible; status color tweaked
- Branding consolidated to "Widget Watch" across the project
- Prewarm script updated to use Widget Watch name

### Fixed
- Popup departure/arrival times preserved when popup HTML is refreshed
- FR24 summary epoch timestamps converted to ISO format before display
- Marker popup correctly refreshed after async flight HTML update
- IRROPS renamed to IROPS throughout the codebase

### Removed
- Alerts ticker feature and all related code
