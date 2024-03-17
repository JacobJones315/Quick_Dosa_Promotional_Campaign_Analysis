# Analyzing Quick Dosa's Promotional Campaign Effectiveness through A/B Testing and Chi-Square Analysis

## Background
* Quick Dosa in our scenario is a pioneering fast-food chain specializing in vegetarian South Indian cuisine. Quick dosa rapidly expanded to 163 franchised restaurants across major cities within two years of its launch. Despite its success, overcrowding issues in dine-in spaces began to impede growth. To address this, Quick Dosa aimed to boost its takeout business by launching a promotional campaign through digital display ads. The campaign offered two options: Promotion A - a complimentary soft drink with takeout orders over $7.50, and Promotion B - a 5% discount on orders over $7.50. To determine the more effective promotion, an A-B test was conducted over one week to determine which propmotion strategy was best.

## Testing Strategy
* During the test week, Quick Dosa targeted individuals in Buffalo, NY through display ads on food-themed websites. Each individual was randomly assigned to either group A or group B, with group A exposed to Promotion A ads and group B to Promotion B ads. Clicking on the ad directed individuals to a landing page on Quick Dosa's website to place a takeout order, with the promotion automatically applied. All clicks resulted in orders, but a 4% cart abandonment rate occurred post-order registration due to credit card issues.

## Test Week Results
* At the end of the test week, Promotion A ads were served 24,963 times, while Promotion B ads were served 25,102 times. The dataset accompanying this case includes 50,065 rows of data, each corresponding to an ad impression. The columns in the dataset are as follows:
* Column A: Anonymized Individual ID
* Column B: Promotion (A or B)
* Column C: Clicked (1) or not (0)
* Column D: Takeout order amount ($) - available only for those who clicked, recorded before any promotional discount or cart abandonment.
* Column E: Indicator for whether the order was for lunch (1) or dinner (0), with a cutoff time of 3 pm to classify orders based on the time the ad was shown to the consumer
