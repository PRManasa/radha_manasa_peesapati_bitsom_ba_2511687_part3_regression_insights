# Residual Analysis
**Model used:** Model 4 (Multiple Regression)  
**Name:** Radha Manasa Peesapati | **Date:** June 2026

---

## Residual
Residual = Actual Sales − Predicted Sales. Positive means the store did better than expected. Negative means it did worse.

---

## Top 5 Positive Residuals (Under-predicted)

| Store | Region | Type | Actual | Predicted | Residual |
|---|---|---|---|---|---|
| STR-1028 | East | Mall | 713,611 | 597,729 | +115,882 |
| STR-1073 | East | Residential | 813,317 | 702,192 | +111,125 |
| STR-1019 | East | Residential | 788,088 | 697,763 | +90,324 |
| STR-1026 | East | Mall | 625,514 | 538,361 | +87,153 |
| STR-1050 | North | Residential | 735,787 | 648,708 | +87,079 |

These stores sold more than the model expected. Something outside the model is helping them — possibly strong local demand, better management, or promotions not captured in the data.

---

## Top 5 Negative Residuals (Over-predicted)

| Store | Region | Type | Actual | Predicted | Residual |
|---|---|---|---|---|---|
| STR-1017 | West | High Street | 685,379 | 844,585 | -159,206 |
| STR-1023 | South | Mall | 627,172 | 769,876 | -142,704 |
| STR-1012 | West | Residential | 595,468 | 713,036 | -117,569 |
| STR-1007 | West | Mall | 800,452 | 915,004 | -114,552 |
| STR-1009 | North | Residential | 641,865 | 743,049 | -101,184 |

These stores underperformed relative to expectations. Possible reasons include local competition, execution issues, or pricing problems not in the dataset.

---

## Patterns
- East stores tend to outperform predictions
- West stores dominate the negative residuals — model may be overestimating West store potential
- Residential stores appear in both lists — high variability within this store type

---

## Limitations
- Residuals don't explain why stores over or underperform, just that they do
- Large residuals likely indicate missing variables in the model
