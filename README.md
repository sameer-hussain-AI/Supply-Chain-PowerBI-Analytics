
# Supply Chain Analytics Dashboard | Power BI

**An interactive business intelligence report for analysing sales performance, profitability, regional contribution, product performance, and trends over time.**

This project uses Microsoft Power BI to organise business performance metrics into a set of connected report pages. The dashboard supports both high-level monitoring and focused exploration, allowing users to move from an executive overview into regional, product, category, and time-based analysis.

> **Project type:** Business Intelligence · Data Analytics  
> **Primary tool:** Microsoft Power BI Desktop  
> **Report file:** `SupplyChainProjectBi.pbix`

---

## Table of Contents

- [Project Overview](#project-overview)
- [Business Problem](#business-problem)
- [Project Objectives](#project-objectives)
- [Dashboard Walkthrough](#dashboard-walkthrough)
- [Key Performance Indicators](#key-performance-indicators)
- [Analytical Workflow](#analytical-workflow)
- [Technical Implementation](#technical-implementation)
- [How to Explore the Report](#how-to-explore-the-report)
- [Repository Structure](#repository-structure)
- [Tools and Skills Demonstrated](#tools-and-skills-demonstrated)
- [Business Insights and Recommendations](#business-insights-and-recommendations)
- [Assumptions and Limitations](#assumptions-and-limitations)
- [Future Improvements](#future-improvements)
- [Author](#author)

---

## Project Overview

Business data becomes more useful when stakeholders can interpret it quickly and investigate the factors behind performance. This project presents a Power BI dashboard that brings core sales and profitability indicators together with regional comparisons, product-level analysis, category breakdowns, and time-series views.

Rather than treating each chart as a standalone visual, the report is organised into pages that serve different analytical purposes:

- **Monitor:** Review the headline performance indicators.
- **Compare:** Examine differences between regions, products, and categories.
- **Investigate:** Use available filters and selections to focus on a particular segment.
- **Track:** Review yearly patterns in sales and order volume.

The report is intended as an exploratory business intelligence tool. It helps users identify areas for further investigation; business conclusions should be supported by the underlying data and the definitions used in the report.

## Business Problem

A business may have sales records available but still lack a clear, connected view of its performance. Reviewing figures separately can make it harder to compare sales with profit, understand regional contribution, identify product-level differences, or recognise changes over time.

This dashboard addresses that reporting challenge by bringing several performance perspectives into one interactive Power BI report.

### Questions the dashboard is designed to investigate

1. What are the overall sales, profit, order volume, and quantity?
2. How does sales performance differ across regions?
3. Which products contribute the most to sales and profit?
4. How do product categories compare across key performance measures?
5. How do sales and order volume change from year to year?
6. Does the view change when a user selects a specific region or business segment?
7. Which areas should be examined further before making an operational decision?

## Project Objectives

- Present key performance indicators in a clear executive-level view.
- Make regional sales comparisons easier to interpret.
- Compare product performance using both sales and profitability measures.
- Summarise performance at category level.
- Provide a time-based view of sales and order-volume patterns.
- Enable interactive exploration through available report filters and selections.
- Demonstrate practical Power BI report design and business-focused data visualisation.

---

## Dashboard Walkthrough

The report contains six pages, each with a distinct purpose.

### 1. Executive Overview

**Purpose:** Provide a quick, high-level summary of business performance.

The overview brings core metrics and summary visuals into one place, helping users understand the overall picture before exploring specific segments.

**Metrics and visuals include:**

- Total Sales
- Total Profit
- Total Orders
- Quantity
- Profit Margin
- Regional sales distribution
- Sales trend
- Product and category visuals

**How to use it:** Start here to review the headline indicators. Then move to a more focused page when you want to investigate a particular aspect of performance.

![Executive Overview](images/executive-overview.png)

### 2. Regional Performance

**Purpose:** Compare sales contribution across regions.

This page focuses on geographic differences in sales and includes regional filtering to support a more focused view.

**Questions to explore:**

- Which regions show the highest sales in the current report context?
- How does the comparison change when a region is selected?
- Which regions may deserve a closer review?

![Regional Performance](images/regional-performance.png)

### 3. Product Analysis

**Purpose:** Explore product-level sales and profit contribution.

The product view compares products using sales and profit visuals. Considering both measures is useful because a product with high sales is not necessarily the product with the highest profit.

**Questions to explore:**

- Which products rank highest by sales?
- Do the highest-sales products also lead in profit?
- Which products may need further profitability analysis?

![Product Analysis](images/product-analysis.png)

### 4. Categorical Analysis

**Purpose:** Compare performance across product categories.

This page summarises sales and profit at category level and provides a visual view of category contribution.

**Questions to explore:**

- How do categories compare in sales?
- Does profit contribution follow the same pattern as sales?
- Which category differences deserve further investigation?

![Categorical Analysis](images/categorical-analysis.png)

### 5. Time Series

**Purpose:** Examine how performance changes over time.

The time-series page includes yearly sales and order-volume trends, with regional filtering available for focused analysis.

**Questions to explore:**

- How does sales performance change between years?
- Does order volume follow a similar pattern to sales?
- Are there periods that merit additional investigation?
- Does the trend differ for a selected region?

![Time Series](images/time-series.png)

### 6. DAX Measures

**Purpose:** Surface the report's core calculated performance measures.

This page presents the main measures used in the report, including the core sales, profit, order, quantity, margin, and average-order metrics.

**Why it matters:** Clearly defined measures help keep recurring business indicators consistent across report visuals. Their exact formulas should be documented alongside the report's metric definitions.

![DAX Measures](images/dax-measures.png)

> **Screenshot note:** Add your actual dashboard screenshots to an `images/` folder using the filenames shown above. Until you add these files, the images will not render on GitHub.

---

## Key Performance Indicators

The report uses a set of headline measures to summarise business performance.

| KPI | Business interpretation | Analytical use |
|---|---|---|
| **Total Sales** | Overall sales value in the current filter context | Monitor sales and compare segments |
| **Total Profit** | Overall profit in the current filter context | Review profit contribution |
| **Total Orders** | Order volume according to the report's measure definition | Understand order activity |
| **Quantity** | Total quantity represented by the selected records | Review quantity sold or recorded |
| **Profit Margin** | A calculated profitability ratio | Compare profitability relative to sales |
| **Average Order** | An order-level performance measure | Review average order performance |

**Important:** These descriptions explain the business purpose of each KPI, not the exact DAX implementation. Check the actual formulas in Power BI before publishing formula-level documentation. In particular, confirm whether `Total Orders` counts distinct order IDs and how `Average Order` is calculated.

### Why sales and profit should be viewed together

Sales alone do not provide a complete picture of business performance. A segment may generate substantial sales without having the strongest profit contribution. Comparing sales, profit, and profit margin gives a more useful starting point for further investigation.

---

## Analytical Workflow

The report follows a practical business intelligence workflow.

### 1. Executive monitoring

Begin with the summary KPIs to establish an overview of the business. Use this page to identify which metrics or segments need closer examination.

### 2. Regional comparison

Move to the regional page to compare geographic sales contribution. Apply the available regional filter to focus on a selected segment.

### 3. Product evaluation

Review product-level sales and profit visuals. Compare rankings across the measures instead of assuming that the highest-sales product is automatically the most profitable.

### 4. Category comparison

Use the category page to compare sales and profit contribution across product groups. Differences between these measures can guide further analysis.

### 5. Trend exploration

Use the time-series page to review yearly sales and order-volume patterns. Treat visible changes as prompts for investigation rather than proof of a cause.

### 6. Metric review

Use the DAX Measures page and the model's measure definitions to confirm how headline metrics are calculated and interpreted.

---

## Technical Implementation

### Power BI report design

The report is built in Microsoft Power BI Desktop and uses multiple pages to separate executive reporting from more focused analysis.

### Measures and calculations

The report includes measures named:

- `Total Sales`
- `Total Profit`
- `Total Orders`
- `Quantity`
- `Profit Margin`
- `Average Order`

These measures support the report's KPI cards and other visuals. Review the actual DAX expressions in the PBIX file before documenting exact formulas or claiming a specific calculation method.

### Visualisation choices

The report uses several visual types to support different analytical tasks:

- **KPI cards:** Show headline metrics.
- **Bar and column charts:** Compare regions, products, and categories.
- **Line charts:** Show changes over time.
- **Pie charts:** Show a part-to-whole breakdown.
- **Treemaps:** Provide a compact view of relative contribution.

Each visual should be interpreted in the context of its title, measure, aggregation, and active filters.

### Filtering and interaction

Available slicers and report selections let users focus the analysis on a selected region or other supported segment. Because filter context can change KPI values, comparisons should be made using consistent selections.

---

## How to Explore the Report

1. Download or clone this repository.
2. Open `SupplyChainProjectBi.pbix` in Microsoft Power BI Desktop.
3. Navigate to **Executive Overview** for the initial summary.
4. Review the KPI cards and summary visuals.
5. Open **Regional Performance** to compare geographic contribution.
6. Open **Product Analysis** and **Categorical Analysis** to explore sales and profit at a more detailed level.
7. Use **Time Series** to review yearly patterns.
8. Open **DAX Measures** when you want to review the report's core metrics.
9. Use the available slicers and selections to investigate a segment, then clear them to return to the broader view.

### Requirements

- A computer capable of running Microsoft Power BI Desktop.
- The `SupplyChainProjectBi.pbix` report file.
- Access to any external data source or credentials if the report requires them after opening. Confirm data-source settings in Power BI if a refresh is needed.

---

## Repository Structure

```text
SupplyChain-Analytics/
│
├── SupplyChainProjectBi.pbix
├── README.md
└── images/
    ├── executive-overview.png
    ├── regional-performance.png
    ├── product-analysis.png
    ├── categorical-analysis.png
    ├── time-series.png
    └── dax-measures.png
```

The `images/` folder is optional. Create it and add your own screenshots if you want the report pages to appear in the GitHub README. Until those images are added, the suggested image paths will not render.

## Tools and Skills Demonstrated

| Tool or skill | Application in this project |
|---|---|
| **Microsoft Power BI Desktop** | Building a multi-page interactive report |
| **DAX** | Creating and using business performance measures |
| **Data visualisation** | Choosing charts to compare values, contributions, and trends |
| **KPI reporting** | Presenting core business indicators |
| **Business analysis** | Structuring visuals around practical business questions |
| **Interactive reporting** | Exploring selected segments through filters and selections |

---

## Business Insights and Recommendations

A strong dashboard project should explain what the data reveals, not only which charts it contains. The report can be used to investigate the following areas.

### Areas to investigate

- **Regional performance:** Identify the regions with the highest and lowest sales in a consistent filter context.
- **Sales versus profit:** Compare sales rankings with profit rankings to identify differences in contribution.
- **Category contribution:** Examine which categories account for the largest shares of sales and profit.
- **Time-based changes:** Investigate year-to-year increases or decreases in sales and order volume.
- **Order-level performance:** Review the exact definition of Average Order before interpreting differences between segments.

### Recommendations for completing this section

Before publishing the final portfolio version, add three to five findings directly supported by your report. For each finding, state the metric, the relevant comparison or period, the observed result, and why it matters.

Use this structure after verifying the numbers:

> **Finding:** [Describe a verified pattern in the report.]  
> **Evidence:** [Add the actual metric, values, and comparison period or segment.]  
> **Business implication:** [Explain why the pattern may matter.]  
> **Suggested next step:** [Recommend a follow-up analysis or action.]

No numerical findings are asserted here because they must be read and validated against the actual report data. This keeps the project documentation accurate rather than presenting invented results as business conclusions.

---

## Assumptions and Limitations

- The report contains six pages covering executive, regional, product, category, time-series, and measure views.
- The available model table is named `Table1`; verify the underlying fields and data-source details in Power BI before describing the full data model.
- The exact formulas for the listed KPIs should be checked in the PBIX file.
- Data-cleaning steps, missing-value treatment, source coverage, and refresh procedures should only be documented after they have been verified.
- A visible trend or difference does not, by itself, establish the reason behind that result.
- KPI values can change with filter selections, so comparisons require a consistent context.
- This repository documents the report; it does not claim that the dashboard alone validates operational or financial decisions.

---

## Future Improvements

Potential improvements for a future version include:

- Add screenshots of every report page to the GitHub README.
- Add a dedicated insights page with quantified, evidence-backed findings.
- Document the DAX formulas and definitions for each KPI.
- Describe the source dataset, field meanings, and any verified data-cleaning steps.
- Add more granular date filtering if supported by the underlying data.
- Document data-quality checks, assumptions, and metric limitations.
- Include a short report walkthrough or demonstration video.
- Review accessibility, visual consistency, and slicer behaviour across pages.

---

## Author

**Sameer Hussain**  
Aspiring Data Analyst | Power BI · Python · Excel · SQL · AI

This project demonstrates a practical approach to business intelligence: presenting core metrics, structuring an interactive report around business questions, and enabling focused analysis of regional, product, category, and time-based performance.

---

*Built with Microsoft Power BI Desktop.*
