# Video Game Sales Forecast Analysis

## Project Overview

This project analyzes historical video game sales data to identify patterns that determine a game's success and help plan future advertising campaigns for the online store Ice. The analysis focuses on identifying trends across platforms, genres, regions, and player demographics using data from 2000-2016.

## Dataset

- **Source**: Video game sales dataset containing 16,715 records
- **Time Period**: 2000-2016 (filtered to 2000-2016 for analysis)
- **Relevant Period for 2017 Forecast**: 2013-2015 (most recent and representative years)
- **Regions Covered**: North America (NA), Europe (EU), and Japan (JP)

### Data Columns
- `name`: Game title
- `platform`: Gaming platform/console
- `year_of_release`: Year the game was released
- `genre`: Game genre category
- `rating`: ESRB rating (E, T, M, etc.)
- `critic_score`: Metacritic critic score (0-100)
- `user_score`: User rating (0-10)
- `na_sales`, `eu_sales`, `jp_sales`, `other_sales`: Sales by region (in millions)
- `total_sales`: Sum of all regional sales

## Key Findings

### 1. Platform Analysis

**Top Performing Platforms (2013-2015)**:
- PS4, PS3, Xbox 360, and Xbox One dominate North America and Europe
- Nintendo 3DS leads the Japanese market
- PC maintains relatively consistent sales due to upgradeable nature

**Platform Lifecycle**:
- Average platform lifespan: ~10 years from release
- Older platforms (PS, N64, DC, PSP, GB, GBA) show significant declining sales as they become outdated
- PS2 was the strongest performer historically with ~100 million in average annual sales over 12 years

**Platform Trends**:
- Newer generation consoles show positive growth trajectories
- Older generation consoles consistently decline as newer systems are released

### 2. Genre Analysis

**Market Share (2013-2015)**:
- Action and Shooter genres control **over 50%** of market share
- Action genre: Steady leader but showing slight decline in recent years
- Shooter genre: Best performer with consistent growth
- Strategy and Puzzle genres: Least popular by sales volume

**Genre Trends**:
- Action and Shooter genres lead in both NA and EU markets
- Japan prefers Action and Role-Playing genres
- Sales remain relatively stable across years for most genres

### 3. Regional Market Characteristics

**North America & Europe**:
- Prefer console gaming (PS4, Xbox platforms)
- Favor Action and Shooter genres
- M-rated games receive the highest sales
- Highest spending regions overall

**Japan**:
- Strong preference for Nintendo platforms (3DS leads)
- Favor Action and Role-Playing genres
- Preference for T-rated games
- Lower absolute sales contribution compared to NA and EU

### 4. Review Score Impact

**On PlayStation 4 (Most Popular Platform)**:
- Critic scores correlate moderately with sales (games scoring 80-90 show highest sales)
- User scores show weaker correlation with sales
- Critical acclaim is more influential than user opinions

### 5. Cross-Platform Games

- PS4 and PS3 have the highest number of cross-platform releases
- Cross-platform availability increases total market reach and sales

### 6. Statistical Testing Results

**Hypothesis 1: Xbox One vs PC User Ratings**
- Result: No significant difference (p-value > 0.05)
- Conclusion: User ratings are similar across these platforms

**Hypothesis 2: Action vs Sports Genre User Ratings**
- Result: Significant difference found (p-value < 0.05)
- Conclusion: User ratings differ between Action and Sports genres

## Data Preparation Steps

1. **Filtered Dataset**: Selected years 2000-2016 to remove outdated entries (pre-2000 had 90%+ missing data)
2. **Data Type Conversions**: 
   - Converted `year_of_release` to integer
   - Converted `user_score` to numeric (handled "TBD" values)
3. **Missing Values Handling**:
   - Removed rows with missing `year_of_release` (essential for temporal analysis)
   - Filled missing ESRB ratings using genre-based patterns (>50% consistency)
   - Retained missing review scores (subjective per-game metric)
4. **Feature Engineering**: Created `total_sales` column combining all regional sales

## Recommendations for 2017 Marketing Strategy

Based on the comprehensive analysis:

1. **Target Regions**: Focus on North America and Europe - they contribute the highest sales volumes
2. **Platform Focus**: Prioritize PS4, Xbox One, and high-end PC platforms for primary distribution
3. **Genre Strategy**: 
   - Invest heavily in Action and Shooter games (proven market leaders)
   - Monitor Action genre decline - may need innovation
   - Consider market gaps in underperforming genres
4. **Critical Reception**: Invest in quality to achieve high critic scores (80-90 range shows peak sales)
5. **Regional Customization**:
   - NA/EU: Action and Shooter games, M-rated content
   - Japan: Role-Playing and Action games, T-rated content
6. **Cross-Platform Availability**: Develop games for multiple platforms to maximize market reach

## Project Structure

- `video_gmae_forcast.ipynb`: Complete analysis notebook with all data exploration, visualizations, and statistical tests
- `README.md`: This file with project summary and findings

## Tools & Libraries Used

- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computations
- **matplotlib & seaborn**: Data visualization
- **scipy.stats**: Statistical hypothesis testing

## Analysis Sections

1. **Step 1**: Loading and Initial Data Exploration
2. **Step 2**: Data Preparation (cleaning, type conversion, missing value handling)
3. **Step 3**: Analyzing Video Game Sales Data (temporal, platform, genre analysis)
4. **Step 4**: Regional Market Analysis and User Profiles
5. **Step 5**: Hypothesis Testing
6. **Step 6**: General Conclusions and Recommendations

---

*Last Updated: 2026*