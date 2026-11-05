# Labelled data

Target: about 1,000 labelled fault descriptions (300 to 500 by late December for the PiP proof of concept).

## Format

One CSV file, `descriptions.csv`, one row per description:

| Column | Meaning | Example |
| --- | --- | --- |
| `id` | Unique number | `1` |
| `text` | The fault description, as a student would write it | `the oven in our kitchen won't turn on` |
| `category` | One of the categories below | `kitchen_appliances` |
| `priority` | `emergency`, `urgent`, `routine` or `none` | `urgent` |
| `area` | `halls`, `campus` or `both` | `halls` |
| `source` | Where it came from: `uwe_example`, `survey`, `generated` or `own` | `own` |

## Categories

`plumbing_water`, `heating_hot_water`, `electrical_lighting`, `kitchen_appliances`, `doors_windows_locks`, `furniture_fittings`, `it_av`, `cleaning_pests`, `safety`, `no_repair_needed`

## Priorities

Based on UWE's repairs service standards:

- `emergency`: attend within 4 hours (serious flooding, total power loss, safety hazards)
- `urgent`: attend within 8 hours (no heating or hot water, faulty locks, broken cooking or fridge appliances)
- `routine`: within 7 days (minor repairs, furniture, slow drains)
- `none`: no repair needed

## Rules

- No personal information in any description
- Generated descriptions are checked and labelled by hand
- Descriptions about the same fault stay in the same train, validation or test split
