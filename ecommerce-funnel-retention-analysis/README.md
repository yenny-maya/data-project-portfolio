# E-commerce Funnel & Retention Analysis (MercadoLibre)

This project analyzes the conversion funnel and user retention patterns for an e-commerce product, using SQL to identify drop-off points, compare performance by country, and highlight the critical retention window after signup.

## Project Context & Goal
E-commerce growth depends not only on acquiring traffic, but also on moving users efficiently through the funnel and retaining them over time.  
The main goals of this analysis are:

- Measure conversion rates across key funnel steps.
- Identify where the largest drop-offs occur.
- Compare funnel performance by country.
- Analyze retention at key time checkpoints (D7, D14, D21, D28).
- Provide actionable recommendations to improve conversion and engagement.

## Dataset & Scope
- **Source:** Bootcamp dataset (MercadoLibre e-commerce events)
- **Period analyzed:** 01/01/2025 to 31/08/2025
- **Outputs:** Funnel conversion tables, country-level comparisons, retention summary by country, cohort retention trends.

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
- The **largest conversion drop** occurs after users select an item, suggesting friction between product interest and purchase intent.
- Conversion outcomes vary significantly across countries, supporting the need for **localized optimization strategies**.
- Retention decreases sharply after the first two weeks, indicating a **critical retention window between D7 and D14**.

## Strategic Recommendations
- Prioritize improvements in the **select_item → add_to_cart** stage, since it represents the highest loss of users and impacts all downstream funnel steps.
- Implement early **re-engagement strategies** (personalized nudges, onboarding incentives) during the first 14 days to reduce churn.
- Extend analysis with additional factors (pricing signals, shipping cost visibility, trust signals, segmentation by acquisition channel) to validate hypotheses.

## Repository Contents
- `funnel_analysis.sql` — SQL used to compute funnel metrics and conversion rates
- `retention_analysis.sql` — SQL used to compute D7/D14/D21/D28 retention and cohort trends
- `images/` — Screenshots of results, tables, and key visuals

## Visuals (Screenshots)
Add your screenshots to the `images/` folder and reference them here, for example:

- Funnel summary table  
  ![Funnel Summary](images/funnel_summary.png)

- Funnel conversion by country  
  ![Funnel by Country](images/funnel_by_country.png)

- Retention by cohort  
  ![Retention by Cohort](images/retention_cohort.png)

## Tools
- SQL (CTEs, aggregations, conditional logic)
- Google Sheets (tables and executive summary formatting)

## Next Improvements
- Publish results in a lightweight dashboard (Looker Studio / Tableau)
- Add segmentation by device type or acquisition channel (if available)
- Model uplift scenarios (e.g., +10% improvement in early funnel conversion)
