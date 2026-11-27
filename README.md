# Heritage Facade Database (2025)

Facade element data for 631 historic buildings in three towns in Saga Prefecture, Japan: Arita, Shiota and Kashima. Each building is described by one type code for its roof, windows, doors and shopfront.

**Associated paper:** [Paper title], City and Build Environments, under review. (Full citation will be added after publication.)

## Repository structure

| Folder | Content |
|---|---|
| `data/` | Building-level data tables (CSV) |
| `analysis/` | Summary tables of component types and their combinations (CSV) |

The facade images are hosted separately (see [Images](#images)).

## Data files (`data/`)

Each file has 631 rows (one per building) plus a header row.

| File | Columns | Description |
|---|---|---|
| `facade_attribute_database.csv` | `building_id`, `address`, `roof_type`, `window_type`, `door_type`, `shopfront_type`, `image_url` | All four element types per building. `address` is the town name only. |
| `roof_distribution.csv` | `roof_id`, `building_id`, `roof_type`, `count` | Roof type per building |
| `window_distribution.csv` | `window_id`, `building_id`, `window_type`, `count` | Window type per building |
| `door_distribution.csv` | `door_id`, `building_id`, `door_type`, `count` | Door type per building |
| `shopfront_distribution.csv` | `shopfront_id`, `building_id`, `shopfront_type`, `count` | Shopfront type per building |

## Identifiers and codes

- `building_id` links all tables. The prefix gives the town: `art` = Arita (397 buildings), `ksm` = Kashima (199), `sht` = Shiota (35).
- Type codes: roofs `R01`–`R04`, windows `W01`–`W03`, doors `D01`–`D03`, shopfronts `S01`–`S03`. The definition of each code is given in the paper ([Table 3]).
- `count` is 1 in every row (one type per building per element).

## Analysis files (`analysis/`)

Summary tables derived from the data above:

- `Building Component Distribution.csv`
- `Building Component Combinations Analysis.csv`
- `Pairwise Building Component Frequencies.csv`
- `Top 10 Types Combination.csv`
- `Top 10 Types Combinations with Building IDs.csv`

## Images

One facade image per building (631 PNG files) is hosted in the Hugging Face dataset [CliffordTheys/heritage-facade-images-2025](https://huggingface.co/datasets/CliffordTheys/heritage-facade-images-2025). The `image_url` column links to each image. File names follow the building number (for example `art_01` is `arita-facade/b_01.png`).

## License

[Data license]

## Citation

[Citation and DOI after publication.]

## Contact

Clifford Theys
clifford.theys@gmail.com
