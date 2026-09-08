# 📱 Google Play Store Analysis & Rating Prediction

## 📌 Project Overview

This project analyzes Google Play Store application data to understand app performance, user engagement, popularity, ratings, installations, pricing, and market trends.
The project uses Python for data cleaning, exploratory data analysis (EDA), and feature engineering, followed by Power BI for interactive visualization and business insights.
A machine learning component is also included to predict application ratings using relevant app characteristics and engagement-related features.


## 🎯 Problem Statement
The Google Play Store contains a large number of applications across different categories, genres, pricing models, and target audiences.

The objective of this project is to analyze application data and identify:
- Which app categories contain the highest number of applications
- Which categories and applications have the highest installations
- Which applications receive the most reviews
- How ratings are related to reviews and installations
- Distribution of free and paid applications
- Pricing patterns across different categories
- Relationship between app size, ratings, reviews, and installations
- Popular applications and categories
- Application update patterns
- Whether application characteristics and engagement metrics can help predict app ratings

These insights can help developers and businesses understand user preferences, application popularity, and factors associated with app performance.

## 📂 Dataset
The dataset contains information about applications available on the Google Play Store.

### Original Dataset
- Records: 10,841
- Columns: 13

### Cleaned Dataset
- Records: 10,840
- Columns: 16

The cleaned dataset includes additional date-based features created during feature engineering.

### Important Columns
| Column | Description |
|---|---|
| App | Name of the application |
| Category | Category under which the application falls |
| Rating | Application rating on Google Play Store |
| Reviews | Number of user reviews |
| Size | Application size |
| Installs | Number of installations |
| Type | Free or Paid application |
| Price | Price of the application |
| Content Rating | Target audience/content rating |
| Genres | Genre of the application |
| Last Updated | Date when the application was last updated |
| Current Ver | Current version of the application |
| Android Ver | Minimum Android version required |
| Day | Day extracted from Last Updated |
| Month | Month extracted from Last Updated |
| Year | Year extracted from Last Updated |

## 🔄 Project Workflow

Raw Dataset
     ↓
Data Cleaning using Python
     ↓
Exploratory Data Analysis (EDA)
     ↓
Feature Engineering
     ↓
Business Insights
     ↓
Power BI Visualization
     ↓
Machine Learning – App Rating Prediction
     ↓
Model Evaluation & Business Recommendations

**##🧹 Data Cleaning**

The dataset was cleaned and prepared using Python and Pandas.
Major data cleaning steps included:

Checked dataset shape and structure
Inspected data types and descriptive statistics
Identified missing values
Identified non-numeric values in the Reviews column
Removed the invalid Reviews record
Converted Reviews into integer format
Converted Size values into numeric format
Handled M, k, and Varies with device values in the Size column
Removed + and commas from Installs
Converted Installs into integer format
Removed $ from Price values
Converted Price into numeric format
Converted Last Updated into datetime format
Checked duplicate application records
Created a cleaned dataset for further analysis

**🔧 Feature Engineering**
Feature engineering was performed to make the dataset more suitable for analysis.
The following features were extracted from the Last Updated column:

Day
Month
Year

These features allow application update patterns to be analyzed over time and can also be used as potential features during predictive modeling.

**##📊 Exploratory Data Analysis**
EDA was performed using Pandas, Matplotlib, and Seaborn.

**Categorical Analysis**
The following categorical variables were analyzed:
App Category
Type (Free vs Paid)
Content Rating
Genre

**Numerical Analysis**
The following numerical variables were analyzed:

Rating
Reviews
Installs
Size
Price
Year

**Relationship Analysis**
Relationships between important variables were explored, including:

Rating vs Reviews
Rating vs Installs
Category vs Installs
Category vs App Count
Category vs Price
App Size vs numerical variables

**Popularity Analysis**
The analysis also focused on:

Top installed applications
Top applications by number of reviews
Top applications within popular categories
Categories with the highest number of applications
Categories with the highest total installations

🔍 Key Insights
📱 App Categories

The Family category contains the highest number of applications, followed by Games and Tools.

The analysis also shows that categories such as Beauty, Comics, Arts, and Weather contain comparatively fewer applications.

📥 Application Installations

The Game category has the highest number of installations, with approximately 35 billion installations in the analyzed dataset.

Other highly installed categories include:

Communication
Tools
Productivity
Social
⭐ Ratings and User Engagement

The analysis explored the relationship between application ratings, reviews, and installations.

Applications with higher levels of user engagement tend to receive larger numbers of reviews and installations, although these relationships should be interpreted as associations rather than causal effects.

💰 Free vs Paid Applications

The majority of applications in the dataset are free applications, while paid applications represent a much smaller proportion.

💵 Pricing

Higher-priced applications are concentrated in categories such as:

Finance
Lifestyle

while highly installed applications are more commonly found in categories such as:

Games
Communication
Tools
Social
📈 Power BI Dashboard

An interactive Power BI dashboard was created to present the major findings from the analysis.

Dashboard KPIs
Total Apps
Total Installs
Average Rating
Total Reviews
Dashboard Visualizations
Number of Apps by Category
Free vs Paid Apps
Average Size by Category
Average Rating vs Reviews
Average Rating by Category
Top 10 Apps by Reviews
Top 10 Apps by Installs
Category filter
Genre filter
Type filter
Content Rating filter
