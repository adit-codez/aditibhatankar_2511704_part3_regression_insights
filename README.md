# 📊 Regression Analysis Project
1. Business Problem Summary
The goal of this project is to analyze the impact of marketing spend and other business factors (customer rating, discount percentage, and regional differences) on monthly sales. The objective is to identify which variables significantly drive sales and provide actionable recommendations for business decision-making.

2. Dataset Description
Observations: 306 rows of monthly sales and predictor variables.

Variables included:

Marketing Spend (continuous)

Customer Rating (continuous)

Average Discount % (continuous)

Region (categorical: East, North, West, South as baseline)

Monthly Sales (dependent variable)

3. Dependent and Independent Variables
Dependent Variable: Monthly Sales

Independent Variables:

Marketing Spend

Customer Rating

Average Discount %

Dummy Variables for Region (East, North, West)

4. Regression Approach
Two regression models were built:

Model 1: Simple Regression → Monthly Sales ~ Marketing Spend

Model 2: Multiple Regression → Monthly Sales ~ Marketing Spend + Customer Rating + Avg Discount % + Region Dummies

5. Dummy Variable Approach
Categorical variable Region was encoded using dummy variables (East, North, West). The South region was treated as the baseline category to avoid multicollinearity.

6. Model Comparison Summary
Criteria	Model 1: Simple Regression	Model 2: Multiple Regression
R-Squared	0.1574 (15.74%)	0.1951 (19.51%)
Adjusted R-Squared	0.1547	0.1789
Significant Variables	Marketing Spend (p < 0.001)	Only Marketing Spend (p < 0.001)
F-Statistic	56.80 (p < 0.001)	12.08 (p < 0.001)
Standard Error	$94,635	$93,267
Business Usefulness	Clear ROI insight	Added complexity, poor predictive value


7. Final Model Selected
Model 1: Simple Regression was chosen as the final model because:

Marketing Spend is the only consistently significant predictor.

Additional variables (Customer Rating, Discount %, Region) do not improve explanatory power meaningfully.

The model provides a clear, actionable ROI interpretation.

8. Business Recommendation
Invest in Marketing Spend: Each $1 spent on marketing yields approximately $2.05 in sales increase, making it a profitable strategy.

Avoid reliance on Customer Ratings or Discounts: These variables do not significantly predict sales. Discounts may even negatively impact revenue.

Regional differences are not statistically significant, so marketing strategies should be applied uniformly across regions.

9. Assumptions and Limitations
Linear relationship assumed between predictors and sales.

Dataset limited to 306 observations; results may vary with larger or more diverse data.

External factors (seasonality, competitor actions, macroeconomic trends) not included.

Model explains ~15–19% of variance in sales, meaning other unobserved factors also influence outcomes.
