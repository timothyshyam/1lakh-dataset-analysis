# 1 Lakh Customer Dataset: End-to-End Analysis

An end-to-end analysis of a 100,000-row customer dataset, covering statistical summaries, geographic and time-based trends, and a Power BI dashboard. The project focuses on what the data can and cannot support, and ends with recommendations for the decisions it can inform.

## Dataset

- **File:** `customers-100000.csv`
- **Rows and columns:** 100,000 rows, 12 columns (Index, Customer Id, First Name, Last Name, Company, City, Country, Phone 1, Phone 2, Email, Subscription Date, Website)
- **Subscription period:** 1 Jan 2020 to 29 May 2022
- **Coverage:** 243 countries and 49,154 cities

## Data Quality Checks

- No missing values in any column.
- No duplicate rows, and no duplicate Customer IDs.
- All subscription dates parsed correctly.
- Index is a row number only and was not used for analysis.

## Analysis Steps

1. **Load and inspect:** checked row count, column names, and data types.
2. **Validate:** checked missing values, duplicate rows, and duplicate IDs.
3. **Summarize by year and month:** counted monthly subscriptions for 2020 to 2022, and compared Jan to May with Jun to Dec for each year.
4. **Statistics:** calculated the mean, median, min, max, range, standard deviation, and mode of monthly subscriptions per year.
5. **Geography:** ranked countries and cities, and calculated the share held by the top 5 and top 10 countries.
6. **Dashboard:** built a Power BI report with four main pages (Executive Overview, KPI Trends, Geographic Analysis, and Decision Support), plus helper pages for DAX checks and country views.

## Key Findings

- **Volume:** 100,000 customers subscribed across the period. Subscriptions were 41,898 in 2020, 41,211 in 2021, and 16,891 in 2022.
- **2022 is partial:** the data covers only January to May 2022, so it should not be compared directly with full years.
- **Monthly pattern:** subscriptions stayed in a steady band of about 3,100 to 3,600 per month. The highest month was December 2020 (3,616), and the lowest was February 2021 (3,106).
- **Geography:** customers are spread widely. The top 10 countries account for 5,243 customers (5.24%), so no small group of countries dominates. Congo (835) and Korea (820) lead, followed by Saudi Arabia (463).
- **Cities:** no city has more than 16 customers, so city-level concentration is very low.

## Conclusion

The dataset shows steady, widely spread customer subscriptions with no clear concentration in any one country or period. Month-to-month changes are small, and the data alone cannot explain why they happen.

## Decisions and Recommendations

- **Do not use this dataset to judge profitability or market value.** It has no revenue, cost, or retention fields.
- **Add revenue and retention data** before making investment or expansion decisions, so that customer counts can be linked to business results.
- **Compare 2022 only with Jan to May of earlier years,** not with full-year totals.
- **Treat small country and city differences as noise** unless they persist over several periods.
- **Investigate the causes of monthly changes** with campaign, pricing, or seasonal data, which this dataset does not contain.

## Limitations

- The dataset contains customer records only. It does not show revenue, profit, acquisition cost, or marketing spend.
- The data covers 2020 to May 2022 only.
- The findings describe the dataset, not verified real-world business performance.

## Files

- `customers-100000.csv`: source dataset
- `Statistical_Analysis(1).xlsx`: monthly statistics by year, donut chart of top countries, and summary metrics
- `1_lakh_data_analysis.pbix`: Power BI report (Executive Overview, KPI Trends, Geographic Analysis, Decision Support, and helper pages)

## Tools

- Power BI (dashboard and DAX measures)
- Excel (statistical tables and charts)
