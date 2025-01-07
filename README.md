# Health Monitoring and Analysis
 
## Overview

Traditional health monitoring systems often categorize patient health status using rigid, predefined thresholds that may not capture the nuanced variations across a diverse patient population. This can lead to oversimplified assessments and potentially overlook subtle yet critical patterns in health data. The challenge is to develop a more dynamic and responsive approach that utilizes unsupervised learning to identify natural groupings within health data, facilitating personalized and precise health management.

## Objectives

* **Identified Clusters:** Distinct patient groups based on health metrics, each with unique characteristics that provide insight into their specific health needs.
* **Personalized Health Insights:** Enhanced understanding of patient health requirements and risks, enabling tailored intervention strategies.
* **Improved Health Monitoring:** Recommendations for targeted monitoring and intervention strategies that cater to the specific needs of each cluster, leading to more effective health management and better patient outcomes.

## Exploratory Data Analysis (EDA) Performed:

### Distribution of Each Numerical Feature

<img width="371" alt="distribution_of_each_numerical_feature" src="https://github.com/user-attachments/assets/af551980-78f6-41ad-bf14-5b1568ae5b6c" />


### Gender Distribution and Correlation Matrix

<img width="987" alt="gender_distribution_and_correlation_matrix" src="https://github.com/user-attachments/assets/49ebb893-b5ee-4a40-a5b4-f8177a5ac07c" />


The pie chart indicates a nearly even split between male and female subjects in the dataset, with males comprising a slight majority at 51.2%. The correlation matrix shows no strong correlations between the variables, as all the values are close to zero. Specifically, none of the health metrics (Age, Heart Rate, Respiratory Rate, Body Temperature, and Oxygen Saturation) display a strong positive or negative linear relationship with one another in this particular dataset.

### Heart Rate by Activity Level

<img width="768" alt="heart_rate_by_activity_level" src="https://github.com/user-attachments/assets/cee8143c-e416-4bc3-9cb1-1efb8ae5c658" />


It shows that the median heart rate increases from resting to walking, which is expected as physical activity increases. However, the median heart rate does not significantly increase further during running compared to walking, which is unusual since we would expect a higher median heart rate for a more strenuous activity. Additionally, there is considerable overlap in the interquartile ranges between walking and running, suggesting similar variability in heart rates for these activities within the sampled population. The presence of outliers in the resting category indicates that some individuals have resting heart rates that are much higher than the typical range for the rest of the group.

### Blood Pressure Distribution and Heart Rate / Oxygen Saturation by Gender

<img width="334" alt="bp_distribution_and_other_metrics_by_gender" src="https://github.com/user-attachments/assets/5b50fb86-0790-481c-b2a4-c3c06dbc0ef5" />


The systolic blood pressure, represented in blue, shows a more spread-out distribution with peaks suggesting common readings around 120 mmHg and 140 mmHg. The diastolic blood pressure, in red, appears to have a narrower distribution, with a significant peak around 80 mmHg. The spread of systolic values is broader than the diastolic ones, which is typical as systolic pressure tends to vary more with factors like activity level and stress. This distribution is consistent with general population trends where a systolic reading of around 120 mmHg and a diastolic reading of around 80 mmHg are considered normal.

For heart rate, both males and females show similar median values with a relatively similar interquartile range, indicating no significant difference in heart rate between genders within this dataset. In terms of oxygen saturation, again, both genders exhibit nearly identical medians and interquartile ranges, suggesting that oxygen saturation does not differ notably between males and females in this sample. There are a few outliers in oxygen saturation for both genders, indicating a few individuals with lower than typical values, but these do not seem to affect the overall distribution significantly.

### Heart Rate and Oxygen Saturation by Sleep Quality and Stress Levels

![heart_rate_and_oxygen_saturation_by_sleep_and_stress](https://github.com/user-attachments/assets/e67948f1-ffa0-434c-bac5-06414cb6e570)

Heart rate appears relatively consistent across different levels of sleep quality and stress, with a slight increase in variation for those reporting poor sleep. Oxygen saturation shows a minimal decrease in median values from excellent to poor sleep quality, with some outliers indicating lower saturation for excellent and good sleep. When correlated with stress levels, oxygen saturation remains largely unchanged. Overall, while there are outliers, the central tendencies suggest that neither heart rate nor oxygen saturation is greatly affected by sleep quality or stress level within this dataset.

### Respiratory Rate and Body Temperature by Activity Level

![respiratory_rate_and_body_temperature_by_activity](https://github.com/user-attachments/assets/0b1d401b-9761-4d92-bc02-8260bb875363)

The respiratory rate tends to increase with activity level, as indicated by higher median rates for walking and running compared to resting. It aligns with physiological responses to exercise, where the breathing rate increases to meet oxygen demands. For body temperature, there is a slight upward trend from resting to running, which is consistent with the body heating up during physical exertion. There are outliers in body temperature at the resting and running levels, suggesting some individuals have temperatures outside the typical range for these activities. Overall, the trends observed are in line with expected physiological responses to varying levels of activity.

### Grouping Patients based on Age Groups, Blood Pressure Categories, Heart Rate Categories, and Oxygen Saturation Categories

![distrubution_of_patient_groupings](https://github.com/user-attachments/assets/739d35b7-d8bc-467c-a6c1-1a03686e4803)

**Observation:**
1. **Distribution of Age Groups:** The count plot shows that the ‘Senior’ category has the highest count, followed by the ‘Young’ and ‘Middle-aged’ categories. It suggests that seniors are the largest age group in this dataset.
2. **Distribution of Blood Pressure Categories:** The majority of the dataset falls under ‘Normal’ blood pressure, with fewer instances in the ‘Elevated’ and ‘Hypertension Stage 1’. ‘Hypertension Stage 2’ has the lowest count, indicating that severe hypertension is less common among the participants.
3. **Distribution of Heart Rate Categories:** Most individuals have a ‘Normal’ heart rate, with very few falling into the ‘Low’ or ‘High’ categories. It indicates that most individuals in this dataset have a heart rate that falls within the expected range.
4. **Distribution of Oxygen Saturation Categories:** Almost everyone has ‘Normal’ oxygen saturation levels, with very few instances of ‘Low’ saturation. It suggests that oxygen deprivation is not a common issue in this group.






