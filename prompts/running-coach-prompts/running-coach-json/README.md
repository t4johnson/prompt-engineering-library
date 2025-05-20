# Runner Profile JSONs

This folder contains structured intake data for testing and developing the AI Running Coach system.

Each file represents a fully formed runner profile, formatted to match the required input schema used in the prompt modules (e.g., `training-plan-generator.md`, `plan-adjustment.md`).

## Usage

These JSON files can be:
- Manually pasted into prompt templates for testing output
- Parsed into an intake form (future UI/API work)
- Used for version-controlled snapshot testing

## Profiles

| File                              | Description                                  |
|-----------------------------------|----------------------------------------------|
| `runner_profile_0_true_beginner` | Wants to run 1 continuous mile               |
| `runner_profile_1_5k_first_timer`| First 5K attempt, nervous and new            |
| `runner_profile_2_10k_pr_chaser` | Intermediate runner chasing a 10K PR         |
| `runner_profile_3_injury_rebuild`| Returning athlete, previously advanced       |
| `runner_profile_4_marathon_bq`   | High-volume, Boston-qualifying marathoner    |

## Template

See `runner-intake-template.json` for the current full field structure.
