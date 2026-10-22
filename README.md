# Northstar — Personal Workspace

A fresh, personal-only Northstar PWA for GitHub Pages. Built with vanilla HTML, CSS and JavaScript; no framework, account, backend, paid API or build step is required.

## Features

- Personal dashboard, quick task capture, tasks with due dates and priority
- Weekly planner and focus note
- Daily habit check-ins and a small seven-day history
- Finance dashboard, manual transactions, PDF bank-statement import, category guesses, duplicate skipping, recurring-payment clues and receipt records with optional resized local images
- Meal planner, recipe library with full ingredients and step-by-step methods, adjustable recipe serving selector, shopping list, pantry list and cleaning tasks
- Projects with steps and progress, notebook, JSON export and restore
- Local browser storage and service-worker shell caching for offline use after first load
- Responsive light-mode interface designed for mobile/iPhone first

## Publish to a new GitHub repository

1. Create a new empty GitHub repository (for example `northstar-personal`).
2. Upload **the contents of this folder** to the repository root. Keep `index.html`, `styles.css`, `app.js`, `sw.js`, `manifest.webmanifest`, and `mark.svg` at the root.
3. In the repository, open **Settings → Pages**. Under Build and deployment, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
4. Wait for GitHub Pages to publish, then open the URL it provides.
5. On iPhone, open the site in Safari, tap Share, then **Add to Home Screen**.
6. Open the app once while online before relying on its cached offline shell.

## Privacy and backup

Workspace records are stored in `localStorage` in the browser on the device. They are not synced to another device. The app has no login or application backend. GitHub Pages serves the static files; it does not receive app data through app features. Imported bank statement PDFs are parsed in the browser and not uploaded by the app. Receipt images are resized in the browser and stored locally with the workspace; many large images can exceed browser storage limits. Export JSON backups regularly and store them somewhere safe.

## Finance import notes

PDF statement import is best-effort, not a certified bank feed. Inspect dates, debit/credit direction, amounts and categories after import. Transactions are not automatically reconciled with bank balances. Recurring payment suggestions are heuristics based on similar descriptions across months; verify before making decisions.

## Known limitations

- This is a new production-oriented starter, not a financial accounting system or independently security-audited product.
- Recipe serving selection currently shows a multiplier rather than recalculating every ingredient quantity. Treat amounts as a guide and adjust sensibly.
- Offline behavior depends on browser support and successful initial caching. A static GitHub Pages deployment cannot guarantee all browser storage survives device cleanup.
- This app has not been tested on every device/browser. Run the checks in `RELEASE_CHECKLIST.md` before using it as your main workspace.


## Bank statement PDF import

The Money screen accepts PDF bank statements only; the CSV import option has been removed. PDF text is extracted in the browser with PDF.js; the statement itself is not uploaded to a Northstar server. The PDF.js library and worker are loaded from cdnjs, so the first PDF import requires an internet connection. Scanned/image-only or password-protected PDFs may not work because OCR is not included. Bank statement layouts vary: check dates, descriptions, amounts, and whether each transaction is income or spending before relying on the imported totals. CSV files are not accepted by this reader.
