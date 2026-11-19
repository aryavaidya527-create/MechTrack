# MechTrack — Phase 1 (v1.0.0)

MechTrack is an independent, browser-based mechanical operations logbook prototype. Phase 1 focuses on three practical workflows: production records, maintenance records, and basic motor calculations.

## Phase 1 features

1. **Production log** — record batch date, product, input mass, output mass, and run time. The app calculates material yield and output rate.
2. **Maintenance log** — record inspections, cleaning, lubrication, repairs, replacements, status, and optional cost.
3. **Motor calculator** — estimate shaft torque from power and speed, or power from torque and speed.
4. **Machine profile** — store a label and user-entered machine details for the workspace.
5. **CSV export** — export production and maintenance records for further analysis.

## Technology

- HTML for the page structure
- CSS for the responsive interface
- Vanilla JavaScript for calculations, records, and navigation
- Browser `localStorage` for local persistence
- Web App Manifest and service worker for optional PWA installation/offline caching when served over HTTPS or localhost

## Run locally

Open `index.html` in a modern browser. The core app works locally. To test service-worker/PWA behavior, serve the folder from `localhost` or deploy it over HTTPS; service workers do not run from a `file://` URL.

## Calculation notes

- Material yield (%) = output mass ÷ input mass × 100
- Output rate (kg/h) = output mass ÷ run time
- Shaft torque (N·m) ≈ 9550 × power (kW) ÷ speed (RPM)
- Shaft power (kW) ≈ torque (N·m) × speed (RPM) ÷ 9550

The motor calculations are ideal shaft estimates. They do not account for motor efficiency, power factor, service factor, gearbox losses, belt losses, or actual load conditions. Verify inputs against reliable nameplate/manufacturer data and qualified engineering review before using results for equipment selection.

## Data and limitations

- Records are stored in the current browser profile on this device. There is no login, cloud database, multi-user access, or automatic sync.
- Export CSV files to keep separate backups. Clearing browser/site data or changing browsers/devices can remove access to locally stored records.
- This is a production and maintenance logbook, not an industrial control, safety, or condition-monitoring system. It does not read sensors or control machinery.
- For public demonstrations, use generic or personally owned machine details. Share internship or employer-owned specifications only when you have permission.

## Roadmap

- **Phase 1:** core production logging, maintenance logging, and motor calculations.
- **Phase 2:** planned production analysis and expanded machine-performance records.
- **Phase 3:** planned broader machine-management workflow and optional hardware-data integration, subject to validation and feasibility.

Roadmap items are planned, not current features.
