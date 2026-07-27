# AlertAble — UI/UX Screens & Technology Map

Interactive mockups for **AlertAble: A Mobility-Adaptive Disaster Response Application for Mobility-Impaired Individuals During Floods and Earthquakes** (CAP-2530-IT, De La Salle University – Manila, College of Computer Studies).

**88 screens across 4 user roles**, each annotated with the specific APIs, sensors, protocols and services that would implement it.

## View it live

Published with GitHub Pages at:

```
https://<your-username>.github.io/<your-repo-name>/
```

The file is named `index.html`, so it loads automatically at the root URL — no filename needed.

### Enabling GitHub Pages

1. Repo → **Settings → Pages**
2. **Source** → *Deploy from a branch*
3. **Branch** → `main`, folder → `/ (root)`
4. **Save**, wait 1–2 minutes for the first build
5. Refresh — a green banner shows the live URL

## Contents

| Tab | Screens | Covers |
|---|---|---|
| **Comms Decision** | — | Transport-ladder recommendation: why a "dedicated line" isn't app-provisionable, and the four-tier fallback (IP → SMS/2G → offline mesh → cell broadcast) |
| **General User** | 20 | Signup, household composition, hazard map, alerts, evacuation, hazard reporting, volunteer assist, check-in, connectivity ladder |
| **Mobility-Impaired** | 24 | Mobility device & assistance profiling, medical/meds/equipment, caregiver linkage, alert dashboard, DND override, wearable pairing, PWD profile page + offline QR handoff, accessible routing, SOS |
| **Caregiver** | 20 | Mandatory linkage gate, permission scope, live tracking, geofences, device health, act-on-behalf, stalled-transit detection, escalation, secondary caregivers |
| **First Responder** | 24 | LGU verification, prioritised resident registry, handling profiles, SOS triage & dispatch, hazard-report verification, mark-area-unwalkable, PWD density heatmap, planning analytics, after-action report |

## Colour system

Sampled directly from the AlertAble logo:

- **Red `#C01120`** — emergency, hazard, SOS, urgent action
- **Navy `#05354F`** — primary navigation and standard actions
- **Mid blue `#439EBD`** — informational, accessible/safe state
- **Macadamia `#F7E3BC`** — supporting surfaces and preparedness

## Technical notes

Self-contained single HTML file — no build step, no dependencies to install. The AlertAble logo is embedded as a base64 data URI (extracted from the group's moodboard), and typography loads from Google Fonts via CDN.

## Troubleshooting a 404

- Confirm Pages finished building (green checkmark in Settings → Pages)
- URLs are case-sensitive
- Confirm the file sits in the folder Pages is set to serve from (root vs `/docs`)
- The repo must be public unless you're on a plan supporting private Pages

## Maps

The maps are real — [Leaflet](https://leafletjs.com) rendering live OpenStreetMap tiles, anchored at **2815 Pilapil St, Pasay City** (`14.540809, 121.000003`, Plus Code `7Q63G2R2+82F`). The surrounding street grid, building footprints and labels are genuine OSM data.

Routes, hazard polygons and the H3-style density hexagons are illustrative overlays drawn at plausible offsets from that anchor, not live routing output — a production build would replace them with OpenRouteService wheelchair-profile responses and verified hazard geometry from the backend.

Tiles load from `tile.openstreetmap.org` in the viewer's browser, so an internet connection is needed to see them. OSM attribution is retained on every map as their tile usage policy requires.

## Logo

`alertable-logo.png` is the tiered pyramid extracted from the group's moodboard, background removed, centred on a transparent square canvas. It is embedded directly in `index.html` as a base64 data URI, so the HTML file stays self-contained.
