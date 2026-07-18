# Tutorial 18 — Weir pulsing

Four small models of a dam supplying a downstream re-regulating weir, showing how
order rules interact with routing delay: why naive rules oscillate ("weir pulsing"),
how to stabilise them, and how storage routing breaks the simple fix.

## Layout

```
018/
├── data/
│   ├── inflows.csv             (dam inflows, 1990-1999)
│   └── orders.csv              (downstream orders at the weir, 1990-1999)
└── models/
    ├── weir1_lag_naive.ini     (lag routing, naive rule → pulsing)
    ├── weir2_lag_stable.ini    (lag routing, order-up-to rule → stable)
    ├── weir3_pwl.ini           (pwl storage routing, same rule → pulsing returns)
    └── weir4_pwl_stable.ini    (pwl storage routing, reach-aware rule → stable)
```

## Running

```bash
cd 018/models
kalix simulate weir1_lag_naive.ini -o results1.csv
```

Repeat for the other three models. Compare `node.005_weir.volume` and
`var.results.shortfall` between runs.

## Expected results (total shortfall, 1990-1999)

| model | shortfall | days |
| --- | --- | --- |
| weir1_lag_naive | 23,115 ML | 711 |
| weir2_lag_stable | 1,876 ML | 66 |
| weir3_pwl | 6,037 ML | 192 |
| weir4_pwl_stable | 1,373 ML | 36 |
