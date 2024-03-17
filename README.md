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

## Summary
* Based on the analysis, Promotion A achieved a return on advertising (ROA) percentage of 649% during lunch hours and 161% during dinner hours, resulting in a total ROA of 810%. In contrast, Promotion B yielded a ROA of 281% during lunch and 388% during dinner, totaling 669% ROA.
* Given these results, Promotion A emerges as the more lucrative option, maximizing revenue and minimizing costs. Therefore, it is advisable to roll out Promotion A to Quick Dosa's other franchised restaurants.

## Procedure
* To begin our analysis I wanted to validate the success of the random assignment of individuals to Promotion A and Promotion B, we conducted a chi-square test to confirm the independence of individual IDs' distribution from the promotional condition. We created a pivot table comparing the observed count of individuals in each promotion with the expected count, ideally being evenly distributed between the two groups. After obtaining our data, we performed a chi-square test using the observed and expected values, yielding a p-value of 0.53.
  * My null hypothesis stated that there is no association between the promotional condition and the distribution of Individual IDs, while the alternative hypothesis suggested otherwise. With a p-value greater than 0.05, indicating no statistical significance, we concluded that the distribution of individuals was successful at an alpha = 0.05, affirming the validity of the random assignment and accepting the null hypothesis.
    
* We proceeded to examine the click-through rates (CTR) for each promotion to determine if they were independent of the promotion shown. By creating a pivot table and calculating the CTR, we found that Promotion A had a CTR of 2.22%, while Promotion B had a CTR of 3.02%. To assess if these rates were statistically equal, we compared the observed values of clicks and non-clicks with the expected values and conducted a chi-square test, resulting in a p-value of 0.00000008.
  * The null hypothesis posited that there is no association between the promotional condition and the click-through rates for each promotion, while the alternative hypothesis suggested otherwise. With a p-value less than 0.05, indicating statistical significance, we concluded that the click-through rate is dependent on the promotion shown at an alpha level of 0.05, thereby rejecting the null hypothesis and accepting the alternate hypothesis.

* I decided to further explore click-through rates (CTR) by analyzing activity during lunch and dinner times. Using a pivot table, I examined the sum of clicks for each promotion during their respective meal periods. For Promotion A, the lunchtime CTR was 1.91%, significantly higher than the 0.31% observed during dinner hours, suggesting that individuals predominantly utilized this promotion during lunch. On the other hand, Promotion B exhibited a lunchtime CTR of 1.55% and a dinner CTR of 1.47%, indicating a relatively even distribution of utilization throughout the day.
* 
