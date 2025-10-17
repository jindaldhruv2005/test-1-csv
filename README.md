# Hello World + CSV Viewer

## Overview
This is a minimal, professional, single-file web app that:
- Displays the text “Hello World” on the home page.
- Loads and displays the contents of sample.csv in a responsive table.

It uses plain HTML, CSS, and JavaScript with no external dependencies. The page tries to fetch sample.csv from the same folder as index.html. If you open the file directly via file:// and the browser blocks file fetching, the app will gracefully fall back to an embedded copy of the provided sample.csv so you can still see the table.

## Setup
You can run this app in two ways:

1) Recommended: serve over HTTP
- Place index.html and sample.csv in the same directory.
- Start a local server in that directory, for example:
  - Python 3: python -m http.server 8000
  - Node (npx): npx serve .
  - VS Code: use the Live Server extension
- Visit http://localhost:8000 in your browser (adjust the port as needed).

2) Open directly from the file system (quick preview)
- Double-click index.html to open it in your browser.
- Note: Many browsers block fetch() for file:// URLs, so live loading of sample.csv may fail.
- This app includes a safe fallback with the provided sample.csv contents to ensure the table still appears. To reflect changes you make to sample.csv, use a local server as described above.

## Usage
- Ensure a file named sample.csv is present alongside index.html.
- Open the app (via local server or directly).
- The CSV table will render automatically. Click “Reload CSV” to refresh from disk when served over HTTP.
- To customize, replace sample.csv with your own CSV (first row treated as headers).

## License
MIT License

Copyright (c) 2025 The Project Authors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the “Software”), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.