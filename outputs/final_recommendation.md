Final Recommendation & Business Problem Summary
File: outputs/final_recommendation.md
 
Business Problem Summary
The Question We Were Trying to Answer:
"What drives monthly sales across our stores — and how can we use data to predict and improve performance?"
The Data We Had:
We analysed 306 store records with the following information:
Monthly Sales (what we want to predict)
Marketing Spend (how much each store spends on advertising)
 	Customer Rating (average customer satisfaction score)
 	Average Discount Percentage (how much discount was given)
 	Region (East, North, West, South)
Our Approach:
We built regression models — mathematical formulas that find the relationship between these factors and monthly sales. We tested a simple model (one variable) and a multiple model (six variables), then compared which was more useful.
 
Final Recommendation
Recommended Final Model:
Simple Linear Regression — Marketing Spend Only
 
Answering All Required Questions
 
1. Which Factors Appear Most Strongly Associated with Monthly Sales?
Marketing Spend is the only factor with a strong, reliable association with monthly sales.
 	Its p-value is 5.58E-13 — essentially zero — meaning there is less than a 0.0000000001% chance this relationship is due to random chance
 	For every $1 increase in marketing spend, monthly sales increase by approximately $2.05
 	No other variable (customer rating, discount %, or region) showed a statistically significant relationship with sales
In simple terms: Of everything we measured, only marketing spend reliably moves the needle on sales.
 
2. Which Variables Should Leadership Focus On?
Leadership should focus on: Marketing Spend
Here's why it deserves attention:
 	It has the clearest, most statistically proven link to sales
 	The return is measurable: every $1 spent on marketing returns $2.05 in sales
 	This is a profitable ROI — the company is getting
back more than it spends
 	Marketing is also a controllable variable — leadership can directly decide to increase or decrease it
Practical Focus Areas:
 	Which stores are underspending on marketing relative to their potential?
 	Are there stores where increasing marketing budget could unlock higher sales?
 	Is the $2.05 return consistent across all regions, or better in some areas?
 
3. Which Variables Should NOT Be OverInterpreted?
Do NOT over-interpret: Customer Rating, Average Discount %, or Region variables
Variable	pvalue	Should We Trust It?
Customer
Rating	0.799	❌ NOT significant — 80% chance this is random noise
Avg
Discount %	0.229	❌ NOT significant — 23% chance this is random
Variable	pvalue	Should We Trust It?
Region East	0.178	❌ NOT significant
Region
North	0.312	❌ NOT significant
Region
West	0.138	❌ NOT significant
What this means in plain language:
 	Just because a store has a higher customer rating does NOT mean it will have higher sales (based on our data)
 	Giving more discounts does NOT appear to increase sales in a statistically reliable way — in fact the coefficient is negative, suggesting discounts may hurt sales (though we can't fully confirm this without a more significant result)
 	Being in the East, North, or West region versus South does NOT show a statistically reliable sales difference in this dataset
Warning: If leadership makes decisions based on these variables alone (e.g., "let's increase discounts to boost sales"), they might be chasing a false signal.
 
4. What Business Action Would You Recommend?
Recommended Actions:
Action 1: Invest More in Marketing — With Accountability
 	The data shows marketing spend has a clear, positive return of $2.05 per $1 spent
 	Stores currently spending less on marketing should consider increasing their budget, especially if they are in high-potential markets
 	However, track whether the $2.05 return holds — some stores (with large negative residuals) are NOT getting this return despite high spend
Action 2: Audit Underperforming Stores (Large Negative Residuals)
 	Some stores spend heavily on marketing but still underperform sales predictions
 	These stores need a deeper investigation: Is the location poor? Is there nearby competition? Is the product mix wrong?
 	Simply giving them more marketing budget is unlikely to fix the root problem
Action 3: Study Overperforming Stores (Large Positive Residuals)
 	Some stores are selling far more than the model predicts even at modest marketing spend
 	These are the hidden champions — what are they doing differently?
 	Can we identify and replicate the success factors in other stores?
Action 4: Do Not Cut Marketing Based on Discount Strategy
 	The data suggests discounts do not reliably increase sales
 	If the business is currently discounting to drive traffic, this strategy should be re-evaluated
Action 5: Collect Better Data
 	Our model only explains 15-20% of sales variation — 80%+ remains unexplained
 	We recommend collecting data on: store size, foot traffic, competitor proximity, staff headcount, product range, and seasonal factors
 	This will allow building a much more powerful and accurate model in the future
 
5. What Risks or Limitations Should Leadership Keep in Mind?
Risk 1: Low Explanatory Power
 	Our best model only explains 15.74% of the variation in sales  	This means 84%+ of what drives sales is NOT captured in this data
 	Decisions made purely on this model carry significant uncertainty
Risk 2: The Model Is an Average
 	The coefficient of $2.05 is an average across all 306 stores
 	Some stores may get $5 per $1 of marketing; others may get $0.50
 	The model cannot tell us which type of store we're dealing with without more information
Risk 3: Outlier Stores May Distort the Picture
 	Stores with very large positive or negative residuals show the model is not a perfect fit for all stores
 	The model works better as a general guide than a store-by-store predictor
Risk 4: Data Quality
 	We do not know how marketing spend was recorded — was it consistently measured across all stores?
 	Differences in how data was collected can create misleading patterns
Risk 5: The Model May Become Outdated
 	Marketing effectiveness can change over time due to economic conditions, competitor activity, and consumer behaviour shifts
 	The model should be re-run periodically (e.g., every 6–12 months) with fresh data
 
6. Why Does Regression Show Association But Not Automatically Prove Causation?
This is one of the most important concepts in data analysis:
What "Association" Means:
Our regression shows that when marketing spend goes up, sales also tend to go up. That is an association — they move together.
Why This Is NOT the Same as Causation:
Reason 1: Reverse Causality
 	Maybe stores that ALREADY have high sales (due to other reasons) choose to spend MORE on marketing because they can afford it
 	In this case, high sales → high marketing spend,
NOT the other way around
 	We can't tell the direction from regression alone
Reason 2: Confounding Variables (Hidden Factors)
 	A third factor — like store location — might cause
BOTH high marketing spend AND high sales
 	Example: Flagship stores in city centres naturally have more resources (hence more marketing budget) AND more customers (hence more sales)
 	The marketing spend didn't cause the sales; the location did, and the marketing spend is just correlated with it
Reason 3: Coincidence / Statistical Noise
 	Even though our p-value is very low, no statistical test is 100% perfect
 	There remains a tiny possibility that this pattern appeared by chance, especially if there are systematic biases in how stores were selected
The Gold Standard for Proving Causation:
To PROVE that marketing spend CAUSES sales to increase, we would need:
 	A randomised controlled experiment: randomly assign different marketing budgets to stores and measure what happens
 	This is expensive and complex, but it's the only way to be truly certain


