# Workout Log

A personal workout-planning and tracking website published through GitHub Pages.

## Live Website

- [Open the Workout Log](https://shepchristian.github.io/workout-log/)

## Repository Files

### `index.html`

The website interface. It loads prescribed workout plans from `workouts.json` and displays them on the GitHub Pages site.

### `methodology.md`

The authoritative training methodology. It defines:

- training phases and dates
- nutrition approach
- running benchmarks
- cycling benchmarks
- lifting and conditioning structure
- core-training rationale
- progression by phase
- weekly training template

Direct file links:

- [View rendered methodology](https://github.com/shepchristian/workout-log/blob/main/methodology.md)
- [View raw methodology](https://raw.githubusercontent.com/shepchristian/workout-log/main/methodology.md)

### `workouts.json`

The complete prescribed-workout history used by the website.

Direct file links:

- [View workout JSON on GitHub](https://github.com/shepchristian/workout-log/blob/main/workouts.json)
- [View raw workout JSON](https://raw.githubusercontent.com/shepchristian/workout-log/main/workouts.json)

### `README.md`

This repository guide for people and AI assistants.

## Data Ownership

- `methodology.md` contains the training rules.
- `workouts.json` contains prescribed workouts.
- `index.html` contains the website interface.
- Supabase will contain actual user activity, including workout completion, sets, reps, weights, and user-specific history.

Do not store private user activity or authentication credentials in this public repository.

## AI Workout-Planning Instructions

When using Claude, Copilot, or another AI assistant to plan a new training week:

1. Read `methodology.md` first.
2. Read the complete current `workouts.json`.
3. Confirm both files were retrieved successfully before planning.
4. Determine the current training phase from `methodology.md` and the dates being planned.
5. Review recent prescribed workouts for continuity, balance, and progression.
6. Use actual performance data only when it is provided from the approved results source.
7. Append newly prescribed workouts to `workouts.json`.
8. Preserve the existing JSON schema and data types.
9. Preserve all historical workouts and existing workout IDs.
10. Never overwrite an existing workout unless the request explicitly identifies that workout for revision.
11. Never invent workout completion, actual reps, actual weights, RPE, or user history.
12. Do not modify `index.html` or `methodology.md` unless explicitly requested.

## Workout History Rules

- Historical prescribed workouts must remain in `workouts.json`.
- The website may display a rolling three-month window, but the underlying JSON should retain older workouts.
- Planned workouts and completed results are separate records.
- User completion and performance belong in Supabase, not `workouts.json`.
- Suggested weights must be clearly distinguished from actual historical weights.

## Weekly Planning Workflow

1. Retrieve the raw methodology and workout JSON from the links above.
2. Validate the current JSON before editing it.
3. Review the relevant phase, recent workouts, and approved performance results.
4. Plan the next seven days.
5. Append the new workout objects without altering existing records.
6. Validate that the finished file is valid JSON.
7. Upload the revised `workouts.json` to the repository's `main` branch.
8. The existing GitHub Pages link will then display the updated plan.

## Required AI Verification

Before generating a revised `workouts.json`, the AI assistant should report:

- whether `methodology.md` was retrieved
- whether `workouts.json` was retrieved
- the current methodology phase
- the number of workout records found
- the latest dated workout found

If either source file cannot be retrieved, the AI assistant should stop instead of reconstructing or inventing missing content.
