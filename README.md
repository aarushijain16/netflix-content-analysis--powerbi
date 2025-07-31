# netflix-content-analysis--powerbi
This project provides an in-depth analysis of Netflix's content library, dissecting distribution trends by type, release year, genre, and country. Built using Power BI with data from Kaggle, this report offers actionable insights into content strategy, audience preferences, and global reach through interactive visualizations.

# Netflix Content Analysis: Trends & Distribution

## Executive Summary:

This project conducts a comprehensive analysis of Netflix's content library, presented through an interactive Power BI dashboard. The analysis dissects content distribution by type (movies vs. TV shows), release year trends, genre popularity, and geographic reach. The goal is to provide data-driven insights into content strategy, identify popular categories, and understand the global footprint of Netflix's offerings.

## Problem Statement:

The primary objective was to transform raw Netflix content data into actionable intelligence across key content strategy areas:

- **Content Type Distribution**: To precisely identify the proportion of Movies versus TV Shows in the Netflix library and analyze their distribution over release years.

- **Content Reach & Diversity**: To understand the number of countries Netflix content originates from and the top directors by country and content type.

- **Genre and Rating Analysis**: To assess the popularity of various genres and the distribution of content by rating.

## Data Sources and Engineering:

This project utilized publicly available datasets from Kaggle, which were integrated and transformed within Power BI to create the comprehensive Netflix Content Dashboard. The primary data sources include:

- netflix data.xlsx - netflix1.csv: Contains core content details (show_id, type, title, release_year).

- netflix data.xlsx - Sheet2.csv: Provides additional content attributes (release_year, rating, duration, listed_in (genre)).

- netflix data.xlsx - Sheet1.csv: Includes director and country information (director, country, date_added, release_year).

The release_year column served as a common key for establishing relationships and integrating data across these sheets within the Power BI data model.

My data engineering process (as implemented within Power BI's Power Query Editor and data model) involved:

- **Data Acquisition**: Sourcing the publicly available Netflix datasets from Kaggle directly into Power BI.

- **Data Cleaning and Preprocessing**: Handled missing values (e.g., "Not Given" for director), ensured consistent data types, and performed necessary transformations to prepare data for analysis.

- **Feature Engineering**: Calculated key performance metrics and created new features to support deeper analysis, including:

  - Total Content

  - No. of Countries

  - No. of Shows

  - No. of Movies

  - Categorization of content by TYPE (Movie/TV Show).

  - Aggregation of content by RELEASE YEAR, GENRE, COUNTRY, and DIRECTOR.

- **Understanding Cardinality**:
  
Cardinality refers to the number of unique values in a column. Understanding cardinality is crucial for effective data modeling and visualization in Power BI:

  - **High Cardinality**: Columns like show_id are expected to have very high cardinality, as each entry is a unique identifier. These are essential for identifying individual records but are not typically used for direct categorical visualization.

 - **Low Cardinality**: Columns such as type (Movie/TV Show) have low cardinality, containing a limited number of distinct values. These are ideal for creating categorical visualizations (e.g., bar charts, pie charts) and filters.

  - **Medium to High Cardinality**: Columns like release_year, country, and listed_in (genre) typically have medium to high cardinality. While they contain many distinct values, they are highly valuable for trend analysis, geographic breakdowns, and detailed genre exploration. Recognizing their cardinality helps in choosing appropriate visualization types and optimizing data model performance.

## Methodology:

The analytical approach for this project was multi-faceted, focusing on turning raw content data into actionable business intelligence through the Power BI dashboard:

- **Overall Content Overview**: Calculated and visualized total content, number of movies, number of TV shows, and the number of countries represented using summary cards and appropriate visuals.

- **Content Type Distribution by Release Year**: Analyzed the trends of Movies vs. TV Shows released over time using an area chart, identifying periods of growth or shift in content strategy.

- **Genre Popularity**: Explored the distribution of content across various genres (e.g., TV Shows, TV Sci-Fi & Fantasy, TV Horror, TV Dramas, TV Comedies, Thrillers, Stand-Up Comedy & Talk Shows) using bar charts.

- **Geographic Analysis**: Identified the top directors by country and analyzed content distribution across different regions (Europe, Africa, South America, etc.) using map visuals and tables.

- **Rating Distribution**: Examined the breakdown of content by various ratings (e.g., GNC-17, NR, PG, PG-13) using bar charts or pie charts.

## Key Findings and Impact:

- **Content Library Composition**: Netflix has a Total Content of 8.78K, with 6.13K Movies and 2.66K TV Shows. This indicates a larger volume of movies compared to TV shows.

- **Global Reach**: Content originates from 86 countries, highlighting Netflix's extensive international presence.

- **Content Distribution Over Time**: The "Content Type Distribution by Release Year" chart shows the volume of both movies and TV shows increasing significantly towards more recent years (e.g., 2000s onwards), with a notable surge in TV shows around 2015-2020.

- **Top Genres**: The dashboard highlights various TV show genres such as TV Sci-Fi & Fantasy, TV Horror, TV Dramas, TV Comedies, and TV Action & Adventure, along with Thrillers and Stand-Up Comedy.

- **Rating Distribution**: The dashboard presents a breakdown of content by ratings like GNC-17, NR, PG, and PG-13, with specific counts (e.g., 4.45K for one rating, 4.53K for another, and smaller counts of 5 and 8).

- **Director Insights**: The "DIRECTOR BY TYPE" section indicates a significant number of entries (4.45K and 4.53K) related to directors, suggesting a rich pool of creators. "TOP DIRECTORS BY COUNTRY" provides a geographical breakdown of directorial contributions.

## Strategic Recommendations:

- **Balance Content Investment**: While movies dominate the volume, the growth in TV shows suggests a strong demand. Continue to invest strategically in both, perhaps focusing on high-impact TV series to drive subscriptions and retention.

- **Expand Genre Diversity**: Leverage the insights from top genres to identify underserved niches or emerging trends. Consider investing more in popular TV show genres to cater to diverse audience preferences.

- **Optimize Global Content Acquisition**: Utilize the "No. of Countries" and "TOP DIRECTORS BY COUNTRY" insights to identify regions with high content output or strong audience engagement. This can inform future content acquisition or production partnerships.

- **Targeted Content Development based on Ratings**: Understand which ratings perform best with specific audience segments to guide future content development and marketing campaigns.

- **Leverage Director Talent**: Analyze the "DIRECTOR BY TYPE" and "TOP DIRECTORS BY COUNTRY" data to identify prolific or highly-rated directors for potential collaborations, especially those with a strong track record in high-demand content types or genres.

## Tools and Technologies:

- **Data Visualization & Analysis**: Power BI 

- **Data Source**: Multiple CSV files from Kaggle (netflix data.xlsx - netflix1.csv, netflix data.xlsx - Sheet2.csv, netflix data.xlsx - Sheet1.csv), linked by release_year.

## Visualizations:

- Overall Content Metrics (Total Content, No. of Countries, No. of Shows, No. of Movies)

- Content Type Distribution by Release Year (Area Chart)

- Genre Distribution (Bar Chart)

- Top Directors by Country (Map/Table)

- Director by Type (Bar Chart)

- Rating Distribution (Bar Chart)
