# E-commerce Funnel & Retention Analysis (SQL Case Study)

This project analyzes user behavior in an e-commerce platform (MercadoLibre case study) using SQL to identify conversion bottlenecks and retention dynamics.

## Project Context & Goal
E-commerce growth depends not only on acquiring traffic, but also on moving users efficiently through the funnel and retaining them over time.  
The main goals of this analysis are:

- Measure conversion rates across key funnel steps.
- Identify where the largest drop-offs occur.
- Compare funnel performance by country.
- Analyze retention at key time checkpoints (D7, D14, D21, D28).
- Provide actionable recommendations to improve conversion and engagement.


## Methodology (SQL)
The analysis followed these steps:

1. **Schema & data exploration** (events structure, key identifiers)
2. **Construct the end-to-end conversion funnel**
   - `page_view → view_item → add_to_cart → begin_checkout → purchase`
3. **Compute conversion rates and drop-offs**
   - Overall funnel conversion
   - Funnel conversion **by country**
4. **Retention analysis**
   - Retention at **D7, D14, D21, D28**
   - Retention comparison **by country**
   - Retention trends **by cohort (monthly)**
5. **Insights & recommendations**
   - Prioritize the most impactful funnel stage for optimization
   - Identify early re-engagement opportunities to reduce churn

## Key Insights
- The largest drop occurs between **select_item → add_to_cart**, indicating friction during product evaluation.
- Final purchase conversion is low (~1–2%), suggesting high funnel leakage.
- Conversion and retention vary significantly across countries.
- Retention drops sharply after D14, revealing a critical early churn window.

## Strategic Recommendations
- Prioritize optimization of the **select_item → add_to_cart** stage.
- Improve product page clarity (pricing, shipping, trust signals).
- Implement early re-engagement strategies before D14.
- Develop country-specific optimization strategies.

## Repository Structure
- `funnel_analysis.sql` — SQL used to compute funnel metrics and conversion rates
- `retention_analysis.sql` — SQL used to compute D7/D14/D21/D28 retention and cohort trends
- `images/` — Screenshots of results, tables, and key visuals

## Visuals (Screenshots)


- Funnel summary table  
  <img width="1657" height="877" alt="image" src="https://github.com/user-attachments/assets/fda73026-e600-4635-8f02-d14c9a15e272" />

- Funnel conversion by country  

  <img width="1687" height="1007" alt="image" src="https://github.com/user-attachments/assets/11d96f7b-3f5c-47f8-9042-5dd359a8c8e0" />

- Retention by cohort  

  <img width="1542" height="1160" alt="image" src="https://github.com/user-attachments/assets/b5914056-1d16-4e68-8c2c-d3a42055bed2" />
  
- Retention by country
  
<img width="1447" height="1167" alt="image" src="https://github.com/user-attachments/assets/0efb8d4b-08ac-4f49-b14f-712f6d215b06" />


## Tech Stack

- SQL (CTEs, aggregation, cohort analysis)
- Google Sheets (result modeling & executive summary)

This project demonstrates strong SQL skills, funnel modeling, retention analysis, and business-driven data interpretation.

## How to Run

- Load dataset (mercadolibre_funnel) into SQL environment.

- Execute funnel_analysis.sql to compute conversion metrics.

- Execute retention_analysis.sql to compute D7/D14/D21/D28 retention.

- Review outputs and visual summaries in the /images folder.
