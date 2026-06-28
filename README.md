# Part 3:

## Business Problem
A retail chain wanted to understand what factors drive monthly sales performance across stores. Leadership is considering actions such as increasing marketing spend, improving inventory, changing discounting strategy, and reallocating staff. Regression analysis was used to identify which factors are most strongly associated with monthly sales.


## Dataset
**File:** business_regression_data.xlsx  
**Records:** 320 (80 stores × 4 months)  
**Columns:** 14 — store_id, month, region, store_type, marketing_spend, footfall, avg_discount_pct, staff_count, inventory_availability_pct, competitor_distance_km, holiday_flag, customer_rating, monthly_sales, monthly_profit


## Variables

**Dependent variable:** monthly_sales

**Independent variables used:**
- marketing_spend (numerical)
- footfall (numerical)
- inventory_availability_pct (numerical)
- customer_rating (numerical)
- region (categorical — converted to dummies, ref: East)
- store_type (categorical — converted to dummies, ref: Airport)

**Variables not used in final model:**
- avg_discount_pct — not statistically significant
- staff_count — collinear with footfall
- competitor_distance_km — 6 missing values, weak predictor
- holiday_flag — binary, minor effect
- monthly_profit — outcome variable, not a predictor


## Regression Approach
Three simple regression models and one multiple regression model were built. All models used monthly_sales as the dependent variable. Excel's Data Analysis ToolPak was used for regression outputs.


## Dummy Variable Approach
Region (4 categories) and store_type (4 categories) were each converted to 3 dummy variables using East and Airport as reference categories respectively. This avoids the dummy variable trap (perfect multicollinearity).


## Model Comparison Summary

| Model | R-squared | Key Variable | Recommended? |
|---|---|---|---|
| Simple — marketing_spend | 0.1672 | marketing_spend | No |
| Simple — footfall | 0.7363 | footfall | No |
| Simple — inventory | 0.0131 | inventory_availability_pct | No |
| **Multiple — all vars** | **0.8312** | footfall, inventory, store_type | **Yes** |


## Final Model
**Multiple regression** with footfall, marketing_spend, inventory_availability_pct, customer_rating, region dummies, and store_type dummies. R-squared = 0.8312.


## Business Recommendation
Footfall is the strongest predictor of sales. Inventory availability and customer rating are also significant. Residential stores underperform Airport stores by ~$42,662/month on average. South and West regions outperform East. Discount percentage is not a significant predictor — discounting should not be the primary lever.


## Assumptions and Limitations
- Regression shows association, not causation
- 17% of sales variation is unexplained by the model
- Analysis covers 4 months only — seasonal effects may be limited
- Missing values in competitor_distance_km and customer_rating were filled with median values


## Screenshots

| File | Description |
|---|---|
| simple_regression_output.png | Simple regression output (footfall model) |
| multiple_regression_output.png | Multiple regression output |
| residuals_preview.png | Predicted values and residuals |
| model_comparison_preview.png | Model comparison table |
