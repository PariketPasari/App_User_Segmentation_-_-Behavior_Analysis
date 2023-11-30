# App User Segmentation & Behavior Analysis 

## Problem Statement
Understanding and analyzing user behavior on a mobile app is essential for app developers and marketers. The challenge is to identify patterns and factors influencing user engagement, retention, or churn.

## Goal
The goal of this project is to analyze user behavior on a mobile app using various metrics such as average screen time, spending, ratings, and last visit minutes. The objective is to gain insights into user engagement, identify potential churn indicators, and provide actionable recommendations for improving user retention.

## Dataset
The dataset includes the following features:
- `userid`: A unique identifier for each user.
- `Average Screen Time`: The average time a user spends on the app (in minutes).
- `Average Spent on App (INR)`: The average amount of money spent by a user on the app (in Indian Rupees).
- `Left Review`: Binary variable indicating whether a user left a review (1) or not (0).
- `Ratings`: User ratings given for the app.
- `New Password Request`: The number of times a user requested a new password.
- `Last Visited Minutes`: The number of minutes since the user's last visit.
- `Status`: The current status of the user, whether they are "Installed" or "Uninstalled" the app.

## EDA & Visualization
### Key Insights:
- **Average Screen Time:** Ranges from 0 to 50 minutes, with an average of 24 minutes.
- **Average Spent on App (INR):** Average spending is 424 INR, ranging from 0 to 998 INR.
- **Rating:** Ratings range from 0 to 10.
- **Status:** Out of 999 users, 83 don't have the app installed, while 916 have it installed.
- Users with less average screen time are more likely to uninstall the app, typically having less than 5 minutes of screen time.
- Users with higher screen time tend to provide higher ratings.
- Users who spent around 100 INR but uninstalled the app usually gave a maximum rating of 5.

### Behavior Analysis
- Users with less average screen time, typically below 5 minutes, are more likely to uninstall the app.
- Users installing the app with elevated screen time tend to give above-average ratings, while lower screen time users are more likely to provide below-average ratings and uninstall the app.
- Users spending around 100 rupees but uninstalling the app generally gave a maximum rating of 5. In contrast, higher-spending users who both installed and made purchases tend to give higher ratings.

### User Status Comparison:
- Users with the app installed have higher screen time and spending.
- Average spending is notably higher among users with the app installed.
- Ratings provided by users with the app installed are significantly higher.
- time of the last visit is markedly longer among users who don't have the app installed on their devices

## User User segmentation based on screen time & spending behviour:

![image](https://github.com/PariketPasari/App_User_Segmentation_and_Behavior_Analysis/assets/49834871/ee1ccd1f-2b81-496b-b545-4e514e4658ed)

**Clusters**
- LOW USAGE LOW SPENDING - CLUSTER 1
- HIGH USAGE HIGH SPENDING - CLUSTER 2
- MODERATE USAGE MODERATE SPENDING - CLUSTER 0

**Cluster Interpretation:**
- Users belonging to the 'High Engagement' cluster are likely more active and engaged with the app, as indicated by their extended screen time and frequent visits.
- Users in the 'Low Engagement' cluster may exhibit less activity or sporadic app usage, suggested by lower screen time and less frequent visits.

## user Segmentation to find app user's retention, or churn: 

![image](https://github.com/PariketPasari/App_User_Segmentation_and_Behavior_Analysis/assets/49834871/f4b8c479-435a-4891-b92f-2330ceebc1f0)

- **Clusters**
- Cluster 0: Retained Users
- Cluster 1: Lost Users
  
  **Cluster Interpretation:**
- Retained Users: This cluster comprises users who demonstrate ongoing engagement with the app, characterized by a relatively higher average screen time and last visited minutes.
- Lost Users: Users in this cluster exhibit lower engagement metrics, suggesting potential disinterest or abandonment of the app.


## Overall Conclusions & Findings
**Behavior Analysis:**
- Users with less average screen time (< 5 minutes) are more likely to uninstall the app. Elevated screen time correlates with higher ratings, while lower screen time corresponds to below-average ratings and app uninstallation. Users who spent around 100 rupees but uninstalled the app typically gave a maximum rating of 5, whereas higher spending users tend to provide higher ratings.

**User Status Comparison:**
- Users with the app installed exhibit higher screen time and spending compared to those without the app. Average spending is notably higher among users with the app installed. Ratings provided by users with the app installed are significantly higher compared to users without the app. The time of the last visit is longer among users without the app installed.

**User Segmentation to Identify Retention or Churn:**
- User Segmentation identifies 'Retained Users' and 'Lost Users' based on higher or lower engagement metrics. 'Retained Users' exhibit ongoing engagement, while 'Lost Users' show lower engagement, indicating potential uninstallation. This segmentation guides targeted efforts to retain users and mitigate churn by tailoring interventions to specific user needs.
  
**User Segmentation based on Screen Time & Spending Behavior:**
- User Segmentation categorizes users into 'Low Usage, Low Spending,' 'Moderate Usage, Moderate Spending,' and 'High Usage, High Spending.' The 'High Usage, High Spending' cluster represents the most engaged and valuable segment. This segmentation strategy enables targeted marketing and personalized experiences for each user segment.

## Suggestions for Further Improvement:
1. **Feature Engineering:**
   Explore additional features or derive new ones for deeper insights into user behavior, considering session frequency, in-app activities, or demographics.
2. **Temporal Analysis:**
   Incorporate time-based analysis to understand how user behavior evolves over time on a monthly or quarterly basis.
3. **Advanced Clustering Techniques:**
   Experiment with other clustering algorithms (e.g., hierarchical clustering, DBSCAN) to identify more meaningful user segments.
4. **Predictive Modeling:**
   Move beyond descriptive analysis and explore predictive modeling to anticipate user behaviors, such as churn or engagement, based on historical data.

