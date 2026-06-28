Model Equations
File: outputs/model_equations.md
 
1.	Simple Regression Equation
What Is Simple Regression?
Simple regression uses one factor to predict sales. We tested which single variable best explains monthly sales.
 
Simple Regression: Marketing Spend Only Mathematical Equation:
 
In Plain English:
"Even if a store spends zero on marketing, we expect it to generate about $567,464 in base sales. For every extra $1 spent on marketing, sales increase by $2.05."
Key Statistics:
 	R² = 15.74% → Marketing spend explains about
16% of the variation in sales  	p-value = 5.58E-13 → Extremely statistically significant (near zero chance this is random)  Standard Error = $94,635
2.	Multiple Regression Equation
What Is Multiple Regression?
Multiple regression uses several factors at once to try to predict sales more accurately.
 
Multiple Regression: All Variables Combined Mathematical Equation:
Monthly Sales = 565,566.87
             + (2603.75 × Customer_Rating)
             + (-95,280.07 × 
Avg_Discount_Pct)
             + (2.05 × Marketing_Spend)              + (21,392.34 × Region_East)
             + (17,773.49 × Region_North)
             + (-23,840.48 × Region_West)
In Plain English:
"Starting from a base of $565,567, sales go up or down depending on customer ratings, discount percentage, marketing spend, and which region the store is in."
Key Statistics:
 	R² = 19.51% → All 6 variables together explain about 19.5% of sales variation
 	Adjusted R² = 17.89% (after penalising for the extra variables)
Standard Error = $93,267
F-statistic p-value = 3.73E-12 → Model is statistically significant overall
 
3.	Explanation of Each Coefficient

Variable	Coefficient	What It
Means in Business
Language
Intercept	$565,566.87	The expected base monthly
sales if all variables are zero
Customer_Rating	+$2,603.75	For every 1star increase in customer rating, sales increase by $2,604 — BUT this is NOT statistically significant (p
= 0.799)
Avg_Discount_Pct	-$95,280.07	For every 1% increase in average discount, sales
DECREASE by
$95,280 — NOT
statistically

Variable	Coefficient	What It
Means in Business
Language
		significant (p
= 0.229)
Marketing_Spend	+$2.05	For every $1 spent on marketing, sales increase by $2.05 — HIGHLY
SIGNIFICANT
(p ≈ 0)
Region_East	+$21,392.34	East region stores sell
$21,392
MORE than South (base) stores — NOT significant (p
= 0.178)
Region_North	+$17,773.49	North region stores sell
$17,773
MORE than South (base) stores — NOT
Variable	Coefficient	What It
Means in Business
Language
		significant (p
= 0.312)
Region_West	-$23,840.48	West region stores sell
$23,840 LESS than South
(base) stores
— NOT
significant (p
= 0.138)
Key Takeaway: Out of 6 variables, only Marketing Spend has a statistically reliable relationship with sales.
4.	Explanation of Dummy Variables
What Are Dummy Variables?
Some information is categorical (not numbers) — like which region a store is in. We can't put "East" or "North" directly into a math equation. So we convert them into dummy variables — simple 0 or 1 values.
How We Created Region Dummies:
Store
Region	Region_East	Region_North	Region_West
East	1	0	0
North	0	1	0
West	0	0	1
South	0	0	0
So for a store in the East → Region_East = 1, all others = 0
For a store in the South → all three = 0 (it gets the intercept only)
 
5.	Reference Category
The reference category (baseline) for Region is:
SOUTH
This means:
 	All regional coefficients are compared against
South region stores
 	Example: Region_East = +$21,392 means East stores earn $21,392 MORE than a comparable South store
 	The South region's effect is already "baked into" the intercept value
We chose South as the reference category because it's a common benchmark region in this dataset.
 
6.	Final Model Selected
✅ FINAL MODEL: Simple Regression —
Marketing Spend Only
 
7.	Reason for Selecting the FinalModel
We chose the Simple Regression model over the Multiple Regression model for the following reasons:
Statistical Reasons:
 	In the Multiple Regression model, 5 out of 6 variables were NOT statistically significant (pvalue > 0.05)
 	Only Marketing Spend had a p-value near zero
(5.58E-13), making it the only reliable predictor
 	The Adjusted R² improved from 15.47% (simple) to only 17.89% (multiple) — a very small gain for adding 5 more variables
 	Adding non-significant variables can actually hurt the model by introducing noise
Business Reasons:
 	The simple model gives a clear, actionable insight: spend more on marketing → earn more in sales
 	The multiple model's other variables (customer rating, discount %) did not help predict sales reliably
 	A simpler model is easier to explain to leadership and easier to act on
 	The coefficient of $2.05 per $1 of marketing spend is a direct ROI metric — every $1 spent returns $2.05 in sales, meaning it is profitable
Principle of Parsimony:
"All else being equal, the simpler model wins." The simple model is nearly as accurate, much clearer, and more useful for business decision-making.
Both models have relatively low R² values (15-20%), meaning there are still many factors not captured in this dataset that influence sales. Future analysis could include foot traffic, competitor proximity, store size, and seasonal data.

