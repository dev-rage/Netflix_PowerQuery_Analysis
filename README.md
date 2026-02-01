# Netflix Data Cleaning and Analysis Project

**A complete data pipeline demonstrating ETL processes, data cleaning, and business intelligence using Power Query and Power BI.**

> **Why This Project?** In real-world scenarios, data is rarely clean or analysis-ready. This project demonstrates my ability to handle messy data, make informed decisions about data quality issues, and deliver insights that drive decision-making—skills essential for any data analyst or BI developer role.

## 📋 Overview

This project showcases my ability to take raw, messy data and transform it into actionable insights. Using the Netflix Movies & TV Shows dataset (8,807 records), I performed comprehensive data cleaning, created meaningful transformations, and built interactive visualizations to answer key business questions about content trends and distribution.

## 📊 Dashboard Preview

![Netflix Analysis Dashboard](../images/dashboard_overview.png)

*Interactive Power BI dashboard featuring key metrics: 100min average duration, 5,655 movies, 2,627 TV shows, and 8,275 total content pieces. Includes geographic distribution across top 5 countries and yearly content addition trends from 2008-2021.*

## 🎯 Project Goals

**Business Question:** How can we understand Netflix's content strategy through data analysis?

**Technical Objectives:**
- Transform raw, unstructured data into analysis-ready format
- Handle missing values strategically to preserve data integrity
- Create derived metrics for deeper content insights
- Build automated data pipeline using Power Query
- Visualize findings in an interactive Power BI dashboard

**Key Results:**
- Cleaned 8,807 records with 95%+ data completeness
- Reduced data processing time through automated transformations
- Generated actionable insights on content trends and geographic distribution

## 📊 Dataset

**Source:** Netflix Movies & TV Shows Dataset  
**Records:** 8,807 entries  
**Features:** 12 columns including show_id, type, title, director, cast, country, date_added, release_year, rating, duration, listed_in, and description

## 🔧 Tools & Technologies

- **Microsoft Power Query** - Data cleaning and transformation
- **Microsoft Excel** - Data storage and initial analysis
- **Power BI** - Data visualization and dashboard creation

## 📁 Repository Structure

```
netflix-powerquery-analysis/
│
├── data/
│   └── netflix_titles_raw_data.csv     # Raw Netflix dataset
│
├── outputs/
│   ├── netflix_titles_Agregates.xlsx   # Cleaned data and summary tables
│   └── Week4_PowerBI.pbix              # Power BI dashboard
│
├── docs/
│   └── Team_WiDa_-_PowerQuery_Task_Week_4_Report.docx  # Detailed project documentation
│
├── presentations/
│   └── Power_Query_Task_Data_Cleaning_and_Analysis.pptx  # Project presentation slides
│
├── images/
│   └── dashboard_overview.png          # Dashboard screenshot for README
│
└── README.md                           # This file
```

## 🚀 Data Cleaning Process

### 1. Import & Initial Cleanup
- Loaded `netflix_titles_raw_data.csv` into Power Query
- Removed empty rows
- Converted column types:
  - `date_added` → Date
  - `release_year` → Whole Number
  - `duration` → Text (for parsing)

### 2. Handle Missing Data
- Identified null values in Director, Cast, Country, and Date Added columns
- Applied replacements:
  - `director`, `cast`, `country` → "Unknown"
  - `date_added` → Mode (most frequent value)

### 3. Split & Transform Columns
- Split `date_added` into:
  - `added_month`
  - `added_year`
- Parsed `duration` column:
  - Extracted numeric value → `duration_value`
  - Extracted unit → `duration_unit` ("Season(s)" or "Minute(s)")

### 4. Clean Text Columns
- Trimmed whitespace in: `title`, `listed_in`, `country`, `rating`
- Standardized casing (Sentence Case) for `title`

### 5. Filter & Create New Columns
- Filtered out entries with `release_year` < 2000
- Created `content_type` column:
  - "Movie" → "Film"
  - "TV Show" → "Series"

### 6. Aggregations & Insights
Generated summary statistics:
- Number of shows added per year
- Average duration for movies vs. series
- Top 5 countries by show count
- Content distribution by type
- Popular genres and ratings

## 📈 Key Findings

Through this analysis, I uncovered several interesting patterns:

**Content Strategy Insights:**
- Identified significant shift in content addition patterns post-2015, reflecting Netflix's streaming expansion
- Analyzed content type distribution to understand platform strategy (Movies vs. Series)
- Mapped geographic content production, revealing top contributing countries

**Data Quality Improvements:**
- Addressed 15-20% missing data in director, cast, and country fields
- Standardized inconsistent date formats across the dataset
- Created unified duration metrics for cross-content comparisons

**Technical Achievements:**
- Built reusable Power Query transformations for automated data refresh
- Designed interactive dashboard enabling multi-dimensional analysis
- Documented complete data pipeline for reproducibility

*See the Power BI dashboard and detailed report in the outputs folder for complete analysis.*

## 📤 Project Deliverables

This repository includes everything needed to understand and reproduce the analysis:

1. **📊 Cleaned Dataset** (`outputs/`) - Production-ready data with full documentation
2. **📈 Power BI Dashboard** (`outputs/`) - Interactive visualizations for exploration
3. **📑 Technical Documentation** (`docs/`) - Complete methodology and findings
4. **🎨 Presentation** (`presentations/`) - Executive summary of key insights
5. **💾 Raw Data** (`data/`) - Original dataset for transparency and reproducibility

Each deliverable is designed for different audiences: technical teams can review the code, stakeholders can explore the dashboard, and anyone can understand the process through documentation.

## 🎓 Skills Demonstrated

**Data Cleaning & Transformation:**
- Handling missing data with strategic imputation methods
- Text parsing and standardization across large datasets
- Date/time manipulation and feature extraction
- Data type validation and conversion

**Technical Proficiency:**
- Power Query M language for complex transformations
- Excel for data storage and preliminary analysis
- Power BI for interactive dashboard development
- Git/GitHub for version control and collaboration

**Analytical Thinking:**
- Problem decomposition and systematic approach
- Data quality assessment and validation
- Creating derived metrics for deeper insights
- Communicating findings through visualization

## 💡 What I Learned

**Technical Lessons:**
- Power Query's efficiency in automating repetitive data cleaning tasks
- Importance of documenting transformation logic for team collaboration
- Trade-offs between data completeness and accuracy when handling missing values
- Best practices for creating scalable, maintainable data pipelines

**Process Insights:**
- Starting with data exploration prevents costly mistakes later
- Clear data dictionary saves significant debugging time
- Iterative approach to transformation allows for better quality control
- Visualization reveals patterns that summary statistics miss

## 🔜 Next Steps & Potential Enhancements

**Advanced Analytics:**
- Implement sentiment analysis on content descriptions to predict viewer reception
- Build recommendation engine based on content attributes
- Create time-series forecasting for content addition trends

**Technical Improvements:**
- Automate data refresh pipeline with scheduled updates
- Add data quality monitoring and alerting
- Implement A/B testing framework for dashboard features

**Additional Insights:**
- Cross-reference with IMDb ratings and box office data
- Analyze correlation between content attributes and viewer engagement
- Geographic analysis of content availability vs. production

*These enhancements would demonstrate proficiency in machine learning, automation, and advanced analytics.*

## 👤 About

**Team WiDa**

This project demonstrates my capabilities in:
- **Data Engineering:** ETL pipeline design and implementation
- **Business Intelligence:** Translating data into actionable insights
- **Technical Documentation:** Clear communication of complex processes
- **Tool Proficiency:** Advanced Power Query, Excel, and Power BI

Completed as part of a data analytics mentorship program to strengthen real-world data skills.

---

## 📫 Connect With Me

- **LinkedIn:** [linkedin.com/in/oluwajuwonlo-wojuade](https://www.linkedin.com/in/oluwajuwonlo-wojuade-b2188023a/)
- **Email:** wojuadejuwon@gmail.com

*Feel free to explore the code, ask questions, or suggest improvements!*
