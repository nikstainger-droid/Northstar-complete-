# Northstar feature audit

## Recipe coverage
- 100 non-baking meal options.
- 22 separate baking recipes.
- Recipes include ingredient quantities, serving sizes, preparation and cooking times, steps, and dietary cautions.
- Search across recipe title, category, and ingredient names.
- Library views: all recipes, meal options, and baking.

## Shopping-list behaviour
- Water / plain cooking water is excluded from shopping suggestions.
- Meal-plan quantities are scaled from each recipe's actual default serving count.
- Matching ingredient names with matching units are combined across planned meals.
- A review/confirmation step is shown before meal-plan ingredients are added.
- Manual shopping items and checked-off items are preserved.
- The recipe-specific Add Ingredients action also skips plain water.

## Retained personal features
Tasks, weekly planner, habits, transactions, bills, savings goals, projects and milestones, cleaning, meal planning, shopping, pantry, events, notes, settings, JSON backup/restore, and PWA/offline support remain in the project.

## Not included
Bank statement import, Supabase, family accounts, invitations, or cloud sharing.

## Validation
Static validation should include JavaScript parsing, recipe count checks, and ZIP integrity. Real browser interaction, recipe review, and iPhone deployment still need human acceptance testing.
