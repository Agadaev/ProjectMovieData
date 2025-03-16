# Project Movie Dashboard
## Table Content
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning & Preperation](#data-cleaning-and-preperation)
- [Questions for Data Analysis](#questions-for-data-analysis)
- [Dashboard](#dashboard)
- [Results and Findings](#results-and-findings)
- [Challenges in Analysis](#challenges-in-analysis)

### Project Overview
This data analysis project is designed to provide insights into the performance and trends of movies from 2012 to 2016 for Apple TV's creative directors. By exploring the dataset, we aim to:
- Uncover patterns in movie performance, including box office revenue and production budgets.
- Evaluate trends across various genres, actors, and directors.
- Deliver data-driven recommendations for future content strategies.
- Enhance understanding of the movie industry's dynamics during the analyzed period.

## Data Sources
The primary dataset, "Movie Data Homework.xlsx", contains detailed information on each movie, including box office performance, production budget, cast, crew, and genre classifications - [Movies Data Dashboard.xlsx](https://github.com/user-attachments/files/19275898/Movies.Data.Dashboard.xlsx)


## Tools
- **Power Query** - Utilized for data extraction, cleaning, and transformation. Power Query enabled us to manage and preprocess the raw movie data effectively.
- **Excel** - Used for deeper data analysis and visualization. Key Excel features employed in the project include:
  - Pivot Tables: Essential for summarizing data and creating interactive dashboards.
  - Charts and Graphs: For visual representation of trends and key performance indicators.

## Data Cleaning & Preperation
Before analysis, the following steps were carried out:
- **Data Loading and Inspection:**
  Imported the Excel file and conducted an initial assessment to understand its structure.
- **Handling Errors and Missing Values:** Identified inconsistencies and missing data points. Applied appropriate methods (e.g., imputation, removal) to handle these issues.
- **Data Formatting:** Standardized date formats, numerical values, and text fields to ensure consistency. The cleaned and preprocessed dataset is available for download here - [Ready to use Dashboard](https://github.com/user-attachments/files/19238698/Cleaned.Movie.Data.with.combined-Avi.xlsx)

## Questions for Data Analysis
The analysis was guided by several key questions:

 1. **Genre Performance:**
    Which top 10 genres achieved the highest box office revenue during the analyzed period?

 2. **Actor Impact:**
    Who are the top 5 actors contributing to the most successful movies based on box office performance?

 3. **Movie Rankings:**
    Which are the top 5 movies when ranked by both box office revenue and production budget?

 4. **Seasonal Trends:**
    How do movie releases and performances vary by season throughout the year?

## Dashboard

The final dashboard integrates interactive visuals and summaries that address the above questions. It provides an at-a-glance view of:
- Revenue by genre, actor, and season.
- Detailed drill-down capabilities to inspect individual movie performances.
- Comparative analyses between box office revenue and budget allocations.


## Results and Findings
Key findings from the analysis include:
- **Genre Success:** For Example, the Best movie for 2013-2016 with the most profitable Box revenue of 102,000,00 USD in the Horror genre was:
![BestMovie](https://github.com/user-attachments/assets/7afe3433-9b9b-4287-b781-76c33c962655)

- **Top Performers:**
The dashboard highlights the best-performing movies and the leading actors who have driven success across multiple metrics.
![Dashboard](https://github.com/user-attachments/assets/c33157e2-de85-4c66-8a1b-dd101a00bb8c)


## Challenges in Analysis
### M Language
Advanced transformations in Power Query using M Language were sometimes complex. Debugging and optimizing these scripts was essential to ensure the reliability and efficiency of the data transformation process.
```
let
    // Load your movie data table 
    Source = Movie_Data_Table,
    
    // Transform column types
    ChangedType = Table.TransformColumnTypes(
        Source,
        {
            {"Movie Title", type text},
            {"Combined Genre", type text},
            {"Release Date", type date},
            {"Wikipedia URL", type text},
            {"Director", type any},
            {"Cast (1)", type text},
            {"Cast (2)", type text},
            {"Cast (3)", type text},
            {"Cast (4)", type text},
            {"Cast (5)", type text},
            {"Budget ($)", Int64.Type},
            {"Box Office Revenue ($)", type number},
            {"ROI", type number}
        }
    )
in
    ChangedType

```
