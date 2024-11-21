# Videogame Store Project

## Overview
This project focuses on analyzing trends in the video game market to provide actionable insights for a store selling video games. The dataset contains information such as game titles, release years, genres, ratings, and sales data. The analysis aims to identify key trends and patterns in video game sales to guide stocking and sales strategies for the year 2017.

---

## Data Preparation

### Handling Missing Values
1. **Name:**  
   - Missing values in the "Name" column were removed as they provide no relevant information and could be errors in the database.

2. **Year of Release:**  
   - Games without a release year were excluded. Since the analysis focuses on trends leading up to 2017, the release year is essential for comparisons. The 269 missing values (1.6% of the dataset) were deemed an acceptable loss.

3. **Genre:**  
   - Missing values in the "Genre" column were identical to those in the "Name" column and were similarly removed.

4. **Ratings:**  
   - Missing rating values were categorized as "U" (Undefined). With access to an ESRB API, these could potentially be verified and updated, but this is beyond the scope of the project.

5. **Critic and User Scores:**  
   - Scores were standardized to the same scale (base 100). For rows where one score was missing but the other was available, the available score was duplicated. Rows missing both scores were marked as NaN and excluded from relevant analyses.

---

## Key Insights

### Generational Trends
- A noticeable spike in sales coincides with the release of new console generations, followed by a decline as the generation matures. This analysis focuses on data from 2012 to 2016, corresponding to the eighth generation of consoles.

---

## Conclusions

### 🔍 Key Findings
- The **European** and **American markets** behave similarly, with **PS4** and **Xbox One** as the leading platforms.  
- The most popular genres are **action** and **shooter**, particularly multiplayer games.  
- **Critic reviews** have a stronger correlation with sales compared to user reviews, regardless of genre.

### 🤔 Impact of Data Processing Choices
- Data with minimal or irrelevant information was excluded, focusing the analysis on actionable insights.  
- While the dataset spans from 1980, the analysis prioritized recent years for relevance.  
- The dataset lacks differentiation between physical and digital sales, discounted sales, or returns. This limits its applicability for retail-specific strategies but provides a broad view of market trends.

### 🎯 Relation to Initial Objectives
The analysis successfully provides insights into general video game sales trends and informs decisions for stocking strategies in 2017.

### 🚀 Suggestions and Recommendations
For the 2017 period, the following strategies are suggested based on the data:
1. Stock **PS4** games, followed by **Xbox One** titles, especially in North America and Europe.  
2. Offer a variety of genres but prioritize **multiplayer shooters**, as they are the best-selling category.

### 📝 Final Thoughts
This project demonstrates how to effectively clean and standardize a dataset to align with specific research questions. A key takeaway is the importance of defining criteria for excluding, standardizing, or adapting data to suit the needs of the analysis.

---
