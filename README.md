# Age-of-Peak-Human-Strength

# Abstract

Commonly held beliefs suggest that there exists a pinnacle age for athletic prowess, a peak of strength, beyond which continuous improvement wanes. As biological organisms, humans inevitably face a period of decline as age advances. This study delves into the question of when humans reach their peak strength. Is it in their early 20s, mid-20s, or perhaps early 30s?

In this analysis, strength is quantified across four key metrics: the maximum squat, bench press, deadlift, and a composite measure of these lifts (total). Our dataset encompasses all Internaltional Powerlifting Federation (IPF) affiliated events post-2019-01-01. The IPF is the governing body of powerlifting, recognized by the IOC and GAISF. The IPF has a strict anti-doping policy, adhering to the World Anti-Doping Agency (WADA) code. The IPF has an extensive competition calendar, featuring World Championships, European Championships, and other international events. I am utilizing the International Powerlifting Federation (IPF) dataset in my study on peak age of strength because it represents the premier strength achievements of drug-tested human populations, providing a reliable and standardized measure of human strength capacity. Furthermore, the IPF's stringent judging standards, including rigorous referee certification criteria (e.g., requiring referees to have a minimum of 2 years of experience and pass a written exam), ensure that the data reflects the highest level of technical proficiency and accuracy.

Admittedly, inherent biases require acknowledgment, notably the exclusivity of data derived solely from competitive lifters. Undoubtedly, there are gaps in our understanding of human performance and strength measures among non-competitive individuals. However, given the burgeoning popularity of Powerlifting and its diverse following across age, socioeconomic strata, and geographic locations, our focus on the competitive lifter demographic offers a robust representation of those who approach gym-going with a dedicated regimen. Ultimately, our inquiry is centered on the attainment of peak strength, and the average gym-goer who abstains from competition falls outside the scope of our analysis.

The data used for this report was from OpenPowerlifting and was last extracted on March 6, 2025. This page uses data from the OpenPowerlifting project, https://www.openpowerlifting.org.  You may download a copy of the data at https://data.openpowerlifting.org. 
Source: https://openpowerlifting.gitlab.io/opl-csv/files/openipf-latest.zip

# Conclusions

- For males, the peak strength age is around 36-37 years old, while for females, it's around 34-36 years old, depending on the lift (total, squat, bench, or deadlift).
- The LateOpen Age Group (35-40 years old) performs best among males, with the highest mean totals, squats, benches, and deadlifts. For females, the Open Age Group (28-35 years old) performs best in terms of mean totals, squats, and deadlifts.
- Females tend to reach peak strength at an older age than males, with significant differences in mean age across all weight groups for totals, squats, and deadlifts.

# Table of Contents

Please refer to the following table of contents to navigate your exploration:

- Data Preparation and Cleaning: Reproducible steps for transforming raw data.
- Hypothesis Testing: Statistical analyses of the top drug-tested lifters.
- Predictive Analytics: Application of General Linear Models (GLMs) and XGBoost models to predict the age of a lifter.

# Core Statistical Testing Results
Please see Data Preparation and Cleaning for more detail regarding Age and Weight Groups.

Age Groups:
- (0-19): Teen
- (19-23): Junior
- (23-28): EarlyOpen
- (28-35): Open
- (35-40): LateOpen
- (40-45): EarlyMaster
- (45-55): Master
- (55+): Elder

Top lifters are defined as the top 90th percentile of weights lifted for each Weight Group. All alpha for statistical significance was set to .05.

**MALE**
-	The 90th percentile strength cutoff for each measure of strength within each Age Group appear to be normally distributed.
-	The mean total of the top lifers appear to be significantly different across the Age Groups.
-	The LateOpen Age Group has the largest mean total for top lifters at 753 kg.
    - There were significant differences, using the adjusted p-values, against the EarlyOpen, Open, and EarlyMaster Age Groups.
-	The LateOpen Age Group has the largest mean squat for top lifters at 278 kg.
    - The same pair-wise conclusion of the total holds for squats.
-	The LateOpen Age Group has the largest mean bench for top lifters at 183 kg.
    - There were significant differences, using the adjusted p-values, against the Junior, EarlyOpen, Open, and EarlyMaster Age Groups.
-	The LateOpen Age Group has the largest mean deadlift for top lifters at 301 kg.
    - This is significantly higher than all other Age Groups’ mean deadlift other than EarlyMaster’s, which had a mean deadlift for top lifters of 294 kg.
-	A 3rd Degree Polynomial Model Orthogonal Distance Regression showed the following peak age for mean weights lifted:
    - Total: 36.5 years old (86% R2)
    - Squat: 35.5 years old (83% R2)
    - Bench: 37.5 years old (86% R2)
    - Deadlift: 35.5 years old (83% R2)
 
**FEMALE**

-	The 90th percentile strength cutoff for each measure of strength within each Age Group appear to be normally distributed.
-	The mean total of the top lifers appear to be significantly different across the Age Groups.
-	The Open Age Group has the largest mean total for top lifters at 450 kg.
    - There was a significant difference, using the adjusted p-values, only against the EarlyOpen Age Group.
-	The Open Age Group has the largest mean squat for top lifters at 168 kg.
    - There were significant differences, using the adjusted p-values, against the EarlyOpen and Master Age Groups.
-	The Master Age Group has the largest mean bench for top lifters at 99 kg.
    - There were significant differences, using the adjusted p-values, against the Junior, EarlyOpen, and Open Age Groups.
-	The Open Age Group has the largest mean deadlift for top lifters at 190 kg.
    - There were significant differences, using the adjusted p-values, against the EarlyOpen and LateOpen Age Groups.
-	A 3rd Degree Polynomial Model Orthogonal Distance Regression showed the following peak age for mean weights lifted:
    - Total: 34.5 years old (86% R2)
    - Squat: 34 years old (90% R2)
    - Bench: 36 years old (90% R2)
    - Deadlift: 36.5 years old (85% R2)


**CROSS-SEX**

-	For the top totals, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was 1.25 years in the Heavy Weight Group.
-	For the top squats, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was .06 years in the SuperHeavy Weight Group (not significant.
-	For the top benches, the Middle and Light Weight Groups did not have a significant difference in mean ages across sexes. For the Heavy and Super Heavy Weight Groups, there was not a significant difference.
-	For the top deadlifts, across all Weight Groups, females had a significantly higher mean age compared to males. The smallest delta was 2.08 years in the Heavy Weight Group.

# Machine Learning Results

**Continuous Age Prediction**

-	These models take the full population of events and predicts the age of the lifter.
-	The inputs are the following:
    - Sex, Bodyweight (KG), Squat, Bench, Deadlift, Total

Linear Regression:
(train, val, test):
-	RMSE: 11.26, 11.31, 11.28
-	R2: .07, .06, .07
-	CV-RMSE: 11.26

Polynomial Regression (n = 3):
(train, val, test):
-	RMSE: 11.07, 11.14, 11.08
-	R2: .1, .09, .1
-	CV-RMSE: 11.09

XGBoost (n_estimators = 100, early_stopping = 3, max_depth = 2:
(train, val, test):
-	RMSE: 10.97, 11.05, 11.00
-	R2: .11, .11, .11

This study demonstrates the potential of using machine learning models to predict age based on sex, bodyweight, and strength metrics. The XGBoost model achieved an RMSE of 11.00, indicating a moderate level of accuracy. While this may seem modest, it's essential to consider the complexity of human development and the multiple factors that influence age-related changes. The model's performance highlights the value of using data-driven approaches to understand the relationships between age, sex, bodyweight, and strength. However, it's crucial to acknowledge that this model only scratches the surface, as it doesn't account for a multitude of factors that can impact athletic performance, such as training experience, years of competition, nationality, socioeconomic status, access to coaching and resources, and even factors like travel and weight cutting for specific competitions.

**AgeGroup Prediction**

-	This model takes the full population of events and predicts the AgeGroup (8 classes) of the lifter.
-	The inputs are the following:
    - Sex, Bodyweight (KG), Squat, Bench, Deadlift, Total

XGBoost (n_estimators = 100, early_stopping = 3, max_depth = 2:
(train, val, test):
-	Accuracy: .33, .33, .33
-	Log loss: 1.7, 1.72, 1.71
-	ROC_AUC: .69, .68, .69


This XGBoost model predicts AgeGroup (8 classes) with an accuracy of 0.33, demonstrating a notable ability to capture the relationships between age, sex, bodyweight, and strength. The model's performance is impressive, considering the complexity of human development and the multiple factors that influence age-related changes. The results highlight the importance of considering multiple factors when trying to understand human development and performance, and demonstrate the value of using data-driven approaches to uncover meaningful patterns and relationships. However, it's essential to recognize that this model provides a limited snapshot of the complex interplay between biological, environmental, and socioeconomic factors that shape athletic performance. Factors like training history, competition experience, access to resources, and even lifestyle choices like nutrition and recovery strategies are not accounted for in this model, emphasizing the need for more comprehensive and nuanced approaches to understanding human performance.
