# Employee-Engagement-Analysis
Excel based analysis of HR survey data to support workforce engagement decisions.
## Problem Statement

The Seattle Department of Public Works recently conducted an internal survey to assess job satisfaction and employee engagement across its 21 departments. Despite collecting over 14,500 individual responses from approximately 1,500 staff members, the HR team lacked a clear, actionable understanding of the results. Raw survey data was inconsistent, unstructured, and difficult to interpret.

As a newly hired Human Capital Analyst, my task to transform this complex dataset into a clean, visual, and insight-driven analysis. The goal was to uncover key drivers of employee satisfaction, identify areas of concern, and support data-informed recommendations to improve morale, motivation, and retention across the workforce.

## 📊 Objectives

1. **Explore & profile the data** to identify and fix data quality issues.
2. **Prepare and reformat** the survey results for visual analysis.
3. **Visualise the responses** and provide actionable HR recommendations.

## 📁 Contents

| Folder | Description |
|--------|-------------|
| `data/` | Raw survey data (.xlsx) |
| `visuals/` | Final stacked bar chart visualization |
| `docs/` | Word-based project summary |
| `scripts/` | List of Excel formulas and data cleaning steps |

## Data Profiling and QA
The Excel file contains two primary tabs: one with the raw data (survey responses) and another with a data dictionary. Filtering techniques were used to explore columns, revealing inconsistencies such as two variations of Question 7 and blank values in Column J.
Key profiling metrics such as MIN, MAX, COUNT, and BLANKS were calculated for numerical columns B, E, F, G, H, and J. The 'Response' column had 14590 entries with 153 blanks. Blank rows were removed, and duplicate records (15 in total) were dropped, leaving 14,575 valid responses.
Pivot tables were used to analyze Department and Question field frequencies. There were 21 departments, with 'Planning and Public Works' having the most responses (4,663), and 'Family Justice Center' the fewest (39). Inconsistencies like 'and' vs '&' in questions were standardized using Find & Replace and TRIM functions.

## 📈 Data Preparation
A Chart Source tab was created. Unique survey questions were extracted using the UNIQUE function. Response counts for values 1 through 4 were calculated using COUNTIFS, and averages were computed using AVERAGEIFS, excluding zeros. Percentages of each response type were calculated based on total responses. This data was then copied as values and sorted descending by average response.
Top-rated question: 'I know what is expected of me at work'. Lowest-rated question: 'I have a best friend at work'.

## 📊 Visualization
A 100% stacked bar chart was created to visualize survey responses. Colors were used to differentiate sentiment: shades of red/orange for negative (1,2) and shades of blue for positive (3,4). X-axis, title, and gridlines were removed to improve readability



![Survey Dashboard](https://github.com/folakeobalakun/Employee-Engagement-Analysis/blob/main/Survey.png)
