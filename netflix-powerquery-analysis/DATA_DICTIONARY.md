# Data Dictionary

This document describes all fields in the Netflix dataset, both original and derived.

## Original Fields (Raw Data)

| Field Name | Data Type | Description | Example |
|------------|-----------|-------------|---------|
| `show_id` | Text | Unique identifier for each show | s1, s2, s3 |
| `type` | Text | Type of content | Movie, TV Show |
| `title` | Text | Title of the show/movie | "Stranger Things" |
| `director` | Text | Director(s) of the content | "John Doe" |
| `cast` | Text | Main cast members (comma-separated) | "Actor A, Actor B" |
| `country` | Text | Country/countries of production | "United States" |
| `date_added` | Text/Date | Date when content was added to Netflix | "September 25, 2021" |
| `release_year` | Number | Year of original release | 2020 |
| `rating` | Text | Content rating | TV-MA, PG-13, R |
| `duration` | Text | Duration of content | "90 min" or "2 Seasons" |
| `listed_in` | Text | Genres/categories | "Documentaries, Drama" |
| `description` | Text | Brief description of content | "A group of friends..." |

## Derived/Transformed Fields

### After Data Cleaning

| Field Name | Data Type | Description | Transformation Applied |
|------------|-----------|-------------|----------------------|
| `added_month` | Text | Month when content was added | Split from `date_added` |
| `added_year` | Number | Year when content was added | Split from `date_added` |
| `duration_value` | Number | Numeric value of duration | Extracted from `duration` |
| `duration_unit` | Text | Unit of duration measurement | Extracted from `duration` (Minutes/Seasons) |
| `content_type` | Text | Simplified content type | "Film" (from Movie) or "Series" (from TV Show) |

### Cleaned Text Fields

| Field Name | Cleaning Applied |
|------------|------------------|
| `title` | Trimmed whitespace, Sentence case |
| `listed_in` | Trimmed whitespace |
| `country` | Trimmed whitespace |
| `rating` | Trimmed whitespace |

### Handling Missing Values

| Field Name | Missing Value Treatment |
|------------|-------------------------|
| `director` | Replaced with "Unknown" |
| `cast` | Replaced with "Unknown" |
| `country` | Replaced with "Unknown" |
| `date_added` | Replaced with Mode (most frequent date) |

## Summary/Aggregate Fields

These fields appear in the summary tables:

| Field Name | Data Type | Description | Calculation Method |
|------------|-----------|-------------|-------------------|
| `shows_added_per_year` | Number | Count of shows added each year | GROUP BY `added_year`, COUNT(*) |
| `avg_movie_duration` | Number | Average duration of movies in minutes | AVG(`duration_value`) WHERE `type` = "Movie" |
| `avg_series_duration` | Number | Average number of seasons | AVG(`duration_value`) WHERE `type` = "TV Show" |
| `country_show_count` | Number | Number of shows per country | GROUP BY `country`, COUNT(*) |
| `top_countries` | Text | Top 5 countries by content | ORDER BY `country_show_count` DESC, LIMIT 5 |
| `movies_count` | Number | Total number of movies | COUNT WHERE `type` = "Movie" |
| `series_count` | Number | Total number of TV shows | COUNT WHERE `type` = "TV Show" |
| `total_content` | Number | Total number of entries | COUNT(*) |

## Data Quality Notes

### Filters Applied
- Removed entries with `release_year` < 2000
- Removed empty rows

### Data Type Conversions
- `date_added`: Text → Date
- `release_year`: Text → Whole Number
- `duration_value`: Text → Number

### Known Limitations
- Some shows may have multiple directors/cast members (stored as comma-separated text)
- Countries may include co-productions (multiple countries listed)
- Missing data was replaced with "Unknown" rather than removed
- Duration units are inconsistent between movies (minutes) and series (seasons)

## Example Records

### Movie Example
```
show_id: s1
type: Movie
title: Dick Johnson Is Dead
director: Kirsten Johnson
cast: 
country: United States
date_added: September 25, 2021
release_year: 2020
rating: PG-13
duration: 90 min
listed_in: Documentaries
content_type: Film
duration_value: 90
duration_unit: Minutes
```

### TV Show Example
```
show_id: s2
type: TV Show
title: Blood & Water
director: 
cast: Ama Qamata, Khosi Ngema, Gail Mabalane...
country: South Africa
date_added: September 24, 2021
release_year: 2021
rating: TV-MA
duration: 2 Seasons
listed_in: International TV Shows, TV Dramas, TV Mysteries
content_type: Series
duration_value: 2
duration_unit: Seasons
```

## Version History

- **v1.0** (Week 4) - Initial data cleaning and transformation
- Data as of: Original dataset date
- Last updated: 2026
