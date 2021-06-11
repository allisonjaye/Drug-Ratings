# Pharmacutical Drug Online Ratings
## Overview
I wanted to take a look at the user ratings of brand-name drugs versus their generic counterpart. This could be used to help identify if getting the brand name version is worth the extra money or from a pharmacutical company perspective, how well their brand is doing compared to the other brands and the generic.

All of this information is from the Drug Review Dataset which publicly available on the UCI Machine Learning Repository website. The data was taken from Drugs.com, an online pharmacutical website that allows it's users to rate the medication they have taken.

## The Data
There are 215,063 reviews in the dataset. Each review includes drug name, condition it was given to treat, a written review, a rating out of 10, the date and a count of other users who found the review helpful. I seperated the data by condition and took a look at the top 5 conditions that were reviewed. The most reviewed condition was birth control. I then broke it down more and looked at which drugs were reviewed most out of the birth control category.

Top 5 Conditions Reviewed:

<img src="https://github.com/allisonjaye/Drug-Ratings/blob/main/Images/TopConditions.jpg" width="720" height="432">

Top 5 Drugs Reviewed in Top Condition:

<img src="https://github.com/allisonjaye/Drug-Ratings/blob/main/Images/TopBCDrugs.jpg" width="720" height="432">

## Hypothesis
My null hypothesis is that there is no difference in the average ratings of generic vs brand named drugs.

H0: µ(Brand) = µ(Generic)

My alternate hypothesis is that the average ratings of the generic version versus the brand names is different.

H1: µ(Brand) != µ(Generic)

## Analysis
Etonogestrel was the most reviewed drug in the birth control category. Implanon and Nexplanon are brand named verisons of Etonogestrel so I decided to use them to run my tests. There is also a drug called NuvaRing which is another brand name of the same medication so I included that as well. From my initial look, all 4 of the medications were rated very similarly on average, around 5.6-6.6 out of 10.

Average Ratings of Generic (Etonogestrel) vs Brand Names:
<img src="https://github.com/allisonjaye/Drug-Ratings/blob/main/Images/GenericVBrand.jpg" width="720" height="432">

I then ran 3 different t-tests at a significance level of 0.05. The first test was comparing the average rating of the generic drug, Etonogestrel, to the first brand-name, Implanon. The second was comparing the generic to the next brand name, Nexplanon and the third comparing the generic to the last brand name, NuvaRing. To account for the number of comparisions, I used the Bonferroni Correction which changed my significance level to 0.016.

## Results
Two out of the three brand name drugs did reject the null hypothesis, meaning I can not say with statisical significance that their means are from the same distribution. Because one of the three failed to reject the null hypothesis, I can not fully reject it. My results are inconclusive.
