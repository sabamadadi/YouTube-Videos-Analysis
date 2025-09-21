# Trending YouTube Videos Analysis
[View Full Report](https://drive.google.com/file/d/1B2rUIn5iJ1CUvf1bYmav0W16_sCJGEQf/view?usp=sharing)  

 [The scraping part is explained separately.](https://github.com/sabamadadi/YouTube-Videos-Analysis?tab=readme-ov-file#scpraping)  


## Overview
This project analyzes the factors influencing YouTube videos trending globally.  
It uses a dataset of trending videos from 10 countries, including metrics like views, likes, dislikes, and comments.

## Data & Methods
- Dataset: Trending videos with metadata such as category, title, description, tags, and publish time.  
- Analysis: Exploratory Data Analysis (EDA), data visualization, and statistical tests (Chi-Square, Kruskal-Wallis).  
- Features studied: Video category, title/description sentiment, clickbait usage, upload timing, and engagement metrics.

## Key Findings
- **High engagement categories:** Music, entertainment, and film.  
- **Content features:** Title and description length have minimal impact.  
- **Sentiment & clickbait:** Positive sentiment and attention-grabbing words increase engagement.  
- **Comments:** Videos with comments enabled show higher engagement.  
- **Upload timing:** Peak engagement occurs on Fridays and afternoons.

## Insights
- Engagement differs significantly across categories but not weekdays.  
- Neutral titles dominate total engagement, while controversial videos spark discussion but attract fewer views.  
- Tags initially increase engagement, but excessive tags do not add value.

## Applications
These insights help new YouTubers optimize content strategy for higher views and engagement.  
Future work could include exploring tag effectiveness, audience demographics, and cross-country trends.

# Scpraping


## Overview
This project focuses on scraping and analyzing trending YouTube videos using the YouTube Data API. The scraper collects comprehensive metadata and engagement statistics for trending videos across multiple countries, allowing for analysis of patterns, trends, and factors that contribute to video popularity.

The script reads an API key and a list of country codes from specified files, authenticates requests, and retrieves the most popular videos in each country. By handling pagination, it gathers extensive data even when multiple pages of results exist.

## Features Collected
The dataset contains a wide range of information for each video:

- **Video ID**
- **Title** and its sentiment
- **Published date and time**
- **Channel ID** and channel title
- **Category ID** and category title
- **Tags**
- **View count, likes, and dislikes**
- **Comment count**
- **Thumbnail link**
- **Status of comments and ratings** (enabled or disabled)
- **Video description** and its sentiment

Additional processing includes cleaning unsafe characters, detecting clickbait words in titles, and calculating engagement levels.

## Supported Countries
Data can be collected from the following countries:

- Australia (AU)  
- Portugal (PT)  
- Spain (ES)  
- South Korea (KR)  
- Russia (RU)  
- Japan (JP)  
- Brazil (BR)  
- Mexico (MX)  

This multi-country approach allows for cross-region comparison and understanding regional differences in trending content.

## Data Processing
After scraping, category IDs are mapped to descriptive titles. Categories are divided into:

- **Assignable Categories:** Chosen by content creators during upload.  
- **Non-Assignable Categories:** Automatically assigned by YouTube.  

Key preprocessing steps include:

- Removing unsafe characters to ensure CSV compatibility.  
- Extracting tags and formatting them consistently.  
- Creating additional features like title length, description length, sentiment scores, and clickbait indicators.  
- Extracting publication details including year, month, season, day of the week, and hour.  

These steps ensure clean, analyzable data ready for visualization and insights.

## Analysis Insights
Analysis of the 2025 dataset revealed significant trends:

- **Category Popularity:** In Mexico, the top three video categories have changed compared to the 2017-2018 dataset, reflecting shifts in audience preferences. Globally, music remains the most popular category, followed by entertainment and film.  
- **Engagement Drivers:** Positive sentiment in titles and descriptions increases engagement. Titles containing attention-grabbing words like “shocking,” “must watch,” “amazing,” “incredible,” and “unbelievable” also boost interaction. Length of title or description has little effect.  
- **Upload Timing:** Videos published around 4 PM on Fridays tend to perform better. Spring and winter see more trending videos compared to other seasons.  
- **Controversial vs. Universally Liked Videos:** Universally liked videos attract more views but provoke less discussion, while controversial videos generate higher interaction despite lower overall views.  
- **Comments and Ratings:** Videos with enabled comments outperform those with disabled comments in engagement, highlighting the importance of interactive features.

## Conclusion
This scraping and analysis workflow provides a systematic way to collect and examine trending YouTube video data across regions. Key takeaways include:

- Understanding changing trends over time.  
- Identifying factors that influence engagement and virality.  
- Guiding content creators on optimal video categories, titles, sentiment, and upload timing.  

Analysis of 2025 data compared to historical datasets underscores the importance of using current data for actionable insights. Staying updated with trends allows creators to adapt strategies effectively, enhancing their chances of creating content that resonates with audiences.
