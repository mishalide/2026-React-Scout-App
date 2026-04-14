# Pearametrics | Pearadox's 2026 Scouting App

[![Version](https://img.shields.io/badge/version-2026.Aldine.2-blue)](https://github.com/mishalide/2026-React-Scout-App)
[![React](https://img.shields.io/badge/React-18.3.1-61DAFB?logo=react&logoColor=white)](https://react.dev)
[![pages-build-deployment](https://github.com/mishalide/2026-React-Scout-App/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/mishalide/2026-React-Scout-App/actions/workflows/pages/pages-build-deployment)

**[Check out the app!](https://mishalide.github.io/2026-React-Scout-App/)**

A React-based FRC scouting app built by Pearadox 5414. Runs entirely offline from a single HTML file: no internet or server required, even for first load!

---

## Setup

### Android (Recommended)
1. Transfer `index.html` to the tablet in Chrome
2. *(Optional)* Tap the menu -> **"Add to Home screen"** to create a shortcut.

### Windows/Linux
1. Open the `index.html` file

### iOS
1. iOS is more finnicky; you can either deploy the app to a web page and load it via the web, or you can download it and use an HTML viewer. We cannot verify whether it works for iOS.

> The app is self-contained; React and all dependencies are bundled inside the HTML file, so it works with no internet connection after the first load.

---

## Customization

**Before using at a competition, update these two lists inside `index.html`:**

- **`scouterNamesData`**: the list of scouter names shown in the dropdown
- **`teamNumbersData`**: the team numbers for the competition

Both are plain arrays near the top of the `<script>` section. Just Ctrl+F for `scouterNamesData` or `teamNumbersData` to find them.

Other things you might want to tweak:

| What | Where to look |
|------|--------------|
| Start position labels | `startPosition` RadioGroup options |
| App title (shown on home screen shortcut) | `<title>` tag at the top of the file |

---

## Navigation Bar

The bar at the top has three buttons:

| Button | Function |
|--------|----------|
| ⛶ | Toggle fullscreen |
| ↻ | Regenerate a previous QR code from history |
| ⚙ | Open Settings |

On smaller screens, the bar can be collapsed/expanded with the ☰ / ✕ toggle.

---

## Settings (⚙)

### Scouting Mode
Switch between Match Scouting and Pit Scouting.

### Fuel Counter Type
Choose how fuel/scoring is tracked during a match. Four options are available:

- **Number Stepper** *(recommended)*: Tap +/− buttons to increment scored and missed fuel counts directly.
- **Cycle Counter**: Log each cycle individually using a slider, then add it to the running total.
- **Relative Amount**: Categorize each cycle as Very Little / Small / Average / Lots / A TON, then add to total.
- **FPS Tracker**: Start/stop a timer while the robot is shooting and record fuel-per-second rate.

---

## Match Scouting

### Pre-Match

| Field | Type | Notes |
|-------|------|-------|
| Scouter Name | Dropdown | Required (*) |
| Team Number | Dropdown | Required (*) |
| Match Number | Number | Required (*); auto-increments on reset |
| No Show | Checkbox | + hides game data fields if checked |
| Start Position | Radio | Depot Trench / Depot Bump / Middle / Outpost Bump / Outpost Trench |

A view Field Map button is available to reference robot starting positions.

### Autonomous
- Hub fuel scored and missed (via selected fuel counter type)
- Fuel collection sources: Depot, Outpost, Neutral Zone
- Climb time: \<3s / \<5s / \<15s / 15+s / Failed / Not Tried
- Climb side (Center or Side) — hidden if climb was Not Tried

### Tele-Op
- Hub fuel scored and missed (via selected fuel counter type)
- Same collection source tracking as auto

### End Game
- Climb result and timing
- Other end-game specific fields

---

## Pit Scouting

Collected during pit visits. Fields include:

- Drive train type (tank, swerve, motor types)
- Intake type (through bumper / over bumper)
- Intake sources (Ground, Outpost, Depot)
- Hopper capacity and dimensions
- Traversal ability (over bump / under trench)
- Climbing ability (L1 / L2 / L3 / Not Able) and climb side
- Autonomous capabilities and preferred paths
- Auto-align capability
- Driver experience (years + hours)
- Drive team rotation strategy
- Robot primary purpose and estimated weight
- Programming language
- Help needed (and type of help)
- Comments / additional notes
- A very helpful reminder to photograph the robot (with team permission!)

---

## QR Code Export

Once a form is complete, tap generate QR Code. The QR encodes all scouted data and can be scanned by a data collection device.

- QR codes are added to a history log for the session.
- Tap ↻ in the nav bar to pull up and re-display any previous QR code.
- After generating, tap Reset Data to start the next entry — the app will preserve your scouter name and auto-increment the match number.

---

## Used By

See [TEAMS.md](TEAMS.md) if you've used Pearametrics at a competition, open a PR and add your team ^_^
