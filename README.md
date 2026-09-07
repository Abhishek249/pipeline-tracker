# Pipeline Tracker

A single-file, no-backend tracker for any application/interview pipeline. One row per company, one column per round — see every stage's status at a glance, plus a calendar and an upcoming-events list.

**Live demo:** https://abhishek249.github.io/pipeline-tracker/

![Pipeline Tracker screenshot placeholder](#)

## Why

Spreadsheets don't show progression well, and most trackers require signing up somewhere. This is one HTML file: open it (locally or via the link above) and start tracking. There's no server, no account, and no analytics - every card you add is written straight to your browser's `localStorage` and never leaves your machine.

## Features

- **Per-company rows, per-round cards** - each card carries its own round name, status, date/time, and notes.
- **Color-coded status** - waiting to hear back (yellow), scheduled (blue), completed (green), offer (purple), rejected (red).
- **Calendar + upcoming list** - any round with a date shows up automatically.
- **Export / Import JSON** - back up your data, move it to another browser or device, or share a snapshot with someone else.
- **Clear all** - wipe the board and start fresh (asks for confirmation first).

## Using it

1. Open `index.html` in any browser (double-click the file, or use the [live demo](https://abhishek249.github.io/pipeline-tracker/)).
2. It loads with two example companies so you can see how it looks. Click **Clear all** to remove them, or just start editing/deleting the example cards.
3. **Add Company** (top-left of the grid) to add a row. Click any `+` cell to add a round to that company.
4. Click any card to edit its status, date, time, or notes. Click a company name to edit or delete the whole row.
5. Use **Export JSON** any time you want a backup file, and **Import JSON** to load one back in (this replaces whatever is currently in the browser).

## Data & privacy

Everything lives in `localStorage`, scoped to whatever browser/profile/device you're using. That means:

- Data does **not** sync between browsers, devices, or incognito windows.
- Clearing your browser's site data for this page deletes your board - export a backup periodically if it matters to you.
- No data is ever sent to a server. This is a static HTML file; you can verify that by reading `index.html` - there are no network calls in it at all.

## Running it locally / self-hosting

There's nothing to build. Clone the repo and open `index.html`, or serve the folder with any static file host (GitHub Pages, Netlify, a plain `python -m http.server`, etc.).

```bash
git clone https://github.com/Abhishek249/pipeline-tracker.git
cd pipeline-tracker
open index.html   # or just double-click it
```

## License

MIT - see [LICENSE](LICENSE).
