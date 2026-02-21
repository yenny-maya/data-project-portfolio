# E-commerce Funnel & Retention Analysis (SQL Case Study)

This project analyzes user behavior in an e-commerce platform (MercadoLibre case study) using SQL.  
The objective is to identify conversion bottlenecks, retention patterns, and high-impact optimization opportunities.

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
2. **Build the conversion funnel**
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
  

- Funnel conversion by country  
  

- Retention by cohort  
  

## Tech Stack

- SQL (CTEs, aggregation, cohort analysis)
- Google Sheets (result modeling & executive summary)

This project demonstrates strong SQL skills, funnel modeling, retention analysis, and business-driven data interpretation.
