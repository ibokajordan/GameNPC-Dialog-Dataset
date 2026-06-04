# Raw Dataset

This folder contains the original/raw version of the GameNPC-Dialog Dataset.

## Files

| File | Description |
|---|---|
| `game_NPC_dataset_raw.jsonl` | Original raw dataset in JSON Lines format. Recommended for large-scale processing and model training. |
| `game_NPC_dataset_raw.json` | Raw dataset as a JSON array. Useful for inspection and JSON-based workflows. |
| `game_NPC_dataset_raw.csv` | Flattened tabular version of the raw dataset. Useful for spreadsheet-based review and statistical analysis. |

## Basic Information

| Item | Value |
|---|---|
| Total records | 91,720 |
| JSONL validation errors | 0 |
| Source file | `game_NPC_dataset.jsonl` |
| Encoding | UTF-8 |

## Domain Distribution

| Domain | Record Count |
|---|---|
| dialogues | 20,977 |
| travel | 20,074 |
| metaverse_information | 15,237 |
| history_npc | 12,967 |
| metaverse_ınformation | 3,500 |
| school_rules | 2,207 |
| disease | 1,234 |
| crisis | 1,200 |
| artificial_intelligence | 1,108 |
| family | 1,100 |
| counseling | 750 |
| health_safety | 746 |
| academic | 650 |
| emergency | 650 |
| search_rescue | 650 |
| virtual_museum | 608 |
| robotics | 580 |
| engineering | 558 |
| assessment | 537 |
| rules | 522 |
| design_production | 516 |
| history | 516 |
| laboratory | 516 |
| data_analysis | 516 |
| physics | 515 |
| chemistry | 496 |
| environment | 495 |
| geography | 458 |
| coding | 458 |
| biology | 457 |
| stem | 450 |
| mathematics | 328 |
| energy | 144 |

## Notes

- The raw files are intended to preserve the dataset in its original structure.
- For public GitHub repositories, large files may require Git LFS if they exceed GitHub's standard file size recommendations.
- Processed, cleaned, or task-specific versions should be stored separately under `data/processed/`.
