Comparison Criteria	Model 1: Simple Regression	Model 2: Multiple Regression
Model Name	
Simple Regression: Marketing Spend Only

Multiple Regression: Marketing + Customer Rating + Average Discount% + Regions

Variables Used	
Independent: Marketing_spend  Dependent: Monthly_sales	
Independent:    Marketing_spend Customer_rating, Avg_discount_pct, Dummy Variables(Region East, Region North, Region West)           Dependent: Monthly_sales

R-Squared(Explanatory Power)	
0.1574 (15.74%)	
0.1951 (19.51%)

Adjusted R-Squared
0.1547 (15.47%)	
0.1789 (17.89%)

Significant Variables (p < 0.05)	

Marketing_Spend p-value: 5.5809E-13 (Highly Significant) Intercept p-value: 4.24E-108
Marketing_Spend ONLY p-value: 3.42E-13
(HIGHLY SIGNIFICANT)                      Customer_rating  p-value:0.799 (NOT SIGNIFICANT)                 Avg_discount_pct  p-value:                0.229 (NOT SIGNIFICANT)                  ALL Region Variables p-values:     0.138 - 0.312                                   (NOT SIGNIFICANT)                     
F-Statistic & Model Significance	F-Statistic: 56.80                                  P-value: 5.5809E-13	F-Statistic: 12.08                                     P-value: 3.73E-12
Standard Error	$94,635.42	$93,267.00

Business Usefulness & Practical Value	

USEFUL FOR DECISIONS
Coefficient: $2.05
Interpretation: Each $1 spent on marketing yields $2.05 in sales increase    
ROI: Profitable (Revenue > Cost)     
Practical Impact: Clear, Actionable insight

POOR FOR DECISIONS                    
5 of 6 variables NOT SIGNIFICANT                                                 
Added complexity without value 
Customer rating doesn't predict sales 
Discount % negatively affects sales
