# heritage-facade-database-2025

Facade element data for historic buildings in three towns: Arita, Shiota and Kashima (Saga Prefecture, Japan). The data is a CSV export of the PostgreSQL database `heritage-facade-database-v1` (Neon), exported on 2026-11-20.

## Repository structure

- `data/`: CSV export of the database (below)
- `images/`: facade images (to be added)
- `analysis/`: analysis CSV files for the paper (to be added)

## Files

All files in this section are in `data/`. Each has 631 rows (one per building) plus a header.

| File | Columns | Description |
|---|---|---|
| `building_summary.csv` | `building_id`, `address`, `image_url` | One row per building. `address` is the town name only. |
| `door_distribution.csv` | `door_id`, `building_id`, `door_type`, `count` | Door type per building |
| `roof_distribution.csv` | `roof_id`, `building_id`, `roof_type`, `count` | Roof type per building |
| `shopfront_distribution.csv` | `shopfront_id`, `building_id`, `shopfront_type`, `count` | Shopfront type per building |
| `window_distribution.csv` | `window_id`, `building_id`, `window_type`, `count` | Window type per building |

## Keys and codes

- `building_id` links all tables. The prefix gives the town: `art` = Arita (397 buildings), `sht` = Shiota (35), `ksm` = Kashima (199).
- Type codes: doors `D01`–`D03`, roofs `R01`–`R04`, shopfronts `S01`–`S03`, windows `W01`–`W03`. The meaning of each code is defined in the project's element annotation guideline, which is not included in this repository.
- In this export, `count` is 1 in every row (one type per building per element).

## Notes

- `image_url` points to facade images stored in Neon object storage. These links may not be publicly accessible. Check them before relying on them in the paper.
- The `neon_auth` tables of the source database (users, sessions) are not exported.

## Citation

Add the paper citation and a data license here once decided.
