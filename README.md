# 📱 Google Play Store Analysis

## 📌 Project Overview
This project analyzes Google Play Store application data to understand app performance, user engagement, popularity, ratings, installations, pricing, and market trends.

The analysis follows an end-to-end data analytics workflow:

**Python Data Cleaning & EDA → Feature Engineering → Power BI Dashboard**

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

These insights can help developers and businesses understand user preferences, application popularity, and factors associated with app performance.

## 🎯 Business Objectives
The project aims to answer important business questions such as:

- Which app categories contain the most applications?
- Which categories generate the highest number of installations?
- Which applications have the highest number of reviews?
- How are ratings related to reviews and installations?
- What is the distribution of free and paid applications?
- Which categories have higher average application prices?
- Which categories have larger average application sizes?
- Which applications are the most popular?
- What patterns can be observed in application updates?
- How can these insights support data-driven application and business decisions?

## 📂 Dataset
The dataset contains information about applications available on the Google Play Store.

### Original Dataset
- **Records:** 10,841
- **Columns:** 13

### Cleaned Dataset
- **Records:** 10,840
- **Columns:** 16

The cleaned dataset includes additional date-based features created during feature engineering.

### Key Fields
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

# 🔄 Workflow of Analytics

## 1. 🧹 Data Cleaning & Preparation
Python and Pandas were used to inspect and prepare the raw Google Play Store dataset before performing further analysis.

### Activities Performed
- Loaded and inspected the dataset
- Checked dataset shape and structure
- Inspected data types and descriptive statistics
- Identified missing values
- Identified non-numeric values in the `Reviews` column
- Removed the invalid Reviews record
- Converted `Reviews` into integer format
- Converted `Size` values into numeric format
- Handled `M`, `k`, and `Varies with device` values in the `Size` column
- Removed `+` and commas from `Installs`
- Converted `Installs` into integer format
- Removed `$` from `Price` values
- Converted `Price` into numeric format
- Converted `Last Updated` into datetime format
- Checked duplicate application records
- Created a cleaned dataset for further analysis

## 2. 🔧 Feature Engineering
Feature engineering was performed to make the dataset more suitable for analysis.

### Additional Fields Created
- `Day`
- `Month`
- `Year`

These features were extracted from the `Last Updated` column.

The newly created date-based fields allow application update patterns to be analyzed over time.

## 3. 📈 Exploratory Data Analysis (EDA)
Exploratory Data Analysis was performed using Python to understand application characteristics, user engagement, popularity, and relationships between important variables.

### EDA Included
- Categorical variable analysis
- Numerical variable analysis
- Distribution analysis
- Application category analysis
- Installation analysis
- Rating analysis
- Review analysis
- Pricing analysis
- Free vs Paid application analysis
- Relationship analysis
- Popularity analysis
- Application update analysis

### Python Libraries Used
- Pandas
- NumPy
- Matplotlib
- Seaborn

### Categorical Analysis
The following categorical variables were analyzed:

- App Category
- Type (Free vs Paid)
- Content Rating
- Genre

### Numerical Analysis
The following numerical variables were analyzed:

- Rating
- Reviews
- Installs
- Size
- Price
- Year

### Relationship Analysis
Relationships between important variables were explored, including:

- Rating vs Reviews
- Rating vs Installs
- Category vs Installs
- Category vs App Count
- Category vs Price
- App Size vs numerical variables

### Popularity Analysis
The analysis also focused on:

- Top installed applications
- Top applications by number of reviews
- Top applications within popular categories
- Categories with the highest number of applications
- Categories with the highest total installations

## 4. 📊 Power BI Dashboard & Visualization
The final analysis was transformed into an interactive Microsoft Power BI dashboard to present the major findings in a clear and business-friendly format.

### KPI Metrics
- Total Apps
- Total Installs
- Average Rating
- Total Reviews

### Dashboard Visualizations
- Number of Apps by Category
- Free vs Paid Apps
- Average Size by Category
- Average Rating vs Reviews
- Average Rating by Category
- Top 10 Apps by Reviews
- Top 10 Apps by Installs

### Interactive Filters
- Category
- Genre
- Type
- Content Rating

# 🔍 Key Insights

## 📱 App Categories
The **Family** category contains the highest number of applications, followed by **Games** and **Tools**.

The analysis also shows that categories such as **Beauty, Comics, Arts, and Weather** contain comparatively fewer applications.

## 📥 Application Installations
The **Game** category has the highest number of installations, with approximately **35 billion installations** in the analyzed dataset.

Other highly installed categories include:
- Communication
- Tools
- Productivity
- Social

## ⭐ Ratings and User Engagement
The analysis explored the relationship between application ratings, reviews, and installations.

Applications with higher levels of user engagement tend to receive larger numbers of reviews and installations, although these relationships should be interpreted as associations rather than causal effects.

## 💰 Free vs Paid Applications
The majority of applications in the dataset are **Free applications**, while Paid applications represent a much smaller proportion.

## 💵 Pricing
Higher-priced applications are concentrated in categories such as:
- Finance
- Lifestyle

While highly installed applications are more commonly found in categories such as:
- Games
- Communication
- Tools
- Social

## 💡 Business Recommendations
Based on the analysis, the following recommendations can be considered:

### 📱 Category Strategy
Focus on high-performing categories such as **Games, Communication, Tools, and Productivity** to understand successful application characteristics and market demand.

### 🎯 Application Development
Use insights from highly installed and highly reviewed applications to identify popular features, categories, and user preferences when planning or improving applications.

### ⭐ Improve User Experience
Monitor application ratings and reviews to identify areas where user satisfaction can be improved and prioritize improvements based on user feedback.

### 📥 Increase User Engagement
Analyze applications with high installations and review volumes to understand engagement patterns and identify opportunities to improve downloads and user interaction.

### 💰 Pricing Strategy
Use category-level pricing analysis to understand how paid applications are positioned across different categories and support data-driven pricing decisions.

### 🆓 Free vs Paid Strategy
Since the dataset is heavily dominated by free applications, developers can evaluate whether a free, paid, or freemium approach is more appropriate based on category, competition, and user engagement.

### 🔄 Application Updates
Use application update patterns to understand how frequently successful applications are maintained and ensure regular updates to improve application quality and user experience.

### 📊 Data-Driven Decision Making
Combine application ratings, reviews, installations, category, pricing, and other application characteristics to support decisions related to application development, marketing, and product strategy.

## 🛠️ Tools & Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- Microsoft Power BI
- Power Query
- Data Cleaning
- Exploratory Data Analysis
- Feature Engineering
- Data Visualization

## 📁 Project Files
- `google_play_store_dataset.csv` – Original dataset
- `google_playstore_cleaned.csv` – Cleaned dataset
- `eda.ipynb` – Python data cleaning, EDA, and feature engineering
- `Google_Play_Store_Dashboard.pbix` – Power BI dashboard
- `Google_Play_Store_Dashboard_Preview.png` – Dashboard preview
- `README.md` – Project documentation

## 📌 Conclusion
The Google Play Store analysis provides insights into application popularity, user engagement, ratings, categories, pricing, installations, and application characteristics.

The analysis shows that **Family** has the largest number of applications, while **Game** has the highest total number of installations in the analyzed dataset.

Python was used for data cleaning, exploratory data analysis, and feature engineering, while Power BI was used to create an interactive dashboard for business-focused visualization.

Overall, the project demonstrates an end-to-end data analytics workflow for transforming raw application data into meaningful insights and business recommendations.

## 👤 Project Type
**Data Analytics Project**

### End-to-End Workflow
`Python → Feature Engineering → Power BI`
