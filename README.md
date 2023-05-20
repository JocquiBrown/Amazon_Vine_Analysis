# Amazon_Vine_Analysis
## Overview
- The purpose of this analysis is to perform an ETL on Amazon product reviews in order to determine the bias of Vine member reviews for video games. In order to perform the ETL, the review dataset for video games was extracted from the list of datasets, the dataset was then transformed into several dataframes. The vine table, which displayed information regarding reviews such as the number of upvotes the review received, the star rating for the review and whether or not the review was a part of the Vine program, was the table used for our analysis.

## Results
- The image below dispalys the unfiltered version of the vine table which consists of the following columns:
  - review_id: The unique ID of the review
  - star_rating: A 1-5 star rating of the review
  - helpful_votes: The number of helpful votes (upvotes) the review received
  - total_votes: The total number of votes the review received
  - vine: Whether or not the review was written as part of the vine program
  - verified_purchase: Whether or not the review was on a verified purchase
  
![Big_Data_Challenge_Screenshot_1](https://github.com/JocquiBrown/Amazon_Vine_Analysis/assets/120291854/8c1e6fbf-2869-4b5d-9221-eb16e8ca2af2)

- Before an analysis was performed the Vine table was filtered to remove all reviews with vote totals under 20 and all reviews where the ratio of helpful votes to total votes was less than half. This left only the reviews with significant votes that voters found helpful. This allows our analysis to be better targeted toward reviews that people actually found useful and the resulting filtered table can be seen below: 

![Big_Data_Challenge_Screenshot_2](https://github.com/JocquiBrown/Amazon_Vine_Analysis/assets/120291854/4c05e17d-5884-4f37-96be-2800ef5fdaa9)

- To determine whether or not there was any bias towards favorable reviews from Vine members, the filtered table was split into Vine program reviews and Non-vine program reviews before being counted. Once the number of reviews were counted for each category, the number of 5-star reviews were also tallied for each type of review and finall a percentage of 5-star reveiws for each review type were calculated. These results are listed below:

- Vine Reviews for Video Games
  - Number of Vine Reviews: 94
  - Number of 5-star Vine Reviews: 48
  - Percentage of 5-star Vine Reviews: 51%
  
- Non-vine Reviews for Video Games
  - Number of Non-vine Reviews: 40,471
  - Number of 5-star Non-vine Reviews: 15,663
  - Percentage of 5-star Non-vine Reviews: 39%
  
## Summary
- Based on the results gathered from our analysis, it is reasonable to conclude that there is a positivity bias from Vine program reviews for video games. This means that Vine program reviews are more likely to yield positive, specifially 5-star, ratings than Non-vine program reviews. This conculsion is supported by the "percentage of 5-star reviews" metric that was calculated for both Vine and Non-vine reviews. According to the observations, over half of all Vine program reviews received a 5-star rating (51%), while less than 40% of Non-vine reviews received the coveted rating (39%). To further support our conclusion, an additional analysis could be performed that compared the number of 1-star reviews between the two review types. This additional analysis would look for a negativity bias in reviews that would allow us to see whether or not Vine members are also less likely to write a negative review than Non-vine members, as this would also help to confirm a positive review bias from Vine members.
