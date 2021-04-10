# Buying a Home in NYC: What Neighborhoods are the Best Value?
### Applying Data Science Tools to Understand NYC's Residential Real Estate Fundamentals

    Josh Grasso | joshgrasso@gmail.com

This project seeks to understand the fundamental factors that explain differences in residential real estate prices across NYC. What might explain why the average brownstone in Tribeca costs \\$10mm, while the average brownstone in Williamsburg is only \\$2mm and is \\$685k in Flushing?

The fundamental factors used in this analysis are: 

1) Commute time and the number of transfers, to get to Midtown, Manhattan via public transit, courtesy of the Directions API from Google Maps 

2) The quality of a neighborhood’s zoned schools – both public and charter – as measured by the NYC Department of Education’s standardized math test score results, administered to all 1,000+ elementary and middle-schools in NYC

3) How safe is the neighborhood, based on statistics from the NYPD identifying every shooting incident that has taken place in NYC since 2006

4) And how desirable is the neighborhood, as measured by the number of local restaurants that are highly-rated on Foursquare, with a rating of 8.5 or above (out of 10.0)

The housing price data used in this analysis is pulled from two sources. One is the NYC Department of Finance, available down to the granularity of actual, individual sales transactions, going back to 2003. The Department of Finance (DoF) collects and uses this data to administer property taxes. The full, public, transaction-level database has over 1.6mm individual transactions, of which 335k or 21\% are single family residences. The second is from Zillow, and is a measure of the value of a “typical” home (in the 35th to 65th percentile), and which is available at the neighborhood level for 235 neighborhoods in NYC, as far back as 1996. 

The two main questions this project seeks to answer are: 
* Based on actual real estate prices across all neighborhoods in NYC, what is the average price paid for, for example, a 10-minute shorter commute time, or a zoned school in the top 20\% of schools instead of the top 30\%?  What is the trade-off between cost and these fundamental features – in \\$/minute and \\$/school rank percentile? 
* Second, using a regression of the average prices in all 250+ neighborhoods in NYC, along with the fundamental features of those neighborhoods, which neighborhoods provide the best value? And which neighborhoods seem overvalued? 

The regression model has an R-squared of 0.54 against the Zillow price data and an impressive 0.70 against the NYC DoF price data. This means that out of the difference and variation in average prices from one neighborhood to another (\\$10mm in Tribeca, \\$2mm in Williamsburg, and \\$685k in Flushing), the fundamental feature noted above and relationships identified in the model are able to understand and explain about 2/3rds of this variation. 
