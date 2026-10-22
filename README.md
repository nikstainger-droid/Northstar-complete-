# Northstar Personal — Complete Build

A single-user, local-first personal workspace for GitHub Pages. It has no Supabase dependency, family accounts, invitations, cloud-sharing, or bank-statement importer.

## Food and home
- 100 complete meal recipes with ingredients, serving sizes, preparation/cooking times, methods, and dietary cautions.
- Separate baking section with 22 complete recipes for biscuits, muffins, cakes, scones, slices, pancakes, and savoury baking.
- Search and filter by all recipes, meals, or baking.
- Link dinner recipes to the meal plan and review the proposed shopping list before adding.
- Shopping-list generation excludes plain water and combines matching ingredient names and units across planned recipes.
- Manual shopping items and checked-off items are preserved when rebuilding meal-plan items.
- Pantry, cleaning tasks, events, and noticeboard.

## Personal workspace
- Tasks, priorities, due dates, recurring tasks, subtasks, and project links.
- Habits and daily tracking.
- Money transactions, bills, goals, savings contributions, and spending summaries.
- Projects with milestones, cleaning routines, searchable notes, JSON backup/restore, local storage, and PWA/offline support.

## Publish
1. Extract the ZIP.
2. Upload the contents of this folder to the root of a new GitHub repository. Keep `index.html`, `manifest.webmanifest`, `worker.js`, and `mark.svg` together.
3. In GitHub, open Settings → Pages, choose Deploy from a branch, select `main` and `/(root)`, and save.
4. Test the deployed app on your phone before relying on it.

## Data and limitations
Data is stored in the browser on the current device. Export a JSON backup regularly; clearing browser storage can delete app data. Offline support depends on the service-worker cache having been installed while online. This release should be interactively tested on target browsers before being treated as production-ready.


## Recipe library verification
- The library contains 100 non-baking meal recipes plus 22 baking recipes (122 total).
- The recipe browser filters by meal, baking, or all recipes and displays the actual count.
- Shopping-list suggestions exclude plain water and other non-purchase cooking liquids.


### Recipe library display
The recipe library shows the first 10 matching recipes initially, with **Show 10 more** and **Show all** controls. The status line reports how many recipes are shown versus how many match the current filter/search. Searching or changing All / Meals / Baking resets the list to the first batch. The service-worker cache name was bumped so the updated app shell can replace an older cached copy.
