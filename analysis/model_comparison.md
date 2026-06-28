# Model Comparison
**Name:** Radha Manasa Peesapati | **Date:** June 2026

---

## Models Built

### Model 1 — Marketing Spend (Simple)
- R-squared: 0.1672
- Coefficient: 2.13
- P-value: <0.001
- Only explains 16.7% of sales variation. Not enough on its own.

### Model 2 — Footfall (Simple)
- R-squared: 0.7363
- Coefficient: 35.68
- P-value: <0.001
- Best simple model. Each additional visitor is associated with ~$35.68 more in sales.

### Model 3 — Inventory Availability (Simple)
- R-squared: 0.0131
- Coefficient: 2,217.83
- P-value: 0.041
- Very weak on its own but becomes more useful in the multiple regression.

### Model 4 — Multiple Regression (Final)
- R-squared: 0.8312
- Variables: footfall, marketing_spend, inventory_availability_pct, customer_rating, region dummies, store_type dummies
- Significant variables: footfall, marketing_spend, inventory, customer_rating, South, West, High Street, Residential
- Not significant: North region, Mall store type
- Recommended model.

---

## Summary Table

| Model | R-squared | Significant? | Use? |
|---|---|---|---|
| Model 1 — marketing_spend | 0.1672 | Yes | No |
| Model 2 — footfall | 0.7363 | Yes | No |
| Model 3 — inventory | 0.0131 | Marginally | No |
| Model 4 — Multiple | 0.8312 | Yes | **Yes** |

---

## Why Model 4
R-squared improved from 0.74 to 0.83 by adding more variables. It also captures regional and store type differences which the simple models miss.

---

## Limitations
- ~17% of sales variation is still unexplained
- Regression shows association, not causation
- Only 4 months of data — seasonal patterns may not be fully captured
