# Model Equations
**Name:** Radha Manasa Peesapati | **Date:** 28 June 2026

---

## Simple Regression Equations

**Model 1 — Marketing Spend**
```
monthly_sales = 569,296 + 2.13 × marketing_spend
```

**Model 2 — Footfall**
```
monthly_sales = 446,232 + 35.68 × footfall
```

**Model 3 — Inventory Availability**
```
monthly_sales = 484,603 + 2,217.83 × inventory_availability_pct
```

---

## Multiple Regression Equation (Final Model)

```
monthly_sales = 82,185
              + 1.21 × marketing_spend
              + 34.01 × footfall
              + 3,048.11 × inventory_availability_pct
              + 13,520.58 × customer_rating
              + 6,089.50 × region_North
              + 20,117.94 × region_South
              + 18,492.64 × region_West
              - 24,559.91 × store_High_Street
              - 13,287.02 × store_Mall
              - 42,662.45 × store_Residential
```

---

## Coefficient Meanings

| Variable | Coefficient | Meaning |
|---|---|---|
| marketing_spend | +1.21 | $1 more spend → ~$1.21 more sales |
| footfall | +34.01 | 1 more visitor → ~$34 more sales |
| inventory_availability_pct | +3,048 | 1% more inventory → ~$3,048 more sales |
| customer_rating | +13,521 | 1-point rating increase → ~$13,521 more sales |
| region_South | +20,118 | South stores earn ~$20,118 more than East |
| region_West | +18,493 | West stores earn ~$18,493 more than East |
| store_Residential | -42,662 | Residential earns ~$42,662 less than Airport |

---

## Dummy Variables

**Region** — 4 categories, 3 dummies created. Reference category: **East**
- region_North, region_South, region_West

**Store Type** — 4 categories, 3 dummies created. Reference category: **Airport**
- store_High Street, store_Mall, store_Residential

One category is dropped from each group to avoid the dummy variable trap.

---

## Final Model Selected
Model 4 (Multiple Regression) — R-squared of 0.8312 versus 0.7363 for the best simple model. Captures both operational and structural factors.
