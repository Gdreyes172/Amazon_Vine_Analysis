# Amazon_Vine_Analysis
Using PySpark language and SQL, this project was to analyze reviews to determine bias towards Amazon product reviews on the basis of Vine members sponsorship.
### Overview:
#### This analysis focused on US digital video download review: "https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Digital_Video_Download_v1_00.tsv.gz"
![Before_dropna](https://github.com/Gdreyes172/Amazon_Vine_Analysis/blob/main/Resources/Uncleaned_dfCount.png)
##### Uncleaned Dataframe
![Post_dropna](https://github.com/Gdreyes172/Amazon_Vine_Analysis/blob/main/Resources/cleaned_dfCount.png)
##### Cleaned Dataframe
#### Before committing to this set of reviews we hoped to identify any nulls and remove them from our dataframes. 
### It was important to identify how many reviews we were starting with to compare against the dataframe were created dropping all nulls. 
### As shown above, the difference was about 630 dropped votes. Out of our 4 million reviews, this wasn’t a total loss. So it seemed logical to continue forward with the analysis. 
### Upon completing the filtering of our reviews by review id, product id, star rating, helpful votes, and participation in the vine program (Yes/ No), and the verified id, our first filter of digital downloads for vine paid videos revealed no results. 
### This was concerning but with the 600 or so dropped nulls, we may have deleted the only vined sponsored downloads. 
### So we went on to collect the rest of the data based on the “cleaned_df” DataFrame. It would be assumed we should still be able to use this data to articulate what unpaid downloads were helpful and how many.
![Summary](https://github.com/Gdreyes172/Amazon_Vine_Analysis/blob/main/Resources/summary.png)
##### Cleand Data Summary
### As seen in our image above you’ll find the 4,056,518 reviews with nulls removed, “total_fivestar” reviews, “paid_total” reviews, the “upaid_total”, “fivestar_paid”, and “fivestar_unpaid.
### Looking at the results, it’s clear that the vine program did not influence these reviews at all. The program was never used to promote any particular product. 
---
## Results:
### A few more lines of code were ran outside of the analysis to confirm that the original DataFrame with nulls in it didn't contain any "Y" vine paid downloads.
### It's clear that either these products are not valueble enough to sponsor through the vine program or perhaps this was just a missed oportunity. 
### One thing is certain, the community reviewing these videos are probably true fans and the reviews they leave behind are likely not corrupted by marketing strategies. Well.., at least this can be said for the reviews that have been found useful. 
