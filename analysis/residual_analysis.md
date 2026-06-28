Residual Analysis
File: analysis/residual_analysis.md
Model Used: Simple Regression — Marketing Spend
Only
Equation: Predicted Sales = 567,463.56 + 2.05 ×
Marketing_Spend
 
What Is a Residual?
A residual is simply the difference between what actually happened and what our model predicted:
Residual = Actual Sales − Predicted Sales
A positive residual means the store sold MORE than the model expected → the model UNDER predicted
 	A negative residual means the store sold LESS than the model expected → the model OVER predicted
 
Step 1: How Predicted Sales Are Calculated
Using the final model equation:
 
Example calculation:
If a store spent $50,000 on marketing:
Predicted Sales = 567,463.56 + (2.05 ×
50,000)
 
Step 2: How Residuals Are Calculated
 
Example:
Actual Sales = $800,000
Predicted Sales = $669,963.56
Residual = +$130,036.44 → Store performed
BETTER than expected
Step 3: Top 5 Records with LARGEST POSITIVE Residuals
(Stores that sold MORE than the model predicted — model UNDER-predicted these)
Rank	Residual
Value	What It Means
🥇
1st	+$220,802.30	This store sold $220,802
MORE than predicted
🥈 2nd	+$215,709.70	This store sold $215,710
MORE than predicted
🥉
3rd	+$207,318.40	This store sold $207,318
MORE than predicted
4th	+$203,838.30	This store sold $203,838
MORE than predicted
5th	+$183,158.30	This store sold $183,158
MORE than predicted
These stores are outperforming expectations. The model underestimated their sales, likely because factors beyond marketing spend (great location, loyal customers, high foot traffic) are boosting their performance.

Step 4: Top 5 Records with LARGEST NEGATIVE Residuals
(Stores that sold LESS than the model predicted — model OVER-predicted these)
Rank	Residual
Value	What It Means
🔴
1st	-$282,804.55	This store sold $282,805
LESS than predicted
🔴 2nd	-$256,917.97	This store sold $256,918
LESS than predicted
🔴
3rd	-$230,722.65	This store sold $230,723
LESS than predicted
🔴
4th	-$215,872.15	This store sold $215,872
LESS than predicted
🔴
5th	-$214,030.75	This store sold $214,031
LESS than predicted

Side-by-Side Comparison
	Positive
Residuals
(Stars ⭐)	Negative
Residuals
(Concern 🚨)
Largest gap	+$220,802	-$282,805
Total gap
(all 5)	+$1,030,827	-$1,200,348
Model behaviour	Under-predicted	Over-predicted
Business signal	Hidden strengths to study	Problems to investigate
 
Step 5: What Do These Residuals Mean in Business Terms?
Stores with Large Positive Residuals (Model Under-Predicted)
These stores are hidden gems. They are performing way better than what our marketing spend data alone would suggest. This could be because:
They have very loyal, repeat customers
They are in excellent locations (high foot traffic, near schools, offices etc.)
 	They may have great store managers or customer service
Word-of-mouth is working well for them
They sell products that are in high demand in their area
Business Action: Study these stores. What are they doing right? Can we replicate their success in other stores?
Stores with Large Negative Residuals (Model Over-Predicted)
These stores are underperformers. They spend a lot on marketing but still sell less than expected. This could be because:
 	Their location has poor foot traffic or competition nearby
 	The marketing money is being spent inefficiently
(wrong channels, wrong audience)
Local economic conditions are weak
Product mix doesn't match customer needs in that area

Business Action: Investigate these stores urgently. Should we reduce their marketing budget? Do they need operational support? Should we reconsider their location strategy?
 
Step 6: Is the Model Over-Predicting or Under-Predicting Certain Stores?
Yes — the model shows a clear pattern:
The model tends to OVER-PREDICT for:
 	Stores with very HIGH marketing spend but in weak markets
Stores that face strong local competition
Stores in low-income or rural areas where spending power is limited
The model tends to UNDER-PREDICT for:
 	Stores in premium locations that naturally attract customers
 	Stores with long-established brand loyalty in their area
 	Stores that benefit from events, foot traffic, or word-of-mouth (factors not captured in the model)
Why Does This Happen?
Our model only uses marketing spend to predict sales. But in reality, many other factors affect sales:
Store location and foot traffic
Local competition
Product quality and variety
Staff performance
Economic conditions of the area Seasonal trends
Since these factors are not in our model, the residuals capture all of these "hidden" influences.
 
Summary Table
Category	What It Means	Business
Response
Large +
Residual	Store is a star performer	Investigate & copy their success
Large -
Residual	Store is underperforming	Investigate causes & intervene
Category	What It Means	Business
Response
Consistent + Residuals in one region	Region performs better than model thinks	Model needs region variable
Consistent Residuals in one region	Region underperforms	Investigate regional factors
 
Standard Error of the model = $94,635.42 — this means on average, our predictions are off by about $94,635 per store per month.

