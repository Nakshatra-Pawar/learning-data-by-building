# Netflix Content Strategy Analysis

This project explores Netflix’s catalog of movies and TV shows to understand content trends, country-level patterns, genre distribution, release timing, and recurring talent presence.

The goal of this project is to use exploratory data analysis to generate simple, data-driven business insights that could help support content strategy and production decisions.

## Project Goal

The main goal of this project is to analyze Netflix title data and answer questions such as:

* What kind of content is most common on Netflix?
* How have movie releases changed over time?
* Are TV Shows becoming more important in recent years?
* Which countries contribute the most Netflix titles?
* Which genres are strongest in the catalog?
* Are there certain months with stronger TV Show additions?
* Which actors and directors appear most frequently?

## Dataset

The dataset used in this project contains information about Netflix titles, including:

* `show_id`
* `type`
* `title`
* `director`
* `cast`
* `country`
* `date_added`
* `release_year`
* `rating`
* `duration`
* `listed_in`
* `description`

During analysis, a few additional columns were created for easier exploration:

* `year_added`
* `month_added`
* `month_name_added`
* `main_country`

## Tools Used

* Python
* Pandas
* Matplotlib
* Seaborn
* Jupyter Notebook / VS Code

## Project Workflow

This project was completed in the following steps:

1. Loaded and inspected the dataset
2. Checked data shape, columns, and missing values
3. Cleaned and transformed date fields
4. Created new time-based and country-based features
5. Compared Movies and TV Shows
6. Analyzed release-year trends
7. Studied content additions over time
8. Explored country-level title distribution
9. Examined TV Show additions by month
10. Identified top genres, actors, and directors
11. Summarized business insights and recommendations

## Key Insights

Some of the main findings from this project are:

* Movies dominate the Netflix catalog overall.
* Both Movies and TV Shows grew strongly after 2015.
* Movies are still added in larger numbers than TV Shows, although TV Shows also show strong growth.
* The Netflix catalog is heavily concentrated in a few countries, especially the United States, India, and the United Kingdom.
* Content mix differs by country. For example, Japan shows relatively stronger TV Show presence compared to some other top countries.
* International Movies and International TV Shows are among the most common genres.
* Drama and Comedy are two of the strongest genres in the catalog.
* TV Show additions are spread throughout the year, with relatively stronger activity in months like July, September, and December.
* Some actors and directors appear repeatedly across the catalog, suggesting recurring talent concentration.

## Business Recommendations

Based on the analysis, the following recommendations were made:

* Continue maintaining a strong movie pipeline, since Movies still dominate the catalog.
* Keep expanding TV Shows in a targeted way, especially in markets where series appear stronger.
* Continue investing in international content, since it is one of Netflix’s biggest strengths.
* Use more localized content strategy by country instead of applying one global content mix everywhere.
* Prioritize broad-appeal genres such as Drama and Comedy.
* Consider stronger TV content pushes during high-activity months.

## Limitations

This project has a few limitations:

* The dataset shows catalog availability, not title performance or viewer engagement.
* `date_added` reflects when a title was added to Netflix, not when it was originally produced.
* For country-level analysis, only the first listed country was used as the main country.
* Frequent actors and directors reflect catalog presence, not quality or popularity.

## Files in This Project

* `netflix_content_strategy_analysis.ipynb` — main notebook with data cleaning, analysis, charts, and findings
* `datasets/netflix_data.csv` — source dataset
* `README.md` — project documentation

## How to Run

1. Open the project folder in VS Code or Jupyter Notebook
2. Install the required libraries:

   ```bash
   pip install pandas matplotlib seaborn jupyter
   ```
3. Run the notebook:

   ```bash
   jupyter notebook
   ```

   or open the notebook directly in VS Code

## Learning Outcome

This project helped me practice:

* working with a real-world tabular dataset
* cleaning and transforming date columns
* handling missing values
* creating new analysis features
* splitting and analyzing multi-value text columns
* building charts for business-focused analysis
* turning analysis into simple recommendations

## Note

This is part of my broader **Learning Data by Building** repository, where I document my hands-on learning journey through small data engineering and data science projects.
