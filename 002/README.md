# Tutorial 2 — Expressions

Builds on Tutorial 1 by replacing the single rainfall input with a weighted combination of three rainfall stations, demonstrating Kalix's expression syntax.

The walk-through lives on the Kalix User Guide:
[Tutorial 2 on Notion](https://chasegan.notion.site/Tutorial-2-Expressions-3713cd7417a281ef90f6d65d71b8de4c)

## Files

- `stringybark_expressions.ini` — the model
- `rain_north.csv`, `rain_central.csv`, `rain_south.csv` — daily rainfall at three stations around the catchment (mm/day)
- `climate_data.csv` — daily potential evaporation (`pet_mm` column; `rain_mm` is unused in this tutorial)
- `observed.csv` — observed streamflow at the gauge (ML/day)
