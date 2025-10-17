# Hello World + CSV Viewer (Add Rows + Download)

## Overview
A minimal, professional, single-file web app that:
- Displays “Hello World” on the home page.
- Loads and displays the contents of sample.csv in a responsive table.
- Lets you add new rows via a simple form generated from the CSV headers.
- Lets you download the edited CSV as a file.

It uses plain HTML, CSS, and JavaScript with no external dependencies. The page tries to fetch sample.csv from the same folder as index.html. If the browser blocks fetch() for file:// URLs, the app gracefully falls back to an embedded copy so you can still see and edit the table.

## Setup
You can run this app in two ways:

1) Recommended: serve over HTTP
- Place index.html and sample.csv in the same directory.
- Start a local server in that directory, for example:
  - Python 3: python -m http.server 8000
  - Node (npx): npx serve .
  - VS Code: Live Server extension
- Visit http://localhost:8000 in your browser (adjust port as needed).

2) Open directly from the file system (quick preview)
- Double-click index.html to open it in your browser.
- Note: Many browsers block fetch() for file:// URLs, so live loading of sample.csv may fail.
- This app includes a safe fallback with embedded sample CSV. To reflect changes you make to sample.csv on disk, use a local server as described above.

## Usage
- Ensure a file named sample.csv is present alongside index.html (optional; if missing, the embedded sample is used).
- Open the app (via local server or directly).
- The CSV table renders automatically.
- Add rows:
  - Click “＋ Add Row” to reveal the form.
  - Enter values for each column and click “Append Row.” Repeat as needed.
- Download the edited CSV:
  - Click “⭳ Download CSV” to save the current table as a CSV file.
  - If edits were made, the file is named sample_edited.csv; otherwise sample.csv.
- Reload from disk (HTTP only):
  - Click “⟲ Reload CSV” to re-fetch sample.csv from the server. If you’ve made in-memory edits, you’ll be asked to confirm before discarding them.

Notes:
- Edits are kept in memory only; the app cannot overwrite files on your disk. Use the Download button to save your edited CSV.
- The first row of a CSV is treated as the header row.

## Improvements from previous version (Round 2)
- Added “＋ Add Row” with an auto-generated form based on the CSV headers to append new rows to the table.
- Added “⭳ Download CSV” to export the current (possibly edited) table as a CSV file with proper quoting/escaping.
- Added a “dirty” status indicator and a confirmation prompt when reloading to prevent accidental loss of edits.
- Retained graceful fallback to embedded CSV when file:// fetch is blocked.

## License
MIT License

Copyright (c) 2025 The Project Authors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the “Software”), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.