# Olympics Games Dashboard (1896 - 2020)

## Overview
This Olympics Games Dashboard is a comprehensive and interactive tool designed to provide detailed insights into the Olympic Games from 1896 to 2020. Built entirely using advanced Excel techniques, the dashboard allows users to explore interesting facts and statistics about the Olympics, including the performance of countries, sports, participants, and medals over the years.

By leveraging the powerful features of Excel, such as dependent dropdowns, dynamic charts, slicers, and section navigation buttons, this dashboard offers a seamless and engaging way to analyze Olympics data. Whether you are a sports enthusiast, student, researcher, or just curious about the Olympics, this dashboard makes it easy to gain knowledge and uncover hidden trends.

## Table Of Contents
1. [Overview](#overview)
2. [Key Features](#key-features)
    - Dependent Dropdowns
    - Dynamic Charts
    - Filter Section with Slicers
    - Section Navigation Buttons
    - Data Range (1896 - 2020)
3. [Data Sources](#data-sources)
    - Athletes - Summer Games
    - Athletes - Winter Games
    - Regions
4. [Data Merging and Transformation](#data-merging-and-transformation)
    - Combining Summer and Winter Games Data
    - Merging with Regions Dataset
    - Data Cleaning and Formatting
    - Creating Calculated Fields
    - Pivot Tables for Dynamic KPI and Charts
5. [Dashboard Setions](#dashboard-sections)
6. [Requirements](#requirements)
7. [Dashboard Objectives](#dashboard-objectives)
8. [How to Use the Dashboard (Video Tutorial)](#how-to-use-the-dashboard-video-tutorial)
9. [Conclusion](#conclusion)
10. [License](#license)

## Key Features
1. **Dependent Dropdowns**
    - The dashboard features intuitive dropdown menus that allow users to filter data dynamically.
    - These dropdowns are interconnected / dependent, meaning that selections in one dropdown will automatically adjust the available options in another.
    - There is a dedicated participant details section which uses those dependent dropdowns to show the details about a particular participant career in Olympics.
    - All the Key Performance Indicators (KPIs) are directly controlled by the dropdowns.

2. **Dynamic Charts**
    - Multiple dynamic charts provide visual representation of data, including trends in medal counts, athlete participation, and country performance across different Olympic years.
    - Charts adjust automatically based on user input, enabling real-time data analysis and comparison.

3. **Filter Section with Slicers**
    - A separate filter section contains slicers for easy data filtering by sport, year, country, and medal type.
    - These slicers offer a user-friendly way to interact with the dashboard, allowing quick filtering and highlighting of specific datasets.

4. **Section Navigation Buttons**
    - Custom navigation buttons enable users to move between different sections of the dashboard seamlessly.
    - Each section is dedicated to specific aspects of the Olympics, such as overall country performance, medal distributions, or sport-specific analysis.

5. **Data Range (1896 - 2020)**
    - The dashboard covers the history of the Olympic Games from 1896 to 2020, offering a long-term view of how countries, sports, and athletes have evolved.
    - Data includes medal tallies, athlete counts, participating countries, and much more.

## Data Sources
All the datasets are directly available in [Kaggle](https://www.kaggle.com/datasets/nitishsharma01/olympics-124-years-datasettill-2020).
Here is a brief description about the datasets.

1. **Athletes - Summer Games (`Athletes_summer_games.csv`):**
    
    - This dataset contains information about the athletes participating in the Summer Olympic Games.
    - Key columns likely include the athlete's name, country, sport, event, medals won (gold, silver, bronze), and the year of participation.

2. **Athletes - Winter Games (`Athletes_winter_games.csv`):**

    - This dataset holds similar information but focuses on the Winter Olympic Games.
    - Key fields likely overlap with the Summer Games data (athlete, country, event, medals) but are specific to Winter sports.

3. **Regions (`regions.csv`):**

    - This file contains regional information related to the countries or National Olympic Committees (NOCs) that participate in the Olympics.
    - It might include the mapping between NOC codes and country names or regions, helping in associating athletes with their respective countries in a consistent manner.

## Data Merging and Transformation
To build a cohesive dataset that can be used to power the dashboard, the datasets are merged and transformed as follows:

1. **Combining Summer and Winter Games Data**
    - The Summer Games and Winter Games datasets are combined into one master dataset.
    - This process involves appending the rows from both datasets while ensuring that common fields such as athlete names, countries, and medals are aligned.
    - A new column might be introduced to differentiate between Summer and Winter Games.

    **Transformation Steps:**
  
      - Use Excel's Power Query or VLOOKUP/INDEX-MATCH to merge the two datasets.
      - Ensure consistent formatting across both datasets, such as standardizing date formats, country names, and sport categories, events ,etc.

2. **Merging with the Regions Dataset**
    - The regions.csv dataset is merged with the combined Summer/Winter dataset to add additional information about the countries or regions associated with each athlete.
    - This is done using the NOC codes as a key to match the regions with athletes' countries.
    
    **Transformation Steps:**

      - A VLOOKUP or Power Query Merge function is used to join the two datasets on the NOC code.
      - Ensure there are no duplicate entries and clean any mismatched data (e.g., missing NOC codes or inconsistent country names).

3. **Data Cleaning and Formatting**
    - Once the datasets are merged, cleaning is performed to ensure consistency and accuracy. Some key steps include:
      1. Removing any duplicate rows.
      2. Handling missing data (e.g., missing medals or athlete information).
      3. tandardizing column names and formats for easier analysis.

    **Excel Techniques:**

     - Drop duplicates in excel can drop the duplicated rows
     - Conditional Formatting to highlight any missing or erroneous data.
     - Use of IFERROR and ISBLANK functions to handle empty or incorrect values.

4. **Creating Calculated Fields**
    - To enable deeper analysis in the dashboard, calculated fields or KPI cards are created. These fields might include:
        1. Total medal counts for each country or athlete.
        2. Year-wise participation trends.
        3. City at which Olympic event held at that particular year and season.
        4. Medal tally for each Olympic event (gold, silver, bronze breakdown) and so on...
    - Calculated fields are created using Excel formulas, pivot tables, or data analysis expressions (DAX).

5. **Pivot Tables for Dynamic Analysis**
    - Using Pivot Tables, the cleaned and merged dataset is summarized to create insights.
    - Pivot Tables are ideal for dynamically aggregating data such as medal counts by country, participation rates by year, or medal breakdowns by sport.
    - Pivot tables are also used as the source of data for each charts in the dashboard which shows the true power of pivot tables.

## Dashboard Sections
1. **First Section** : Consists of dropdowns, slicers, KPIs and dedicated participant details section ![image](Assets/First%20Page.png)
2. **Second Section** : Consists of a country-slicer and country-performance charts ![image](Assets/Second%20Page.png)
3. **Third Section** : Consists of country-participants and their percentage charts ![image](Assets/Third%20Page.png)
4. **Fourth Section** : Consists of yearwise-charts such as medal count and age comparision ![image](Assets/Fourth%20Page.png)
5. **Fifth Section** : Consists of some other important charts such as genderwise medals count, popular sports, medals count by season, etc. ![image](Assets/Fifth%20Page.png)![image](Assets/Sixth%20Page.png)

## Requirements
- Microsoft Excel 365 (recommended)
- Basic familiarity with Excel navigation and functionality

## Dashboard Objectives
- **Explore Medal Trends:** Track the performance of different countries and identify top-performing nations over the years.
- **Analyze Athlete Participation:** Get insights into athlete participation rates across different sports and Olympics and its seasons.
- **Compare Countries:** Easily compare how different countries have performed in terms of medal counts and participation in various sports.
- **Examine Sport-Specific Data:** Analyze trends within specific sports, such as which countries dominate certain disciplines.
- **Discover Fun Facts:** Uncover interesting and lesser-known facts about the Olympics, such as historical milestones, records, and unique events in each sports.
- **Learning Purposes:** If you want to learn more about Olympic games, you are definitely at the right place. 

## How to Use the Dashboard (Video Tutorial)
***Click on it to watch the entire tutorial.***
[![Watch the video](https://img.youtube.com/vi/gWVdVq3XTNA/maxresdefault.jpg)](https://youtu.be/gWVdVq3XTNA)

## Conclusion
This Olympics Games Dashboard offers a powerful yet easy-to-use tool for exploring over a century of Olympic history. Whether you are conducting research, presenting data, or simply satisfying your curiosity about the Games, this dashboard brings the data to life through intuitive, interactive features and visually appealing charts.

If you are a fan of sports analytics, Excel-based dashboards, or interactive data visualization, this project must be super interesting to look at!

## License
This project is licensed under the MIT License - see the [LICENSE](https://github.com/LinconDash/Olympics-Games-Dashboard/blob/master/LICENSE) file for details.

