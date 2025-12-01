# Exploring Crime Trends in Los Angeles (2020–2023)

## Overview
This project analyzes over **843,000** reported crimes in the city of Los Angeles (2020–Nov 2023) to identify temporal and spatial crime patterns, understand victim demographics, and uncover trends in solved versus unsolved cases. By performing SQL-based analysis on a star‑schema data model, we derive actionable insights for law enforcement and public safety strategies.

## Data Source
The crime data comes from the **Los Angeles Open Data Portal** ([Crime Data from 2020 to Present](https://data.lacity.org/Public-Safety/Crime-Data-from-2020-to-Present/2nrs-mtv8/about_data)). Each record includes incident date/time, location (address, latitude, longitude), offense description and code, victim age/sex/descent, and whether the case was cleared.

We transformed the raw dataset into a star schema with fact and dimension tables (FactCrime, DateDim, LocationDim, VictimDim, etc.) for efficient querying.

![Fact and Dimensions](Fact%20and%20Dimensions.jpg)

## Business Questions & Key Findings
1. **How has crime evolved over time?**  
   - Annual crime counts reveal a decline in 2020 due to pandemic restrictions, followed by a rise in 2021 and a peak in 2022, with a slight decrease in 2023 (data through October).  
   - Quarterly analysis shows seasonal fluctuations, with Q2 and Q3 typically experiencing higher crime rates.

2. **Which months experience the highest crime?**  
   - Month-wise counts for 2022 highlight **May**, **October**, and **June** as peak months, suggesting a need for targeted enforcement during those periods.

3. **Top crime types (solved vs. unsolved)**  
   - A breakdown of the ten most common crime types and their clearance rates reveals where investigative resources have been effective and where improvements are needed.

4. **Solved crimes per year**  
   - The number of cases solved dropped from **47,751** in 2020 to **29,994** in 2023, indicating increasing caseloads or resource constraints.

5. **Victim demographics**  
   - Analysis of victim age groups and top crimes affecting each group shows distinct patterns (e.g., burglary and theft prevalent among older adults, assault common among young adults).

6. **Geographic hotspots**  
   - Identifying neighborhoods with the highest and lowest crime rates supports evidence-based policing and resource allocation.

These questions are answered using SQL queries on the star schema, with results visualized in charts included in the notebook.

## Why This Matters
Understanding crime dynamics helps city officials, law enforcement, and community organizations allocate resources effectively, craft targeted interventions, and improve public safety. A robust analytical model also demonstrates the value of data engineering (building fact and dimension tables) in enabling complex analyses.

## Repository Contents
- **Los Angeles Crime Data Analytics Python .ipynb** – Jupyter notebook with ETL, dimensional modeling, exploratory analysis, and insights.
- **Los Angeles Crime Data Analytics from 2020.pdf** – PDF report summarizing the analysis.
- **Fact and Dimensions.jpg** – Diagram illustrating the star schema used.
- **README.md** – Project overview and key findings.

## Getting Started
To run the notebook yourself:

1. Clone the repository:

```bash
git clone https://github.com/BalajigowdaHS/Los_Angeles_Crime_Analytics.git
cd Los_Angeles_Crime_Analytics
```

2. Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn
```

3. Launch Jupyter and open the notebook:

```bash
jupyter notebook "Los Angeles Crime Data Analytics Python .ipynb"
```

This project demonstrates how data engineering and analytics can turn raw crime data into actionable insights for safer communities.
