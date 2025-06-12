
# Employee Engagement Analysis

## Problem Statement

The Seattle Department of Public Works recently conducted an internal survey to assess job satisfaction and employee engagement across its 21 departments. Despite collecting over 14,500 individual responses from approximately 1,500 staff members, the HR team lacked a clear, actionable understanding of the results. Raw survey data was inconsistent, unstructured, and difficult to interpret.

As a newly hired Human Capital Analyst, my task to transform this complex dataset into a clean, visual, and insight-driven analysis. The goal was to uncover key drivers of employee satisfaction, identify areas of concern, and support data-informed recommendations to improve morale, motivation, and retention across the workforce.

## 📊 Objectives

1. **Explore & profile the data** to identify and fix data quality issues.
2. **Prepare and reformat** the survey results for visual analysis.
3. **Visualise the responses** and provide actionable HR recommendations.

## 📁 Contents

| Folder | Description | File |
|--------|-------------|------|
| `data/` | Raw survey data (.xlsx) | [HR Employee Survey Responses.xlsx](https://github.com/folakeobalakun/Employee-Engagement-Analysis/blob/main/HR%20Employee%20Survey%20Responses.xlsx) |
| `visuals/` | Final stacked bar chart visualization | [Survey.png](https://github.com/folakeobalakun/Employee-Engagement-Analysis/blob/main/Survey.png) |
| `analysis/` | Cleaned & prepared analysis Excel file | [Analysis.xlsx](https://github.com/folakeobalakun/Employee-Engagement-Analysis/blob/main/Analysis.xlsx) |
| `scripts/` | List of Excel formulas and data cleaning steps | [formulas_used.md](https://github.com/folakeobalakun/Employee-Engagement-Analysis/blob/main/formulas_used.md) |



## Data Profiling and QA
The Excel file contains two primary tabs: one with the raw data (survey responses) and another with a data dictionary. Filtering techniques were used to explore columns, revealing inconsistencies such as two variations of Question 7 and blank values in Column J.
Key profiling metrics such as MIN, MAX, COUNT, and BLANKS were calculated for numerical columns B, E, F, G, H, and J. The 'Response' column had 14590 entries with 153 blanks. Blank rows were removed, and duplicate records (15 in total) were dropped, leaving 14,575 valid responses.
Pivot tables were used to analyze Department and Question field frequencies. There were 21 departments, with 'Planning and Public Works' having the most responses (4,663), and 'Family Justice Center' the fewest (39). Inconsistencies like 'and' vs '&' in questions were standardized using Find & Replace and TRIM functions.

## 📈 Data Preparation
A Chart Source tab was created. Unique survey questions were extracted using the UNIQUE function. Response counts for values 1 through 4 were calculated using COUNTIFS, and averages were computed using AVERAGEIFS, excluding zeros. Percentages of each response type were calculated based on total responses. This data was then copied as values and sorted descending by average response.
Top-rated question: 'I know what is expected of me at work'. Lowest-rated question: 'I have a best friend at work'.

## 📊 Visualisation
A 100% stacked bar chart was created to visualize survey responses. Colors were used to differentiate sentiment: shades of red/orange for negative (1,2) and shades of blue for positive (3,4). X-axis, title, and gridlines were removed to improve readability



![Survey Dashboard](https://github.com/folakeobalakun/Employee-Engagement-Analysis/blob/main/Survey.png)

## Insights
- Top-rated question is "I know what is expected of me at work" which means employees feel clear about their job roles and are supported by their supervisors, this suggests strong leadership alignment and communication on expectations.
- The lowest engagement areas relate to recognition, peer connection, and accountability—common drivers of long-term satisfaction and team performance.
- Departments with the most response are Family Justice Center, Emergency Management, Exec Office & Directors	, Communications Office and Human Resources. These departments are seen as engaged and supportive environments potential models for best practices.

## Recommendations
- Boost Peer Relationships: The low score for “I have a best friend at work” signals a lack of social connection. HR could promote inter department networking events or mentorship programs.
- Enhance Recognition Programs: Employees don’t feel regularly recognized. Implement lightweight recognition tools like peer nominated shoutouts or manager dashboards for timely feedback.
- Improve Accountability Culture: The relatively low response on supervisor accountability may indicate a lack of follow through on performance standards. Targeted training for mid level managers may help here.
- Scale What Works: Replicate leadership, recognition, and communication practices from top performing departments like  Family Justice Center and Emergency Management across the organisation.
