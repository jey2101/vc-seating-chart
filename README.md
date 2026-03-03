# VC Seating Chart

A classroom seating chart app for teachers. Arrange students in a configurable grid, drag and drop them between seats, import rosters from CSV, and export print-ready PDFs with built-in attendance/participation tracker grids.

## Live Demo

[https://jey2101.github.io/vc-seating-chart/](https://jey2101.github.io/vc-seating-chart/)

## Features

- **Multiple classes** — create and switch between as many class sections as you need
- **Configurable grid** — set rows, columns, and aisle spacing per class
- **Drag-and-drop seating** — move students between seats or to/from an unassigned roster
- **Disable seats** — mark individual seats as unavailable (e.g. broken chair, blocked view)
- **CSV import** — paste or upload a student roster; names are parsed automatically
- **PDF export** — prints in landscape, black-and-white, with auto-sized names and a 5×2 tracker grid under each seat for attendance or participation marks
- **Persistent state** — all data saved automatically in `localStorage`; your charts survive page refreshes

## Usage

### Setting up a class
1. Click **Manage Classes** to create a class and set its grid dimensions (rows, columns, aisle placement).
2. Click **Import Students** and paste a CSV or newline-separated list of student names.

### Arranging seats
- Drag a student from the **Unassigned** list on the right into any empty seat.
- Drag a seated student to a different seat, or back to the Unassigned list.
- Right-click a seat to disable or re-enable it.

### Printing
Click **Print / Export PDF** to open the browser print dialog. The layout switches to a compact, black-and-white grid with a 5-row × 2-column tracker box under each name — suitable for daily use.

## Tech Stack

- Plain HTML, CSS, and JavaScript — no frameworks, no build step
- [PapaParse 5.5.3](https://www.papaparse.com/) (loaded from CDN) for CSV parsing
- Native HTML5 Drag-and-Drop API
- `window.print()` for PDF export
- `localStorage` for persistence

## Running Locally

No install or build step required. Just open the file in a browser:

```
open index.html
```

Or serve it with any static file server if you prefer:

```
npx serve .
```

## Data & Privacy

All data (class names, rosters, seat assignments) is stored exclusively in your browser's `localStorage`. Nothing is sent to a server. Clearing your browser data will erase your charts, so use the CSV import/export workflow to back up rosters you want to keep.
