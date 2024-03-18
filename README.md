# Analyzing Quick Dosa's Promotional Campaign Effectiveness through A/B Testing and Chi-Square Analysis

## Background
* Quick Dosa in our scenario is a pioneering fast-food chain specializing in vegetarian South Indian cuisine. Quick dosa rapidly expanded to 163 franchised restaurants across major cities within two years of its launch. Despite its success, overcrowding issues in dine-in spaces began to impede growth. To address this, Quick Dosa aimed to boost its takeout business by launching a promotional campaign through digital display ads. The campaign offered two options: Promotion A - a complimentary soft drink with takeout orders over $7.50, and Promotion B - a 5% discount on orders over $7.50. To determine the more effective promotion, an A-B test was conducted over one week to determine which propmotion strategy was best.

## Testing Strategy
* During the test week, Quick Dosa targeted individuals in Buffalo, NY with display ads on food-themed websites. Each person was randomly assigned to either group A or group B, where group A saw Promotion A ads and group B saw Promotion B ads. Clicking on an ad directed individuals to Quick Dosa's website to place a takeout order, with the promotion automatically applied. All clicks resulted in orders, but a 4% cart abandonment rate occurred due to credit card issues. To determine the best strategy, we will analyze the return on advertising (ROA) percentage to maximize revenue and minimize costs during both lunch and dinner hours. The best strategy will be rolled out to the remaining franchised restauranst in the other major cities. 

## Test Week Results
* At the end of the test week, Promotion A ads were served 24,963 times, while Promotion B ads were served 25,102 times. The dataset accompanying this case includes 50,065 rows of data, each corresponding to an ad impression. The columns in the dataset are as follows:
* Column A: Anonymized Individual ID
* Column B: Promotion (A or B)
* Column C: Clicked (1) or not (0)
* Column D: Takeout order amount ($) - available only for those who clicked, recorded before any promotional discount or cart abandonment.
* Column E: Indicator for whether the order was for lunch (1) or dinner (0), with a cutoff time of 3 pm to classify orders based on the time the ad was shown to the consumer

## Costs Breakdown/Assumptions
* The cost to Quick Dosa of a soft drink that is given away with Promotion A is $0.25.
* Promotion B - a 5% discount on orders.
* The average contribution margin on both lunch and dinner orders is 40% of before- promotion revenue.
* The cost per exposure for display advertising is $0.03.
* All clicks resulted in orders, but a 4% cart abandonment rate occurred due to credit card issues.

## Summary
* Based on the analysis, Promotion A achieved a return on advertising (ROA) percentage of 649% during lunch hours and 161% during dinner hours, resulting in a total ROA of 810%, meaning for every $1 spent on advertising $8.10 was generated in incremental contribution. In contrast, Promotion B yielded a ROA of 281% during lunch and 388% during dinner, totaling 669% ROA, meaning for every $1 spent on advertising $6.69 was generated in incremental contribution.
* Given these results, Promotion A emerges as the more lucrative option, maximizing revenue and minimizing costs. Therefore, it is advisable to roll out Promotion A to Quick Dosa's other franchised restaurants.

## Procedure
* To begin our analysis I wanted to validate the success of the random assignment of individuals to Promotion A and Promotion B, we conducted a chi-square test to confirm the independence of individual IDs' distribution from the promotional condition. We created a pivot table comparing the observed count of individuals in each promotion with the expected count, ideally being evenly distributed between the two groups. After obtaining our data, we performed a chi-square test using the observed and expected values, yielding a p-value of 0.53.
  * My null hypothesis stated that there is no association between the promotional condition and the distribution of Individual IDs, while the alternative hypothesis suggested otherwise. With a p-value greater than 0.05, indicating no statistical significance, we concluded that the distribution of individuals was successful at an alpha = 0.05, affirming the validity of the random assignment and accepting the null hypothesis.
    
* We proceeded to examine the click-through rates (CTR) for each promotion to determine if they were independent of the promotion shown. By creating a pivot table and calculating the CTR, we found that Promotion A had a CTR of 2.22%, while Promotion B had a CTR of 3.02%. To assess if these rates were statistically equal, we compared the observed values of clicks and non-clicks with the expected values and conducted a chi-square test, resulting in a p-value of 0.00000008.
  * The null hypothesis posited that there is no association between the promotional condition and the click-through rates for each promotion, while the alternative hypothesis suggested otherwise. With a p-value less than 0.05, indicating statistical significance, we concluded that the click-through rate is dependent on the promotion shown at an alpha level of 0.05, thereby rejecting the null hypothesis and accepting the alternate hypothesis.

* I decided to further explore click-through rates (CTR) by analyzing activity during lunch and dinner times. Using a pivot table, I examined the sum of clicks for each promotion during their respective meal periods. For Promotion A, the lunchtime CTR was 1.91%, significantly higher than the 0.31% observed during dinner hours, suggesting that individuals predominantly utilized this promotion during lunch. On the other hand, Promotion B exhibited a lunchtime CTR of 1.55% and a dinner CTR of 1.47%, indicating a relatively even distribution of utilization throughout the day.
* After calculating the CTR for each meal period for each promotion, I proceeded to determine the average meal cost during each meal period. Using a pivot table, I analyzed each promotion and their respective average takeout order. For Promotion A, the average lunch order was $24.68, slightly higher than the dinner average of $24.37. Similarly, for Promotion B, the average lunch order amounted to $23.62, with a dinner average of $23.59. These findings indicate that individuals tend to spend more money during both lunch and dinner periods for Promotion A compared to Promotion B.

* After computing insightful statistics such as the click-through rate (CTR) during each meal period for each promotion and the average meal costs, it was imperative to assess the profitability of each promotion by calculating the return on advertising (ROA) percentage.
  * First, I created a pivot table to determine the sum of takeout orders for each promotion during both meal periods, factoring in the 4% cart abandonment rate to find the actual total revenue generated.
  * Then, assuming each click resulted in a purchase, I adjusted the number of clicks to reflect the number of purchases after incorporating the 4% cart abandonment rate.

* For Promotion A, the promotional costs during each meal period were calculated by multiplying the number of purchases in each period by $0.25 to account for the cost of the free soft drink. For Promotion B, the promotional costs during each meal period were determined by multiplying the total revenue generated from the promotion by 5%.

* Additionally, I calculated the ad-exposure costs by multiplying the total individuals shown each promotion in each meal period by $0.03.
  * The total costs were then obtained by summing the promotional costs and ad-exposure costs for each meal period and promotion.

* Finally, using the ROA percentage formula [(contribution margin - total costs) / total costs], I computed the profitability of each promotion during each meal period, to determine which promotion maximized revenue and minimize costs.
  * Promotion A demonstrated superior profitability, boasting a lunch period ROA of 649% and a dinner period ROA of 161%, culminating in a total ROA of 810%. Given these impressive results, Promotion A should be rolled out to the other cities.
 
 ## Screenshot of Outputs
![](/images/Chi_Squared_Test_Random_Assignment.png)

![](/images/Chi_Squared_Test_CTR1.png)

![](/images/Promotion_A-B_Meals_CTR.png)
![](/images/Promotion_A-B_Avg_Meal_Costs.png)

![](/images/Promotion_A-B_ROA_Data1.png)

![](/images/Promotion_A-B_ROA_Calculations4.png)






