# Tutorial 5 — Running Kalix from Python

A Jupyter notebook that drives a Kalix simulation from Python, reads the outputs as pandas DataFrames, and plots them. Uses the [`kalix`](https://pypi.org/project/kalix/) package.

## Layout

```
005/
├── data/                       (5 CSVs, carried from earlier tutorials)
└── models/
    └── baseline/
        ├── stringybark.ini     (the model, uses trailhead paths)
        └── analysis.ipynb      ← the notebook
```

## Running the notebook

```bash
pip install kalix
cd 005/models/baseline
jupyter lab analysis.ipynb
```

Then run all cells.

## What the notebook does

1. Imports `kalix` and prints the version
2. Runs `stringybark.ini` with `kalix.simulate(output_file="results.csv")`
3. Reads `results.csv` and plots simulated vs observed flow for 1989–1990
4. Bonus: runs the same model with `output_file="results.pxb"` (Pixie — Kalix's native Gorilla-compressed format) and reads it back with `kalix.read_pixie()`
