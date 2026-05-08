# 2016-17 NBA Season: Team Performance Dashboard

An interactive Tableau dashboard analyzing team efficiency, game pace, and regular-season 
success across the 2016-17 NBA regular season. This project evaluates 30 unique teams 
to separate volume-based success from underlying structural advantages.

👉 [View the Interactive Dashboard on Tableau Public] (https://public.tableau.com/views/_twbx_17782154814180/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link))

### Visual Layers
* **Regular Season Winners:** A ranked horizontal bar chart displaying top-performing teams by total wins.
* **Pace vs. SRS Scatter Plot:** A league-wide distribution mapping team game speed (Pace) against team quality using the Simple Rating System (SRS).
* **Division Standings Matrix:** A clean layout visualizing final season standings and team placements.

### Data Cleaning & Technical Implementation
The raw historical data sourced via Kaggle contained structural trailing artifacts, duplicate categorical entries and inconsistent string variations. The following technical optimizations were engineered directly within Tableau:

1. **String Normalization:** Handled duplicate franchise entries and removed trailing asterisk markers (`*`) from raw dimensions using targeted calculation logic:
   ```tableau
   TRIM(REPLACE([Team], "*", "")) ```

2. **Category Standardization:** Standardized team and categorical dimension naming conventions to ensure consistent filtering, grouping, and aggregation behavior across worksheets.
3. **Data Validation:** Verified that cleaned dimension values propagated consistently throughout all visualizations, calculations, and dashboard filters.
4. **Calculated Field Engineering:** Built calculated fields to support dynamic metric analysis, custom aggregations, and interactive dashboard functionality.
5. **Dashboard Actions & Scoping:** Configured global filtering cards across multiple worksheets to ensure seamless cross-chart interaction and synchronized data state.
6. **Interactive Dashboard Architecture:** Implemented cross-worksheet filtering and dashboard actions to improve exploratory analysis and user navigation.
7. **KPI Integration:** Embedded KPI summary cards to surface high-level performance indicators and key analytical takeaways.
8. **Responsive Dashboard Design:** Configured dashboard sizing and layout behavior for improved desktop and mobile viewing compatibility.
9. **Presentation & Formatting Optimization:** Applied custom formatting, layout alignment, and visual hierarchy adjustments to improve readability and dashboard usability.
10. **Workflow Organization:** Structured worksheets and dashboard components into a cohesive analytical workflow for streamlined end-user interaction.


### How to Run Locally
1. Clone this repository to your machine.
2. Ensure you have **Tableau Desktop** or **Tableau Public (Free)** installed.
3. Open the `.twbx` packaged workbook file included in this repository to explore the data extraction and underlying calculated fields.
