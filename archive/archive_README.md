# Age-of-Peak-Human-Strength

# Abstract

Commonly held beliefs suggest that there exists a pinnacle age for athletic prowess, a zenith of strength, beyond which continuous improvement wanes. As biological organisms, humans inevitably face a period of decline as age advances. This study delves into the question of when humans reach their peak strength. Is it in their early 20s, mid-20s, or perhaps early 30s? The revelations from our findings may defy conventional expectations.

In this comprehensive analysis, strength is quantified across four key metrics: the maximum squat, bench press, deadlift, and a composite measure of these lifts. Our dataset encompasses all powerlifting events post-2018-01-01. Admittedly, inherent biases require acknowledgment, notably the exclusivity of data derived solely from competitive lifters. Undoubtedly, there are gaps in our understanding of human performance and strength measures among non-competitive individuals. However, given the burgeoning popularity of Powerlifting and its diverse following across age, socioeconomic strata, and geographic locations, our focus on the competitive lifter demographic offers a robust representation of those who approach gym-going with a dedicated regimen. Ultimately, our inquiry is centered on the attainment of peak strength, and the average gym-goer who abstains from competition falls outside the scope of our analysis.

This study adopts a tripartite lens, examining sub-populations within the realm of competitive Powerlifting. These subgroups consist of the top performers subject to drug testing, the top non-drug tested athletes, and a broader category termed the "general population" of lifters. While the delineation of the first two groups is straightforward, the designation of the general population warrants disclosure of an inherent bias. Our methodology entails selecting lifters falling within the interquartile range (25% to 75%) of each drug-tested weight group to compose this general population cohort. Consequently, individuals who commence their competitive journey in this group, likely younger and less experienced, may outgrow this general population status over time, progressing to surpass the 75th percentile threshold. Consequently, the data within the general population subset may skew towards a younger age for the purported "peak" performance.

The data used for this report was from OpenPowerlifting and was last extracted on April 5, 2024. This page uses data from the OpenPowerlifting project, https://www.openpowerlifting.org.  You may download a copy of the data at https://data.openpowerlifting.org. 

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
-	The LateOpen Age Group has the largest mean total for top lifters at 731.65 kg.
    - This is significantly higher than all other Age Groups’ mean total other than EarlyMaster’s, which had a mean total for top lifters of 729.47 kg.
-	The EarlyMaster Age Group has the largest mean squat for top lifters at 270.21kg.
    - This is significantly higher than all other Age Groups’ mean squat other than LateOpen’s, which had a mean squat for top lifters of 269.44 kg.
-	The EarlyMaster Age Group has the largest mean bench for top lifters at 188.9 kg.
    - This is significantly higher than all other Age Groups’ bench.
-	The LateOpen Age Group has the largest mean deadlift for top lifters at 295.86 kg.
    - This is significantly higher than all other Age Groups’ mean deadlift other than EarlyMaster’s, which had a mean deadlift for top lifters of 294.85 kg.
-	Using the metric of largest mean weight lifted in top lifts, the LateOpen and EarlyMaster Age Groups are a clear indication of a potential peak in strength.
-	A 3rd Degree Polynomial Model Orthogonal Distance Regression on all lifters showed the following peak age for mean weights lifted:
    - Total: 36 years old (90.9% R2)
    - Squat: 35 years old (90.85% R2)
    - Bench: 39 years old (93.1% R2)
    - Deadlift: 36.5 years old (86.39% R2)

Non Drug Tested Population:
-	The 90th percentile strength cutoff for each measure of strength except deadlift within each Age Group appear to be normally distributed.
-	The LateOpen Age Group has the largest mean total for top lifters at 779.68 kg.
    - This is significantly higher than all other Age Groups’ mean total other than EarlyMaster’s, which had a mean total for top lifters of 778.38 kg.
-	The LateOpen Age Group has the largest mean squat for top lifters at 289.07 kg.
    - This is significantly higher than all other Age Groups’ mean squat other than EarlyMaster’s, which had a mean squat for top lifters of 288.09 kg.
-	The EarlyMaster Age Group has the largest mean bench for top lifters at 209.07 kg.
    - This is significantly higher than all other Age Groups’ bench.
-	The LateOpen Age Group has the largest mean deadlift for top lifters at 314.95 kg.
    - This is significantly higher than all other Age Groups’ mean deadlift other than EarlyMaster’s, which had a mean deadlift for top lifters of 313.57 kg.
-	Using the metric of largest mean weight lifted in top lifts, the LateOpen and EarlyMaster Age Groups are a clear indication of a potential peak in strength.
-	A 3rd Degree Polynomial Model Orthogonal Distance Regression on all lifters showed the following peak age for mean weights lifted:
    - Total: 33.5 years old (72.99% R2)
    - Squat: 35 years old (83.97% R2)
    - Bench: 40 years old (93.17% R2)
    - Deadlift: 37.5 years old (87.91% R2)

General Population:
-	The 90th percentile strength cutoff for each measure of strength except deadlift and total within each Age Group appear to be normally distributed.
-	The EarlyMaster Age Group has the largest mean total for top lifters at 591.92 kg.
    - This is significantly higher than all other Age Groups’ mean total.
-	The EarlyMaster Age Group has the largest mean squat for top lifters at 213.51 kg.
    - This is significantly higher than all other Age Groups’ mean squat other than Master’s, which had a mean squat for top lifters of 211.89 kg.
-	The EarlyMaster Age Group has the largest mean bench for top lifters at 144.91 kg.
    - This is significantly higher than all other Age Groups’ mean bench other than Master’s, which had a mean bench for top lifters of 144.63 kg.
-	The EarlyMaster Age Group has the largest mean deadlift for top lifters at 238.46 kg.
    - This is significantly higher than all other Age Groups’ mean deadlift.
-	Using the metric of largest mean weight lifted in top lifts, the EarlyMaster and Master Age Groups are a clear indication of a potential peak in strength.
-	A 3rd Degree Polynomial Model Orthogonal Distance Regression on all lifters showed the following peak age for mean weights lifted:
    - Total: 37 years old (87.79% R2)
    - Squat: 38 years old (86.13% R2)
    - Bench: 39 years old (91.1% R2)
    - Deadlift: 37.5 years old (86.03% R2)
 
**FEMALE**

Drug Tested Population:
-	The 90th percentile strength cutoff for each measure of strength except deadlift within each Age Group appear to be normally distributed.
-	The Master Age Group has the largest mean total lifted for top lifters at 439.63 kg.
    - This is significantly higher than the EarlyOpen’s (429.11 kg), Junior’s (429.93 kg), and Elder’s (406.66 kg) mean top total. 
    - The other Age Groups’ mean total were not significantly different than the mean total lifted for top lifters in the Masters.
-	The EarlyMaster Age Group has the largest mean squat for top lifters at 164.26 kg.
    - This is significantly higher than the EarlyOpen’s (159.51 kg), Junior’s (161.15 kg), and Elder’s (152.2 kg) mean top squat. 
    - The other Age Groups’ mean squat were not significantly different than the mean squat for top lifters in the EarlyMasters.
-	The Master Age Group has the largest mean bench for top lifters at 100.52 kg.
    - This is significantly higher than all other Age Groups’ bench.
-	The Open Age Group has the largest mean deadlift for top lifters at 186.01 kg.
    - This is significantly higher than the EarlyOpen’s (181.95 kg), Junior’s (181.10 kg), and Elder’s (178.96 kg) mean top deadlift. The other Age Groups’ mean deadlift were not significantly different than the mean deadlift for top lifters in the Open.
-	Using the metric of largest mean weight lifted in top lifts, the EarlyMaster and Master Age Groups could be a potential peak in strength.
-	A 3rd Degree Polynomial Model Orthogonal Distance Regression on all lifters showed the following peak age for mean weights lifted:
    - Total: 35.5 years old (88.19% R2)
    - Squat: 34 years old (90.37% R2)
    - Bench: 36.5 years old (93.04% R2)
    - Deadlift: 37.5 years old (89.09% R2)

Non Drug Tested Population:
-	The 90th percentile strength cutoff for each measure of strength except deadlift within each Age Group appear to be normally distributed.
-	The EarlyMaster Age Group has the largest mean total lifted for top lifters at 466.95 kg.
    - This is significantly higher than all other Age Groups’ mean total other than LateOpen’s (462.90 kg) and Elder’s (460.78 kg) mean total for top lifters.
    - Note: Elder has 59 samples.
-	The EarlyMaster Age Group has the largest mean squat for top lifters at 173.99 kg.
    - This is significantly higher than all other Age Groups’ mean squat other than LateOpen’s (172.25 kg) and Elder’s mean squat for top lifters.
    - Note: Elder has 53 samples.
-	The EarlyMaster Age Group has the largest mean bench for top lifters at 108.73 kg.
    - This is significantly higher than all other Age Groups’ mean bench other than Master’s, which had a mean bench for top lifters of 107.17 kg.
-	The EarlyMaster Age Group has the largest mean deadlift for top lifters at 197.14 kg.
    - This is significantly higher than all other Age Groups’ mean deadlift other than Mater’s (194.48 kg) and Elder’s mean deadlift for top lifters.
    - Note: Elder has 105 samples.
-	Using the metric of largest mean weight lifted in top lifts, the LateOpen and EarlyMaster Age Groups are a clear indication of a potential peak in strength.
-	Using the metric of largest mean weight lifted in top lifts, the EarlyMaster and Master Age Groups could be a potential peak in strength.
-	A 3rd Degree Polynomial Model Orthogonal Distance Regression on all lifters showed the following peak age for mean weights lifted:
    - Total: 35.5 years old (74.88% R2)
    - Squat: 35.5 years old (81.0% R2)
    - Bench: 39 years old (82.89% R2)
    - Deadlift: 38 years old (87.50% R2)

General Population:
-	The 90th percentile strength cutoff for each Age Group appear to be normally distributed.
-	The Junior Age Group has the largest mean total lifted for top lifters at 473.19 kg.
    - This is only significantly higher than EarlyOpen’s (459.25 kg) mean total for top lifters.
-	The Junior Age Group has the largest mean squat for top lifters at 174.75 kg.
    - This is only significantly higher than EarlyOpen’s (170.15 kg) mean squat for top lifters.
-	The Master Age Group has the largest mean bench for top lifters at 113.57 kg.
    - This is significantly higher than all other Age Groups’ mean bench.
-	The LateOpen Age Group has the largest mean deadlift for top lifters at 199.1 kg.
    - This is only significantly higher than EarlyOpen’s (191.26 kg) and Juniors’ (192.64 kg) mean deadlift for top lifters.
-	Using the metric of largest mean weight lifted in top lifts, there is no clear Age Group for peak in strength.
-	A 3rd Degree Polynomial Model Orthogonal Distance Regression on all lifters showed the following peak age for mean weights lifted:
    - Total: 33 years old (25.33% R2)
    - Squat: 32 years old (63.82% R2)
    - Bench: 37.5 years old (68.7% R2)
    - Deadlift: 37 years old (65.34% R2)


# Cross-Sex Findings

Drug Tested Population:
-	For the top totals, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was 1.31 years in the Heavy Weight Group.
-	For the top squats, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was .93 years in the Heavy Weight Group.
-	For the top benches, the Middle and Light Weight Groups did not have a significant difference in mean ages across sexes. For the Heavy and Super Heavy Weight Groups, males had a higher mean age compared to females.
-	For the top deadlifts, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was 2.09 years in the Heavy Weight Group.

Non Drug Tested Population:
-	For the top totals, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was 2.86 years in the SuperHeavy Weight Group.
-	For the top squats, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was 2.46 years in the SuperHeavy Weight Group.
-	For the top benches, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was 1.50 years in the Middle Weight Group.
-	For the top deadlifts, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was 3.77 years in the Middle Weight Group.

General Population:
-	For the top totals, across all Weight Groups except SuperHeavy, females had a significantly higher mean age compared to males. The smallest delta between females and males was .83 years in the Heavy Weight Group.
    - The mean age for males (29.97) with top SuperHeavy totals are significantly higher than the mean age for females (29.11) with top SuperHeavy totals.
-	For the top squats, across all Weight Groups except SuperHeavy, females had a significantly higher mean age compared to males. The smallest delta was .61 years in the Heavy Weight Group.
    - The mean age for males (29.8) with top SuperHeavy squats are significantly higher than the mean age for females (28.14) with top SuperHeavy squats.
-	For the top benches, females had a significanly higher mean age in the Light Weight Group (2.71 delta) and males had a significantly higher mean age in the SuperHeavy Weight Group (1.35 delta). No other Weight Groups had a significant difference.
-	For the top deadlifts, across all Weight Groups except SuperHeavy, females had a significantly higher mean age compared to males. 
    - The smallest delta was .04 years in the SuperHeavy Weight Group.

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
-	RMSE: 93.10 kg, 19.96%
-	MAE: 71.36 kg, 15.3%
-	R2: 64.15%
-	CV-RMSE: 93.24 kg

Squat:
-	RMSE: 37.20 kg, 22.32%
-	MAE: 28.45 kg, 17.1%
-	R2: 59.1%
-	CV-RMSE: 37.13 kg

Bench:
-	RMSE: 27.14 kg, 24.31%
-	MAE: 20.81 kg, 18.6%
-	R2: 64.5%
-	CV-RMSE: 27.1 kg

Deadlift:
-	RMSE: 38.99 kg, 20.16%
-	MAE: 29.87 kg, 15.44%
-	R2: 58.43%
-	CV-RMSE: 39 kg

The robust R2 scores observed across all measures of strength suggest a strong linear correlation between the four features and expected strength performance. This outcome aligns with our expectations, as both the statistical testing and regression fitting thoroughly examined the relationship between these features and strength performance.

Random Forest:
Total:
-	RMSE: 84.81 kg, 18.18%
-	MAE: 64.41 kg, 13.81%
-	R2: 70.25%
-	CV-RMSE: 85.61 kg

Squat:
-	RMSE: 34.86 kg, 20.92%
-	MAE: 26.41 kg, 15.85%
-	R2: 64.07%
-	CV-RMSE: 35.24 kg

Bench:
-	RMSE: 24.62 kg, 22.05%
-	MAE: 18.35 kg, 16.44%
-	R2: 70.8%
-	CV-RMSE: 24.84 kg

Deadlift:
-	RMSE: 35.32 kg, 18.26%
-	MAE: 26.7 kg, 13.8%
-	R2: 65.88%
-	CV-RMSE: 35.71 kg



**10th Percentile Model**

-	This model takes only the 10th percentile of lifters, per Weight Group, and predicts the total weight lifted across the four measures of strength.
-	The inputs are the following:
    - Sex, Drug Tested, Age, and Weight

Linear Regression:
Total:
-	RMSE: 50.03 kg, 8.0%
-	MAE: 37.55 kg, 6.0%
-	R2: 89.85%
-	CV-RMSE: 50.58 kg

Squat:
-	RMSE: 20.63 kg, 8.97%
-	MAE: 15.38 kg, 6.7%
-	R2: 87.78%
-	CV-RMSE: 20.47 kg

Bench:
-	RMSE: 17.18 kg, 10.84%
-	MAE: 12.88 kg, 8.12%
-	R2: 87.52%
-	CV-RMSE: 16.92 kg

Deadlift:
-	RMSE: 20.57 kg, 8.01%
-	MAE: 15.23 kg, 5.94%
-	R2: 88.06%
-	CV-RMSE: 20.4 kg

The exceptionally high R2 scores and minimal margin of errors observed across all strength measures signify a robust correlation between the four features and expected strength performance. The superior performance compared to the general model underscores the potency of these features—age, weight, drug testing status, and sex—as strong indicators for performance at the elite level of strength.

Random Forest:
Total:
-	RMSE: 41.59 kg, 6.66%
-	MAE: 30.61 kg, 4.9%
-	R2: 92.99%
-	CV-RMSE: 42.73 kg

Squat:
-	RMSE: 17.26 kg, 7.51%
-	MAE: 12.49 kg, 5.43%
-	R2: 91.44%
-	CV-RMSE: 17.54 kg

Bench:
-	RMSE: 13.79 kg, 8.7%
-	MAE: 9.88 kg, 6.23%
-	R2: 91.96%
-	CV-RMSE: 13.87 kg

Deadlift:
-	RMSE: 17.27 kg, 6.73%
-	MAE: 12.35 kg, 4.81%
-	R2: 91.58%
-	CV-RMSE: 17.45 kg
