# Tutorial 3 — Relative paths and trailhead paths

Restructures Tutorial 2's Stringybark model into a typical multi-folder project layout, demonstrating why Kalix's trailhead path syntax (`^/...`) is the right default once you start organising models into subfolders.

The walk-through lives on the Kalix User Guide:
[Tutorial 3 on Notion](https://chasegan.notion.site/Tutorial-3-Relative-paths-and-trailhead-paths-3713cd7417a2819abaf9fd445d3e6722)

## Layout

```
003/
├── data/                  ← shared inputs (carried over from Tutorial 2)
│   ├── climate_data.csv
│   ├── observed.csv
│   ├── rain_north.csv
│   ├── rain_central.csv
│   └── rain_south.csv
└── models/
    └── baseline/
        └── stringybark.ini  ← ships with relative paths; the tutorial converts them to trailhead
```

During the tutorial you'll create a second model variant under `models/scenarios/wetter/` and watch the relative paths break before fixing them with trailhead paths.
