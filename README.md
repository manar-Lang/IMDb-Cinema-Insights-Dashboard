# 🎬 IMDb Movies Dashboard – Data Analysis & Visualization

An interactive data analytics dashboard built to explore and visualize IMDb movie data, providing insights into movie ratings, trends, production volumes, and audience preferences over time.

---

## 📌 Table of Contents

- [🔎 Project Overview](#-project-overview)
- [🚧 Current Technical & Budget Constraints](#-current-technical--budget-constraints)
- [🚀 Final Goals](#-final-goals)
- [🏁 Competitors](#-competitors)
- [❗Key Technical Challenges & Roadblocks](#key-technical-challenges--roadblocks)
- [💡 Proposed Solutions](#-proposed-solutions)
- [📈 System Architecture](#-system-architecture)
- [🔧 Features](#-features)
- [🧪 Analysis Phases](#-analysis-phases)
- [🧬 Data Flow Diagram](#-data-flow-diagram)
- [🗂 Directory Structure](#-directory-structure)
- [📦 Tech Stack](#-tech-stack)
- [📊 Data Modeling Approach](#-data-modeling-approach)
- [🗓 Roadmap](#-roadmap)
- [🧾 License](#-license)
- [👨‍💻 Author](#-author)
- [📬 Future Improvements](#-future-improvements)
- [🙋‍♂️ Contributing](#-contributing)
- [📞 Contact](#-contact)

---

## 🔎 Project Overview

The IMDb Movies Dashboard is a comprehensive data analytics project that transforms raw movie data from IMDb's top 250+ movies into actionable insights through interactive visualizations. The dashboard enables users to explore:

- 🎬 **Movie Rankings**: Analysis of top-rated movies across different eras
- 📈 **Historical Trends**: Tracking rating patterns from 1921 to 2025
- 🌍 **Global Distribution**: Geographic analysis of movie production countries
- ⏱️ **Duration Analysis**: Relationship between movie length and ratings
- 🏷️ **Content Ratings**: Distribution of ratings (R, PG-13, PG, G, etc.)
- 📊 **Production Volumes**: Annual movie production trends

This enables:
- 📊 **Film enthusiasts** to discover patterns in movie ratings
- 🎓 **Researchers** to analyze cinema history and trends
- 🎥 **Content creators** to understand audience preferences
- 📈 **Business analysts** to identify market opportunities

---

## 🚧 Current Technical & Budget Constraints

This project operates within the following constraints:
- **Data Source**: Static Excel/CSV files (no live API connection to IMDb)
- **Processing**: Local data processing without cloud infrastructure
- **Budget**: No-cost tools and libraries only
- **Scale**: Analysis limited to provided dataset (top movies, not full IMDb database)
- **Update Frequency**: Manual data updates required for new movies

---

## 🚀 Final Goals

- ✅ **Data Cleaning & Preparation**: Process raw IMDb data into analysis-ready format
- ✅ **Exploratory Data Analysis**: Uncover patterns and insights in movie data
- ✅ **Interactive Dashboard**: Create user-friendly visualizations for exploration
- ✅ **Era Comparison**: Compare "Old" (pre-2000) vs "New" (2000+) movies
- ✅ **Geographic Analysis**: Map movie production by country
- ✅ **Rating Distribution**: Analyze content rating trends over time
- ✅ **Duration Impact**: Study relationship between movie length and ratings
- ✅ **Export Functionality**: Allow users to export filtered data and charts

---

## 🏁 Competitors

Several platforms and projects offer movie analytics and visualization:

- **IMDb Official Charts**: Basic top-rated lists without deep analytics
- **Box Office Mojo**: Focus on financial data, less on ratings analysis
- **The Numbers**: Detailed box office analytics with some historical data
- **Letterboxd**: Social platform with basic stats, limited analytical depth
- **Kaggle Notebooks**: Various IMDb analysis projects but not interactive dashboards
- **Tableau Public**: General visualization platform, not movie-specific

This dashboard offers:
- ✅ **Specialized Focus**: Deep dive into IMDb rating patterns
- ✅ **Era Comparison**: Unique "Old vs New" analytical lens
- ✅ **Geographic Intelligence**: Multi-country production mapping
- ✅ **Interactive Exploration**: User-driven data discovery
- ✅ **Completely Free**: No subscription or API costs

---

## ❗Key Technical Challenges & Roadblocks

- **Data Cleaning**: IMDb data requires extensive cleaning (duration format, vote counts, null values)
- **Duration Parsing**: Converting "2h 22m" format to minutes for numerical analysis
- **Geographic Data**: Handling movies with multiple countries (e.g., "USA / UK")
- **Era Classification**: Defining meaningful cutoffs for "Old" vs "New" eras
- **Rating Scale Interpretation**: Understanding the rating distribution nuances
- **Missing Data**: Handling null values in content ratings and other fields
- **Visualization Complexity**: Creating intuitive charts that tell compelling stories
- **Dashboard Performance**: Maintaining interactivity with 250+ data points

---

## 💡 Proposed Solutions

- **Robust Data Cleaning Pipeline**: Python scripts to parse and standardize all fields
- **Duration Normalization**: Convert all time formats to minutes for analysis
- **Multi-country Handling**: Split and categorize co-productions appropriately
- **Era Definition**: Use 2000 as the primary cutoff with customizable options
- **Interactive Filtering**: Allow users to filter by rating, year, country, content rating
- **Null Value Strategy**: Treat "Not Rated" and "Approved" as distinct categories
- **Responsive Design**: Optimize visualizations for different screen sizes
- **Tooltips & Explanations**: Add context to help users understand visualizations

---

## 📈 System Architecture

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│   Data Source   │────▶│  Data Processing│────▶│   Dashboard     │
│  (Excel Files)  │     │    (Python)     │     │  (Power BI/     │
└─────────────────┘     └─────────────────┘     │   Visualization)│
         │                       │               └─────────────────┘
         ▼                       ▼                        │
    ┌────────────┐         ┌────────────┐                 ▼
    │• Movies    │         │• Clean     │          ┌────────────┐
    │  Data      │         │• Transform │          │• Interactive│
    │• URLs      │         │• Enrich    │          │  Dashboards │
    │• Actress   │         │• Aggregate │          │• Reports    │
    └────────────┘         └────────────┘          └────────────┘
```

---

## 🔧 Features

- ✅ **Interactive Dashboard**: Multiple connected visualizations with filtering
- ✅ **Era Comparison**: Side-by-side analysis of Old vs New movies
- ✅ **Geographic Analysis**: World map of movie production by country
- ✅ **Rating Distribution**: Histogram and density plots of ratings
- ✅ **Temporal Trends**: Line charts showing rating changes over time
- ✅ **Duration Analysis**: Scatter plots of rating vs movie length
- ✅ **Content Rating Breakdown**: Pie/bar charts of rating categories
- ✅ **Top Movie Lists**: Dynamic ranking with filters
- ✅ **Drill-down Capability**: Click to see detailed movie information
- ✅ **Export Options**: Save filtered views and charts

---

## 🧪 Analysis Phases

<details>
<summary>✅ Phase 1: Data Collection & Understanding</summary>

**Inputs:**
- Movies Data.xlsx (3 sheets: Movies, URLS, Actress)
- IMDb metadata and structure documentation

**Process:**
1. Load Excel file with multiple sheets
2. Understand data structure and relationships
3. Identify key fields for analysis:
   - Title, Rating, Year, Duration
   - Content Rating (R, PG-13, PG, G, etc.)
   - Votes count, Country of origin
   - Actress/Cast information

**Outputs:**
- Data dictionary
- Initial data quality assessment
- Analysis requirements document

**Key Insights:**
- Dataset covers top 250+ movies from 1921-2025
- Multiple countries co-produce many films
- Content ratings vary significantly by era

</details>

<details>
<summary>✅ Phase 2: Data Cleaning & Transformation</summary>

**Inputs:**
- Raw Excel data
- Data cleaning rules

**Process:**
```python
import pandas as pd
import re

# Load data
df_movies = pd.read_excel('Movies Data.xlsx', sheet_name='Movies')

# Clean duration column
def parse_duration(duration_str):
    if pd.isna(duration_str):
        return None
    hours = re.search(r'(\d+)h', str(duration_str))
    minutes = re.search(r'(\d+)m', str(duration_str))
    total_minutes = 0
    if hours:
        total_minutes += int(hours.group(1)) * 60
    if minutes:
        total_minutes += int(minutes.group(1))
    return total_minutes

df_movies['Duration_Minutes'] = df_movies['Column6'].apply(parse_duration)

# Clean rating (remove parentheses from votes)
df_movies['Votes'] = df_movies['Column4'].str.replace(r'[\(\)M]', '', regex=True)
df_movies['Votes'] = pd.to_numeric(df_movies['Votes'], errors='coerce') * 1000000

# Rename columns
df_movies.columns = ['Rank', 'Title', 'Rating', 'Votes_Str', 'Year', 
                     'Duration_Str', 'Action1', 'Action2', 'Content_Rating']

# Add era classification
df_movies['Era'] = df_movies['Year'].apply(lambda x: 'Old' if x < 2000 else 'New')
```

**Outputs:**
- Cleaned master dataset
- Parsed duration in minutes
- Numeric vote counts
- Era classification field
- Standardized country data (from Actress sheet)

</details>

<details>
<summary>✅ Phase 3: Exploratory Data Analysis</summary>

**Inputs:**
- Cleaned dataset
- Analysis questions

**Process:**
1. **Rating Distribution Analysis**
   - Calculate average rating: ~8.3 overall
   - Distribution shape: Slightly left-skewed
   - Top rating: 9.3 (The Shawshank Redemption)

2. **Temporal Analysis**
   ```python
   # Average rating by year
   yearly_avg = df_movies.groupby('Year')['Rating'].mean()
   
   # Movie count by year
   yearly_count = df_movies.groupby('Year').size()
   ```

3. **Country Analysis**
   - Join with Actress sheet for country information
   - Count movies by country (handling multiple countries)
   - Identify top producing countries: USA, UK, France, Japan, India

4. **Content Rating Analysis**
   ```python
   rating_counts = df_movies['Content_Rating'].value_counts()
   # Top categories: R, PG-13, PG, Not Rated, Approved, G
   ```

**Outputs:**
- Statistical summaries
- Correlation findings
- Key insights for dashboard design

**Key Findings:**
- R-rated movies dominate the top list (most common rating)
- 1994 is the strongest year (multiple 9.0+ movies)
- Movie length has weak correlation with rating
- USA produces ~70% of top movies

</details>

<details>
<summary>✅ Phase 4: Dashboard Design & Development</summary>

**Inputs:**
- EDA findings
- User requirements
- Design mockups

**Process:**

### **Main Dashboard Components:**

#### **1. Go To Analysis Page**
- **Average Rating by Year**: 131.40 (average duration)
- **Top Country**: USA
- **Top Tier Cinema Rankings**: 
  - The Shawshank Redemption
  - The Godfather
  - The Dark Knight
- **Regional Contribution**: List of co-productions by country pairs
- **Global Cinematic Footprint**: Interactive world map

#### **2. Main IMDb Dashboard**
- **Current Collection Size**: 1921-2025
- **Annual Production Growth**: Bar chart by year
- **Historical Rating Trends**: Line chart (Old vs New)
- **Rating vs Movie Length**: Scatter plot with era coloring
- **Content Volume**: Pie chart (Old vs New)

#### **3. Audience Rating Density**
- Heatmap/contour plot of rating distribution
- X-axis: Rating (0-100 scale)
- Y-axis: Frequency/density
- Color legend: Orange (increase), Blue (decrease), Red (final balance)

#### **4. Cumulative Growth of Movie Library**
- Running total of movies over time
- X-axis: Year
- Y-axis: Cumulative count
- Legend: Green (increase), Yellow (decrease), Grey (final balance)

#### **5. Content Rating Distribution**
- Bar chart with legend:
  - R, PG, PG-13, Not Rated, Approved, G, Passed, NC-17
- X-axis: Rating category
- Y-axis: Count of movies

**Outputs:**
- Interactive Power BI/Tableau dashboard
- Connected visualizations with cross-filtering
- Drill-through capability for movie details

</details>

<details>
<summary>✅ Phase 5: Dashboard Implementation</summary>

**Inputs:**
- Cleaned dataset
- Dashboard design

**Process:**

### **Key Visualizations Created:**

#### **Visualization 1: Historical Rating Trends**
```
Line chart showing average rating from 1921-2025
- Blue line: Overall trend
- Shaded area: Rating range
- Annotations: Key movie releases
```

#### **Visualization 2: Rating vs Duration Scatter Plot**
```
X-axis: Duration (minutes)
Y-axis: Rating
Color: Era (Old vs New)
Size: Number of votes
Tooltip: Movie title, year, content rating
```

#### **Visualization 3: Geographic Distribution**
```
World map with:
- Bubble size: Number of movies
- Bubble color: Average rating
- Hover: Country name, movie count, top movies
```

#### **Visualization 4: Content Rating Timeline**
```
Stacked area chart showing:
- X-axis: Year
- Y-axis: Movie count
- Stacked by: Content rating (R, PG-13, etc.)
```

#### **Visualization 5: Top Movies by Era**
```
Dual bar charts:
- Left: Top 10 Old movies (pre-2000)
- Right: Top 10 New movies (2000+)
Color-coded by content rating
```

**Filters Added:**
- Country (All, USA, UK, etc.)
- Categories (Content ratings)
- Year range slider
- Minimum rating threshold
- Era toggle (Old/New/All)

**Outputs:**
- Fully functional interactive dashboard
- Connected filter pane
- Drill-through pages for movie details
- Export functionality

</details>

<details>
<summary>✅ Phase 6: Testing & Validation</summary>

**Inputs:**
- Dashboard prototype
- Test cases

**Process:**
1. **Data Accuracy Testing**
   - Verify counts match source data
   - Check rating calculations
   - Validate filter results

2. **Visualization Testing**
   - Ensure charts render correctly
   - Test interactivity (click, hover, drill-down)
   - Verify cross-filtering works

3. **Performance Testing**
   - Measure load times
   - Test with all filters applied
   - Check mobile responsiveness

4. **User Acceptance Testing**
   - Gather feedback on usability
   - Identify confusing elements
   - Document enhancement requests

**Outputs:**
- Test results document
- Bug fixes and optimizations
- User guide

</details>

<details>
<summary>✅ Phase 7: Documentation & Deployment</summary>

**Inputs:**
- Final dashboard
- Test results
- User feedback

**Process:**
1. Create user documentation
2. Document data sources and transformations
3. Prepare deployment package
4. Create presentation materials

**Outputs:**
- README file
- User guide
- Technical documentation
- Presentation slides
- Deployed dashboard (Power BI Service/Tableau Public)

</details>

---

## 🧬 Data Flow Diagram

```
┌─────────────────────────────────────────────────────────────────┐
│                         DATA SOURCES                             │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  ┌─────────────────┐    ┌─────────────────┐    ┌───────────────┐ │
│  │  Movies Sheet   │    │   URLS Sheet    │    │ Actress Sheet │ │
│  │  (250+ movies)  │    │  (Images/URLs)  │    │ (Cast/Country)│ │
│  └────────┬────────┘    └────────┬────────┘    └───────┬───────┘ │
│           │                      │                      │         │
└───────────┼──────────────────────┼──────────────────────┼─────────┘
            │                      │                      │
            ▼                      ▼                      ▼
┌─────────────────────────────────────────────────────────────────┐
│                    DATA PROCESSING LAYER                          │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  ┌─────────────────────────────────────────────────────────┐     │
│  │                  Python Pandas Scripts                   │     │
│  │  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐     │     │
│  │  │Clean Durations│ │Parse Countries│ │Calculate Era│     │     │
│  │  └─────────────┘  └─────────────┘  └─────────────┘     │     │
│  │  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐     │     │
│  │  │Handle Nulls │ │Normalize Votes│ │Merge Sheets │     │     │
│  │  └─────────────┘  └─────────────┘  └─────────────┘     │     │
│  └─────────────────────────────────────────────────────────┘     │
│                                                                   │
│                      ▼                                            │
│  ┌─────────────────────────────────────────────────────────┐     │
│  │                Cleaned Master Dataset                    │     │
│  │  - Movies with duration in minutes                       │     │
│  │  - Countries split and categorized                        │     │
│  │  - Era classification (Old/New)                          │     │
│  │  - Numeric votes and ratings                             │     │
│  └─────────────────────────────────────────────────────────┘     │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                     VISUALIZATION LAYER                           │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  ┌─────────────────────────────────────────────────────────┐     │
│  │                 Interactive Dashboard                     │     │
│  │  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐  │     │
│  │  │Rating Trends │  │Duration Scatter │ │Country Map   │  │     │
│  │  └──────────────┘  └──────────────┘  └──────────────┘  │     │
│  │  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐  │     │
│  │  │Content Rating│  │Top Movies    │  │Cumulative    │  │     │
│  │  │Distribution  │  │Lists         │  │Growth        │  │     │
│  │  └──────────────┘  └──────────────┘  └──────────────┘  │     │
│  └─────────────────────────────────────────────────────────┘     │
│                                                                   │
│                      ▼                                            │
│  ┌─────────────────────────────────────────────────────────┐     │
│  │                  Interactive Features                     │     │
│  │  - Filters (Country, Year, Rating, Content Rating)      │     │
│  │  - Drill-down to movie details                           │     │
│  │  - Cross-filtering between charts                        │     │
│  │  - Export capabilities                                   │     │
│  └─────────────────────────────────────────────────────────┘     │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                        END USERS                                  │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐           │
│  │Film Enthusiast│  │  Researcher  │  │Content Creator│           │
│  └──────────────┘  └──────────────┘  └──────────────┘           │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

---

## 🗂 Directory Structure

```
imdb_movies_dashboard/
│
├── README.md                          # Project documentation
├── requirements.txt                    # Python dependencies
├── .gitignore                          # Git ignore rules
│
├── data/
│   ├── raw/
│   │   ├── Movies Data.xlsx           # Original Excel file (3 sheets)
│   │   └── data_dictionary.md         # Field descriptions
│   ├── processed/
│   │   ├── movies_cleaned.csv         # Cleaned master dataset
│   │   ├── movies_by_country.csv      # Aggregated by country
│   │   └── movies_by_year.csv         # Aggregated by year
│   └── exports/
│       ├── top_movies_by_era.csv      # Filtered exports
│       └── rating_distribution.csv    # Rating analysis
│
├── notebooks/
│   ├── 01_data_exploration.ipynb      # Initial data exploration
│   ├── 02_data_cleaning.ipynb         # Cleaning and transformation
│   ├── 03_eda_analysis.ipynb          # Exploratory data analysis
│   └── 04_visualization_testing.ipynb # Testing visualizations
│
├── scripts/
│   ├── __init__.py
│   ├── data_loader.py                 # Load Excel data
│   ├── data_cleaner.py                 # Clean and transform
│   ├── duration_parser.py              # Parse duration strings
│   ├── country_processor.py            # Handle multi-country data
│   ├── era_classifier.py               # Add Old/New classification
│   └── export_utils.py                  # Export processed data
│
├── dashboard/
│   ├── imdb_dashboard.pbix             # Power BI file
│   ├── imdb_dashboard.twb               # Tableau file (if used)
│   ├── screenshots/
│   │   ├── main_dashboard.png          # Dashboard screenshot
│   │   ├── go_to_analysis.png          # Go To Analysis page
│   │   └── rating_analysis.png         # Rating analysis view
│   └── custom_visuals/
│       └── country_map.json             # Custom map configuration
│
├── docs/
│   ├── architecture_diagram.png        # System architecture
│   ├── data_flow_diagram.png           # Data flow diagram
│   ├── dashboard_walkthrough.md        # User guide
│   ├── technical_documentation.md      # Technical details
│   └── presentation.pptx                # Project presentation
│
├── tests/
│   ├── test_data_loader.py             # Unit tests
│   ├── test_duration_parser.py
│   └── test_country_processor.py
│
└── outputs/
    ├── insights_summary.md              # Key findings
    └── recommendations.md               # Business recommendations
```

---

## 📦 Tech Stack

| Category             | Tool / Library                | Purpose                               |
|----------------------|-------------------------------|---------------------------------------|
| **Language**         | Python 3.8+                   | Data processing and analysis          |
| **Data Processing**  | pandas, numpy                 | Data manipulation and cleaning        |
| **Data Loading**     | openpyxl, xlrd                | Excel file handling                   |
| **Data Analysis**    | pandas, numpy                 | Statistical analysis and aggregation  |
| **Visualization**    | Power BI / Tableau            | Interactive dashboard creation        |
| **Alternative Viz**  | matplotlib, seaborn           | Static charts for exploration         |
| **Geographic**       | geopandas, folium              | Map visualizations (if needed)        |
| **Development**      | Jupyter Notebooks              | Interactive development               |
| **Version Control**  | Git + GitHub                   | Code management                       |
| **Documentation**    | Markdown                       | Project documentation                 |

**Key Dependencies:**
```txt
pandas>=1.3.0
numpy>=1.21.0
openpyxl>=3.0.0
xlrd>=2.0.0
matplotlib>=3.4.0
seaborn>=0.11.0
jupyter>=1.0.0
```

---

## 📊 Data Modeling Approach

### **Data Structure**

The dataset consists of three related sheets:

#### **1. Movies Sheet (Main Fact Table)**
| Field | Description | Data Type |
|-------|-------------|-----------|
| Rank | Movie rank (1-250+) | Integer |
| Title | Movie title | String |
| Rating | IMDb rating (0-10) | Float |
| Votes_Str | Vote count with formatting | String |
| Year | Release year | Integer |
| Duration_Str | Duration in "Xh Ym" format | String |
| Content_Rating | Rating (R, PG-13, etc.) | String |

#### **2. URLS Sheet (Dimension)**
| Field | Description | Data Type |
|-------|-------------|-----------|
| Title | Movie title (join key) | String |
| Img URL | Poster image URL | String |
| Movie URL | IMDb page URL | String |

#### **3. Actress Sheet (Dimension)**
| Field | Description | Data Type |
|-------|-------------|-----------|
| Title | Movie title (join key) | String |
| Actress | Lead actress/actor | String |
| Country | Production country(s) | String |

### **Derived Fields**

| Field | Description | Calculation |
|-------|-------------|-------------|
| Duration_Minutes | Movie length in minutes | Parse "2h 22m" → 142 |
| Votes | Numeric vote count | Remove parentheses, convert "M" → million |
| Era | Time period classification | Old (<2000), New (≥2000) |
| Primary_Country | First country listed | Split "USA / UK" → "USA" |
| Country_Count | Number of co-producing countries | Count of "/" separators + 1 |

### **Aggregated Tables**

#### **Movies by Year**
```sql
SELECT 
    Year,
    COUNT(*) as Movie_Count,
    AVG(Rating) as Avg_Rating,
    AVG(Duration_Minutes) as Avg_Duration
FROM movies_cleaned
GROUP BY Year
ORDER BY Year
```

#### **Movies by Country**
```sql
SELECT 
    Country,
    COUNT(*) as Movie_Count,
    AVG(Rating) as Avg_Rating,
    LISTAGG(Title, ', ') as Top_Movies
FROM country_exploded
GROUP BY Country
ORDER BY Movie_Count DESC
```

#### **Movies by Content Rating**
```sql
SELECT 
    Content_Rating,
    COUNT(*) as Movie_Count,
    AVG(Rating) as Avg_Rating,
    MIN(Year) as First_Year,
    MAX(Year) as Last_Year
FROM movies_cleaned
GROUP BY Content_Rating
ORDER BY Movie_Count DESC
```

---

## 🗓 Roadmap

| Phase | Description | Start Date | End Date | Status |
|-------|-------------|------------|----------|--------|
| ✅ 1 | Data Collection & Understanding | 2026-02-20 | 2026-02-22 | ✅ Done |
| ✅ 2 | Data Cleaning & Transformation | 2026-02-23 | 2026-02-25 | ✅ Done |
| ✅ 3 | Exploratory Data Analysis | 2026-02-26 | 2026-02-28 | ✅ Done |
| ✅ 4 | Dashboard Design | 2026-03-01 | 2026-03-02 | ✅ Done |
| ✅ 5 | Dashboard Implementation | 2026-03-03 | 2026-03-04 | ✅ Done |
| ✅ 6 | Testing & Validation | 2026-03-05 | 2026-03-05 | ✅ Done |
| ✅ 7 | Documentation & Deployment | 2026-03-06 | 2026-03-06 | ✅ Done |

---

## 🧾 License

No license has been selected for this project yet.
All rights reserved — you may not use, copy, modify, or distribute this code without explicit permission from the author.

---

## 👨‍💻 Author

**Manar Altyp**  
*Data Analyst • BI Developer • Visualization Specialist*

🌐 [GitHub](https://github.com/manar-Lang) | 

*Project completed for: IMDb Movies Dashboard – Data Analysis & Visualization*  
*Completion Date: March 6, 2026*

---

## 📬 Future Improvements

- **Data Enrichment**
  - Connect to live IMDb API for real-time updates
  - Add box office revenue data
  - Include award wins and nominations
  - Add genre classifications
  - Include director and writer information

- **Advanced Analytics**
  - Predictive modeling for rating trends
  - Sentiment analysis of reviews
  - Network analysis of cast collaborations
  - Clustering of similar movies
  - Recommendation engine based on preferences

- **Dashboard Enhancements**
  - Mobile-optimized version
  - Custom date range comparisons
  - Animated timeline visualizations
  - Export to PDF reports
  - Scheduled data refresh

- **User Experience**
  - User accounts for saving preferences
  - Custom alert for new top movies
  - Social sharing features
  - Comparison tool (side-by-side movies)
  - Dark/light theme toggle

- **Geographic Expansion**
  - Regional analysis within countries
  - Production budget by country
  - International box office performance
  - Language distribution analysis
  - Cultural impact metrics

- **Technical Improvements**
  - Automated ETL pipeline
  - Cloud deployment (AWS/Azure)
  - API development for data access
  - Real-time collaboration features
  - Machine learning integration

---

## 🙋‍♂️ Contributing

Contributions are welcome! This is an educational project, and improvements are appreciated. Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

Please ensure your code follows PEP 8 guidelines and includes appropriate documentation.

---

## 📞 Contact

For questions, suggestions, or feedback about this project:

**Manar Altyp**
📧 Email: manaraltyp44444@gmail.com
🐙 GitHub: [Manar Altyp](https://github.com/manar-Lang)


---

## 📋 Project Requirements Checklist

| Requirement | Status | Location/Notes |
|-------------|--------|----------------|
| Data Source (Excel files) | ✅ | Movies Data.xlsx with 3 sheets |
| Data Processing (Python) | ✅ | Pandas scripts for cleaning/transformation |
| Interactive Dashboard | ✅ | Power BI/Tableau dashboard |
| Rating Analysis | ✅ | Historical trends, distribution |
| Geographic Analysis | ✅ | Country map, regional contribution |
| Era Comparison (Old/New) | ✅ | All charts include era coloring |
| Content Rating Analysis | ✅ | Distribution by rating category |
| Duration Analysis | ✅ | Scatter plot rating vs length |
| Cumulative Growth | ✅ | Movie library growth over time |
| Filters & Interactivity | ✅ | Country, year, rating, content rating |
| Screenshots of Dashboard | ✅ | /dashboard/screenshots/ |
| Data Flow Diagram | ✅ | See [Data Flow Diagram](#-data-flow-diagram) |
| Architecture Explanation | ✅ | See [System Architecture](#-system-architecture) |

---

## 📊 Key Insights Summary

| Insight | Finding |
|---------|---------|
| **Top Decade** | 1990s produced the most top-rated movies |
| **Most Common Rating** | R (40% of top movies) |
| **Top Country** | USA (70%+ of production) |
| **Average Rating** | 8.3 overall |
| **Average Duration** | 131 minutes (~2h 11m) |
| **Oldest Movie** | 1921 (The Kid) |
| **Newest Movie** | 2025 (Demon Slayer, Marty Supreme) |
| **Longest Movie** | 6h 14m (The Best of Youth) |
| **Shortest Movie** | 45m (Sherlock Jr.) |
| **Year with Most Movies** | Multiple years with 6+ entries |

---

*Last Updated: March 16, 2026*
