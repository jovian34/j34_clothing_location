# j34_clothing_location

# Chi-square test on online store purchases
## Masters in Data Analytics Capstone

Carl James
College of Information Technology, Western Governors University
October 12th, 2023
 
## Chi-square test on online store purchases
### A. Executive Summary
	In an online retail clothing store, how the products are merchandised can impact sales (Ecwid, N.D.). This analysis studied the impact of product placement on sales quantities. Specifically, does the distribution between large and small quantity purchases differ significantly based upon the page and position of the first item a customer purchases in a transaction.
	The null hypothesis is that the distribution of large and small orders is the same for all purchases and for subsets segmented by the page and position of the first item the customer purchases. The alternate hypothesis is that the distribution differs significantly.

#### Data Analysis Process
	The clickstream data including 165,174 items purchased was imported into a Python Jupyter Notebook (clickstream, 2019). The original 14 features were reduced to 5 that were useful to this analysis. Dummy variables were then created with Boolean values for location and page showing if the clothing item was in that location or on that page when purchased. Variables were then calculated for each combination of location and page with a similar Boolean value.
	The rows were reduced to include only the first item purchased in each transaction and include a new feature showing how many items were included in each of the 24,026 transactions. Another feature was calculated as a Boolean value showing True for orders with more than three items in the order. Looking at all transactions it was calculated that 54.3% of transactions were more than three items, which is being called a large order.
	The analysis then calculated the large order rate for transactions where the first item purchased was in each location, page, and combination of location and page. Those rates were compared via a Chi-square test to an alpha p-value of 5%. If the p-value was below 5% the null hypothesis was rejected for that subset of the data. A data frame showing the p-value and rejection or acceptance of the null hypothesis for each of the 41 positional possibilities was stored.

#### Findings
	The null hypothesis was rejected in 24 of the 41 positional subsets of the transaction data. The combination of the first page and first position had the lowest p-value and thus the most significant difference for the distribution of large orders in all transactions. This study shows that item placement on the website is a significant factor in order quantity

#### Limitations
	 A limitation of the analysis is that the positions of the items on the website were taken at different times. Those could have corresponded to different promotional events which could have impacted the order size. Since Chi-square compares just one variable, another limitation is that this analysis defines large orders only by item quantities and does not factor the pricing data at all.

#### Proposed Actions
	The recommendation for next action is gathering better data that can control for other variables that are being directly tested. To that end, one approach to further study is to gather better data with controlled A/B tests, where the business selects a placement of items on the site that would maximize order quantities to increase sales, but controls for other variables (Indarjo, 2020).

#### Expected Benefits
	Knowing that item placement is significant related to order quantities gives the business an opportunity to make small and relatively inexpensive changes to increase total sales. It also shows that the most prominent location on the site, the first item on the first page, shows the most significant difference. This can help the business in devising more controlled tests that can provide specific recommended changes to the website to drive improved sales.

## Sources

clickstream data for online shopping. (2019). UCI Machine Learning Repository. https://doi.org/10.24432/C5QK7X 
Ecwid. (N.D.) Merchandising 101: Everything You Need to Know About Product Merchandising. https://www.ecwid.com/blog/all-about-product-merchandising.html 
Indarjo, P. (2020). Meet the Engine of A/B Testing: Chi Square Test. Medium. https://medium.com/bukalapak-data/meet-the-engine-of-a-b-testing-chi-square-test-30e8a8ab44c5

