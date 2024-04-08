# Age-of-Peak-Human-Strength

# Abstract

Commonly held beliefs suggest that there exists a pinnacle age for athletic prowess, a zenith of strength, beyond which continuous improvement wanes. As biological organisms, humans inevitably face a period of decline as age advances. This study delves into the question of when humans reach their peak strength. Is it in their early 20s, mid-20s, or perhaps early 30s? The revelations from our findings may defy conventional expectations.

In this comprehensive analysis, strength is quantified across four key metrics: the maximum squat, bench press, deadlift, and a composite measure of these lifts. Our dataset encompasses all powerlifting events post-2018-01-01. Admittedly, inherent biases require acknowledgment, notably the exclusivity of data derived solely from competitive lifters. Undoubtedly, there are gaps in our understanding of human performance and strength measures among non-competitive individuals. However, given the burgeoning popularity of Powerlifting and its diverse following across age, socioeconomic strata, and geographic locations, our focus on the competitive lifter demographic offers a robust representation of those who approach gym-going with a dedicated regimen. Ultimately, our inquiry is centered on the attainment of peak strength, and the average gym-goer who abstains from competition falls outside the scope of our analysis.

This study adopts a tripartite lens, examining sub-populations within the realm of competitive Powerlifting. These subgroups consist of the top performers subject to drug testing, the top non-drug tested athletes, and a broader category termed the "general population" of lifters. While the delineation of the first two groups is straightforward, the designation of the general population warrants disclosure of an inherent bias. Our methodology entails selecting lifters falling within the interquartile range (25% to 75%) of each drug-tested weight group to compose this general population cohort. Consequently, individuals who commence their competitive journey in this group, likely younger and less experienced, may outgrow this general population status over time, progressing to surpass the 75th percentile threshold. Consequently, the data within the general population subset may skew towards a younger age for the purported "peak" performance.

The data used for this report was from OpenPowerlifting and was last pulled on March 19, 2024. This page uses data from the OpenPowerlifting project, https://www.openpowerlifting.org.  You may download a copy of the data at https://data.openpowerlifting.org. 

# Table of Contents

Please refer to the following table of contents to navigate your exploration:

- Data Preparation and Cleaning: Reproducible steps for transforming raw data.
- Drug Tested: Analysis of drug-tested lifters exclusively.
- Non-Drug Tested: Examination of lifters who have not undergone drug testing.
- General Population: Assessment of lifters falling within the 25th to 75th percentile strength range and subject to drug testing.
- Peak Age for Human Strength Summary: Summary of findings regarding peak age across the three sub-populations.
- Predictive Analytics: Application of Linear Regression and Random Forest Regression models.

# Core Statistical Testing Results
Please see Data Preparation and Cleaning for more detail regarding Age and Weight Groups.

Age Groups:
-	(0-15): Teen
-	(15-20): Junior
-	(20-25): EarlyOpen
-	(25-30): Open
-	(30-35): LateOpen
-	(35-45): EarlyMaster
-	(45-55): Master
-	(55+): Elder

Top lifters are defined as the top 90th percentile of weights lifted for each Weight Group. All alpha for statistical significance was set to .05.

**MALE**

Drug Tested Population:
-	The 90th percentile strength cutoff for each measure of strength within each Age Group appear to be normally distributed.
-	The LateOpen Age Group has the largest mean total for top lifters at 730.58 kg.
    - This is significantly higher than all other Age Groups’ mean total other than EarlyMaster’s, which had a mean total for top lifters of 727.52 kg.
-	The EarlyMaster Age Group has the largest mean squat for top lifters at 269.86 kg.
    - This is significantly higher than all other Age Groups’ mean squat other than LateOpen’s, which had a mean squat for top lifters of 269.19 kg.
-	The EarlyMaster Age Group has the largest mean bench for top lifters at 188.96 kg.
    - This is significantly higher than all other Age Groups’ bench.
-	The LateOpen Age Group has the largest mean deadlift for top lifters at 295.45 kg.
    - This is significantly higher than all other Age Groups’ mean deadlift other than EarlyMaster’s, which had a mean deadlift for top lifters of 294.37 kg.
-	Using the metric of largest mean weight lifted in top lifts, the LateOpen and EarlyMaster Age Groups are a clear indication of a potential peak in strength.
-	A 3rd Degree Polynomial Model Orthogonal Distance Regression on all lifters showed the following peak age for mean weights lifted:
    - Total: 36 years old (91% R2)
    - Squat: 35 years old (90.85% R2)
    - Bench: 39 years old (93.11% R2)
    - Deadlift: 36.5 years old (89.18% R2)

Non Drug Tested Population:
-	The 90th percentile strength cutoff for each measure of strength except deadlift within each Age Group appear to be normally distributed.
-	The LateOpen Age Group has the largest mean total for top lifters at 778.31 kg.
    - This is significantly higher than all other Age Groups’ mean total other than EarlyMaster’s, which had a mean total for top lifters of 776.82 kg.
-	The LateOpen Age Group has the largest mean squat for top lifters at 288.95 kg.
    - This is significantly higher than all other Age Groups’ mean squat other than EarlyMaster’s, which had a mean squat for top lifters of 287.58 kg.
-	The EarlyMaster Age Group has the largest mean bench for top lifters at 209.14 kg.
    - This is significantly higher than all other Age Groups’ bench.
-	The LateOpen Age Group has the largest mean deadlift for top lifters at 315.18 kg.
    - This is significantly higher than all other Age Groups’ mean deadlift other than EarlyMaster’s, which had a mean deadlift for top lifters of 314.07 kg.
-	Using the metric of largest mean weight lifted in top lifts, the LateOpen and EarlyMaster Age Groups are a clear indication of a potential peak in strength.
-	A 3rd Degree Polynomial Model Orthogonal Distance Regression on all lifters showed the following peak age for mean weights lifted:
    - Total: 36 years old (82.14% R2)
    - Squat: 35.5 years old (80.56% R2)
    - Bench: 40 years old (93.27% R2)
    - Deadlift: 37.5 years old (87.37% R2)

General Population:
-	The 90th percentile strength cutoff for each measure of strength except deadlift within each Age Group appear to be normally distributed.
-	The EarlyMaster Age Group has the largest mean total for top lifters at 591.71 kg.
    - This is significantly higher than all other Age Groups’ mean total.
-	The EarlyMaster Age Group has the largest mean squat for top lifters at 213.45 kg.
    - This is significantly higher than all other Age Groups’ mean squat other than Master’s, which had a mean squat for top lifters of 211.84 kg.
-	The EarlyMaster Age Group has the largest mean bench for top lifters at 144.89 kg.
    - This is significantly higher than all other Age Groups’ mean bench other than Master’s, which had a mean bench for top lifters of 144.62 kg.
-	The EarlyMaster Age Group has the largest mean deadlift for top lifters at 238.37 kg.
    - This is significantly higher than all other Age Groups’ mean deadlift.
-	Using the metric of largest mean weight lifted in top lifts, the EarlyMaster and Master Age Groups are a clear indication of a potential peak in strength.
-	A 3rd Degree Polynomial Model Orthogonal Distance Regression on all lifters showed the following peak age for mean weights lifted:
    - Total: 37.5 years old (88.39% R2)
    - Squat: 38 years old (86.51% R2)
    - Bench: 39 years old (91.3% R2)
    - Deadlift: 37.5 years old (86.56% R2)
 
**FEMALE**

Drug Tested Population:
-	The 90th percentile strength cutoff for squat and bench within each Age Group appear to be normally distributed, total and deadlift do not.
-	The Master Age Group has the largest mean total lifted for top lifters at 438.40 kg.
    - This is significantly higher than the EarlyOpen’s (427.91 kg), Junior’s (429.71 kg), and Elder’s (406.57 kg) mean top total. 
    - The other Age Groups’ mean total were not significantly different than the mean total lifted for top lifters in the Masters.
-	The EarlyMaster Age Group has the largest mean squat for top lifters at 164.11 kg.
    - This is significantly higher than the EarlyOpen’s (159.27 kg), Junior’s (161.32 kg), and Elder’s (152.2 kg) mean top squat. 
    - The other Age Groups’ mean squat were not significantly different than the mean squat for top lifters in the EarlyMasters.
-	The Master Age Group has the largest mean bench for top lifters at 100.4 kg.
    - This is significantly higher than all other Age Groups’ bench.
-	The Open Age Group has the largest mean deadlift for top lifters at 185.83 kg.
    - This is significantly higher than the EarlyOpen’s (181.85 kg), Junior’s (181.25 kg), Teen’s (160.6 kg), and Elder’s (178.6 kg) mean top deadlift. The other Age Groups’ mean deadlift were not significantly different than the mean deadlift for top lifters in the Open.
-	Using the metric of largest mean weight lifted in top lifts, the EarlyMaster and Master Age Groups could be a potential peak in strength.
-	A 3rd Degree Polynomial Model Orthogonal Distance Regression on all lifters showed the following peak age for mean weights lifted:
    - Total: 35.5 years old (88.37% R2)
    - Squat: 34 years old (90.56% R2)
    - Bench: 36.5 years old (93.06% R2)
    - Deadlift: 37.5 years old (86.4% R2)

Non Drug Tested Population:
-	The 90th percentile strength cutoff for each measure of strength except deadlift within each Age Group appear to be normally distributed.
-	The EarlyMaster Age Group has the largest mean total lifted for top lifters at 466.86 kg.
    - This is significantly higher than all other Age Groups’ mean total other than LateOpen’s (461.82 kg) and Elder’s (459.67 kg) mean total for top lifters.
    - Note: Elder has 57 samples.
-	The EarlyMaster Age Group has the largest mean squat for top lifters at 173.13 kg.
    - This is significantly higher than all other Age Groups’ mean squat other than LateOpen’s (170.93 kg) and Elder’s mean squat for top lifters.
    - Note: Elder has 52 samples.
-	The EarlyMaster Age Group has the largest mean bench for top lifters at 108.6 kg.
    - This is significantly higher than all other Age Groups’ mean bench other than Master’s, which had a mean bench for top lifters of 287.58 kg.
-	The EarlyMaster Age Group has the largest mean deadlift for top lifters at 196.80 kg.
    - This is significantly higher than all other Age Groups’ mean deadlift other than Mater’s (194.36 kg) and Elder’s mean deadlift for top lifters.
    - Note: Elder has 103 samples.
-	Using the metric of largest mean weight lifted in top lifts, the LateOpen and EarlyMaster Age Groups are a clear indication of a potential peak in strength.
-	Using the metric of largest mean weight lifted in top lifts, the EarlyMaster and Master Age Groups could be a potential peak in strength.
-	A 3rd Degree Polynomial Model Orthogonal Distance Regression on all lifters showed the following peak age for mean weights lifted:
    - Total: 35 years old (73.52% R2)
    - Squat: 35.5 years old (80.63% R2)
    - Bench: 39 years old (82.84% R2)
    - Deadlift: 38 years old (87.58% R2)

General Population:
-	The 90th percentile strength cutoff for squat and bench within each Age Group appear to be normally distributed.
    - Total and deadlift within each Age Group do not appear to be normally distributed.
-	The Junior Age Group has the largest mean total lifted for top lifters at 472.25 kg.
    - This is only significantly higher than EarlyOpen’s (457.68 kg) mean total for top lifters.
-	The Junior Age Group has the largest mean squat for top lifters at 174.52 kg.
    - This is only significantly higher than EarlyOpen’s (169.77 kg) mean squat for top lifters.
-	The Master Age Group has the largest mean bench for top lifters at 113.24 kg.
    - This is significantly higher than all other Age Groups’ mean bench.
-	The EarlyMaster Age Group has the largest mean deadlift for top lifters at 195.61 kg.
    - This is only significantly higher than EarlyOpen’s (190.92 kg) and Juniors’ (192.37 kg) mean deadlift for top lifters.
-	Using the metric of largest mean weight lifted in top lifts, there is no clear Age Group for peak in strength.
-	A 3rd Degree Polynomial Model Orthogonal Distance Regression on all lifters showed the following peak age for mean weights lifted:
    - Total: 33 years old (27.36% R2)
    - Squat: 32 years old (67.61% R2)
    - Bench: 37.5 years old (69.97% R2)
    - Deadlift: 35.5 years old (67.17% R2)


# Cross-Sex Findings

Drug Tested Population:
-	For the top totals, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was 1.35 years in the Heavy Weight Group.
-	For the top squats, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was .96 years in the Heavy Weight Group.
-	For the top benches, the Middle and Light Weight Groups did not have a significant difference in mean ages across sexes. For the Heavy and Super Heavy Weight Groups, males had a higher mean age compared to females.
-	For the top deadlifts, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was 2.12 years in the Heavy Weight Group.

Non Drug Tested Population:
-	For the top totals, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was 2.8 years in the SuperHeavy Weight Group.
-	For the top squats, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was 2.56 years in the SuperHeavy Weight Group.
-	For the top benches, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was 1.54 years in the Middle Weight Group.
-	For the top deadlifts, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was 3.78 years in the Middle Weight Group.

General Population:
-	For the top totals, across all Weight Groups except SuperHeavy, females had a significantly higher mean age compared to males. The smallest delta was .74 years in the Heavy Weight Group.
    - The mean age for males (29.97) in top SuperHeavy totals significantly higher than the mean age for females (29.11) in top SuperHeavy totals.
-	For the top squats, across all Weight Groups except SuperHeavy, females had a significantly higher mean age compared to males. The smallest delta was .48 years in the Heavy Weight Group.
    - The mean age for males (29.81) in top SuperHeavy totals significantly higher than the mean age for female (28.05) in top SuperHeavy squats.
-	For the top benches, females had a significanly higher mean age in the Light Weight Group (2.64 delta) and males had a significantly higher mean age in the SuperHeavy Weight Group (1.36 delta). No other Weight Groups had a significant difference.
-	For the top deadlifts, across all Weight Groups except SuperHeavy, females had a significantly higher mean age compared to males. 
    - The smallest delta was .21 years in the SuperHeavy Weight Group.

# Interesting Notes

- Within both the Drug Tested and General Population categories, females exhibited greater variation in the Age Group with the highest mean weight lifted among top lifters compared to males.
- For General Population males, a peak age of 38 for squats was observed using a 3rd Degree Polynomial Model via Orthogonal Distance Regression.
- Across all metrics and methodologies, the peak age for maximal bench press strength appears to be at least 35 years old, with the peak age nearing 38 years old.
- Notably, females across most measures of strength and population characteristics seemed to peak at a significantly older age than males, with the disparity widening among non-drug tested lifters and narrowing within the general population.

# Machine Learning Results

**General Model**

-	This model takes the full population of lifters and predicts the total weight lifted across the four measures of strength.
-	The inputs are the following:
    - ex, Drug Tested, Age, and Weight

Linear Regression:
Total:
-	RMSE: 92.68 kg, 19.9%
-	MAE: 71.17 kg, 15.28%
-	R2: 64.69%

Squat:
-	RMSE: 37.20 kg, 22.36%
-	MAE: 28.46 kg, 17.11%
-	R2: 59.14%

Bench:
-	RMSE: 27.12 kg, 24.24%
-	MAE: 20.81 kg, 18.6%
-	R2: 64.83%

Deadlift:
-	RMSE: 38.84 kg, 20.12%
-	MAE: 29.76 kg, 15.42%
-	R2: 58.56%

The robust R2 scores observed across all measures of strength suggest a strong linear correlation between the four features and expected strength performance. This outcome aligns with our expectations, as both the statistical testing and regression fitting thoroughly examined the relationship between these features and strength performance.

Random Forest:
Total:
-	RMSE: 83.68 kg, 17.97%
-	MAE: 63.50 kg, 13.64%
-	R2: 71.05%

Squat:
-	RMSE: 34.47 kg, 20.78%
-	MAE: 26.21 kg, 15.76%
-	R2: 64.72%

Bench:
-	RMSE: 24.46 kg, 21.86%
-	MAE: 18.23 kg, 16.29%
-	R2: 71.40%

Deadlift:
-	RMSE: 35.03 kg, 18.15%
-	MAE: 26.48 kg, 13.72%
-	R2: 66.29%



**10th Percentile Model**

-	This model takes only the 10th percentile of lifters, per Weight Group, and predicts the total weight lifted across the four measures of strength.
-	The inputs are the following:
    - Sex, Drug Tested, Age, and Weight

Linear Regression:
Total:
-	RMSE: 50.60 kg, 8.14%
-	MAE: 38.02 kg, 6.11%
-	R2: 89.66%

Squat:
-	RMSE: 20.69 kg, 8.99%
-	MAE: 15.33 kg, 6.66%
-	R2: 87.62%

Bench:
-	RMSE: 17.16 kg, 10.82%
-	MAE: 12.82 kg, 8.1%
-	R2: 87.56%

Deadlift:
-	RMSE: 20.15 kg, 7.87%
-	MAE: 14.94 kg, 5.84%
-	R2: 88.70%

The exceptionally high R2 scores and minimal margin of errors observed across all strength measures signify a robust correlation between the four features and expected strength performance. The superior performance compared to the general model underscores the potency of these features—age, weight, drug testing status, and sex—as strong indicators for performance at the elite level of strength.

Random Forest:
Total:
-	RMSE: 40.58 kg, 6.53%
-	MAE: 30.07 kg, 4.84%
-	R2: 93.35%

Squat:
-	RMSE: 17.12 kg, 7.44%
-	MAE: 12.30 kg, 5.34%
-	R2: 91.53%

Bench:
-	RMSE: 13.70 kg, 8.64%
-	MAE: 9.77 kg, 6.17%
-	R2: 92.10%

Deadlift:
-	RMSE: 17.02 kg, 6.65%
-	MAE: 12.20 kg, 4.77%
-	R2: 91.94%
