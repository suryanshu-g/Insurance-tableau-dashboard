# Insurance Insights: Comparative Study of Countries

An interactive Tableau dashboard for exploring insurance-market indicators across countries and comparing changes over time. The project combines an insurance dataset with country-level financial-development data to support geographical analysis, year-over-year comparisons, and historical trend exploration.

**Author:** Suryanshu Gupta  
**Project type:** Data Analytics · Business Intelligence · Tableau

## Overview

Insurance-market indicators can be difficult to compare when they are spread across multiple datasets, countries, and years. This project brings selected insurance measures into an interactive Tableau dashboard so users can explore differences between countries, view indicators in the context of country income groups, and compare a selected year with the preceding year.

The dashboard is intended for exploratory analysis and decision support. It can help identify patterns and countries for further investigation; it does not, by itself, establish market profitability or predict future performance.

## Key Features

- **Geographical view:** Displays countries on a world map and uses income group to provide financial-development context.
- **Interactive year selection:** Select a year from the workbook's available period (2006–2016) and compare it with the preceding year.
- **Dynamic metric selection:** Switch between five insurance indicators without creating a separate dashboard for each measure.
- **KPI comparison:** Shows the selected measure for the chosen period alongside the previous period.
- **Growth indicator:** Communicates whether the selected measure increased or decreased compared with the preceding year.
- **Historical trend line:** Displays how the selected indicator changes over time.
- **Income-group filtering and map interaction:** Explore a subset of countries and narrow the displayed analysis.

## Insurance Indicators

The category selector includes the following measures, using the relevant life-insurance fields available in the workbook:

1. **Life insurance share**
2. **Market share**
3. **Penetration**
4. **Ratio of reinsurance accepted**
5. **Retention ratio**

Metric definitions and units should be interpreted according to the source data. In particular, a difference between two percentage values is a **percentage-point change**; it is not the same as relative percentage growth.

## Data Sources

The repository includes two Excel workbooks:

- `Insurance_Sample_Dataset_1_.xlsx` — insurance indicators by country and year.
- `Global_Financial_Development_Database_-_Jul2018.xlsx` — country-level financial-development information, including country attributes such as region and income group.

The Tableau workbook uses **data blending** to combine information from the two sources for analysis. Country fields need to match correctly across sources; inconsistent country names, missing values, or mismatched keys can affect the results.

## Tools and Techniques

- **Tableau** — dashboard design, maps, charts, parameters, filters, calculated fields, and dashboard actions.
- **Microsoft Excel** — source data files.
- **Data blending** — combines information from separate data sources in Tableau visualizations.
- **Calculated fields and parameters** — dynamically select a metric, isolate current- and previous-year values, calculate their difference, and determine the direction of change.

This is a descriptive analytics and business-intelligence project. It does not use a trained machine-learning model.

## Repository Structure

```text
Insurance-insights--Tableau-main/
├── Insurance_insights_-_Comparative_study_of_Countries.twbx
├── Insurance_Sample_Dataset_1_.xlsx
├── Global_Financial_Development_Database_-_Jul2018.xlsx
└── README.md
```

## How to Open the Project

1. Download or clone this repository.
2. Install Tableau Desktop or use a compatible Tableau application that can open packaged workbooks.
3. Open `Insurance_insights_-_Comparative_study_of_Countries.twbx`.
4. If Tableau prompts you to locate a data source, reconnect it to the corresponding Excel file included in this repository.
5. Use the year, category, country, and income-group controls to explore the dashboard.

> **Note:** `.twbx` is a packaged Tableau workbook. The workbook and data files are provided for local exploration; the dashboard is not a live data feed and should not be assumed to contain current insurance-market figures.

## Analytical Workflow

1. Load the insurance and financial-development datasets in Tableau.
2. Blend the sources using the relevant country field.
3. Build a geographical map and configure income-group context and filtering.
4. Create year and category parameters for interactive analysis.
5. Use calculated fields to select the chosen insurance measure and isolate current- and previous-year values.
6. Compare the values in a KPI view and display the direction of change in a growth indicator.
7. Plot the selected measure over time in a trend line.
8. Validate the dashboard by comparing selected values against the source data and checking filter and parameter behavior.

## Interpreting the Year-over-Year Comparison

The workbook compares the selected year's aggregated value with the preceding year's aggregated value. Conceptually:

```text
Absolute change = Current-year value - Previous-year value
```

For example, if a metric moves from 4.2% to 4.8%, the absolute change is **+0.6 percentage points**. Relative growth would be calculated separately as `(current - previous) / previous × 100`, provided the previous value is non-zero and suitable for comparison.

## Potential Business Use

The dashboard can support questions such as:

- How do selected insurance indicators vary between countries?
- How does an indicator differ across country income groups?
- Did the selected indicator rise or fall compared with the previous year?
- Is a recent change consistent with the historical trend?
- Which countries merit further research based on the patterns observed?

These observations should be considered alongside additional evidence—such as regulation, competition, customer demand, premium growth, and operating costs—before making market-entry or investment decisions.

## Limitations

- The analysis is based on the datasets packaged with this project and is limited to their coverage, definitions, and time period.
- Country-level comparisons depend on consistent country keys and appropriate aggregation.
- A positive change in an indicator does not automatically mean a market is more profitable or commercially attractive.
- The growth comparison is an absolute difference unless relative percentage growth is explicitly calculated.
- Validate zero, missing, and unmatched values before using results for formal business decisions.

## Author

**Suryanshu Gupta**  
Tableau · Data Analytics · Business Intelligence

---

*Created as a course project to practise interactive dashboard development, data blending, calculated fields, and country-level insurance analysis.*
