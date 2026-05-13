# 🏀 NBA Season Analysis Dashboard (2016-17)

### Project Overview
An interactive Tableau dashboard analyzing team efficiency, game pace, and regular-season 
success across the 2016-17 NBA regular season. This project evaluates 30 unique teams 
to separate volume-based success from underlying structural advantages.

### 📊 Interactive Analysis
[👉 View the Live Dashboard (Tableau Public)](https://public.tableau.com/views/_twbx_17782154814180/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

### Visual Layers
* **Regular Season Winners:** A ranked horizontal bar chart displaying top-performing teams by total wins.
* **Pace vs. SRS Scatter Plot:** A league-wide distribution mapping team game speed (Pace) against team quality using the Simple Rating System (SRS).
* **Division Standings Matrix:** A clean layout visualizing final season standings and team placements.

## 📊 Key Analytical Insights

### 1. Quality Over Speed: The SRS vs. Pace Discovery
The data demonstrates that a team's **Simple Rating System (SRS)**—their true quality—is a much stronger predictor of winning than their **Pace** (how fast they play).
*   **The Evidence:** Both the **San Antonio Spurs** (61 wins) and **Houston Rockets** (55 wins) finished in the Top 3 for both Wins and SRS, yet they played at opposite ends of the speed spectrum.
*   **Takeaway:** Success in the NBA is achievable through multiple styles; a "slow and methodical" team can be just as dominant as a "fast-paced" team as long as they maintain a high point differential.

### 2. The Golden State "Outlier"
The **Golden State Warriors** represent a rare statistical "perfect storm."
*   They led the league in **Wins (67)** and **SRS (11.35)** while playing at a blistering **Pace (~100)**. 
*   While high-speed teams often sacrifice defensive efficiency, this squad remained the most efficient team in the league while playing faster than almost everyone else.

### 🔍 Methodology
### Data Cleaning & Technical Implementation
The raw historical data sourced via Kaggle contained structural trailing artifacts, duplicate categorical entries and inconsistent string variations. The following technical optimizations were engineered directly within Tableau:

1. **String Normalization:** Handled duplicate franchise entries and removed trailing asterisk markers (`*`) from raw dimensions using targeted calculation logic:
   ```tableau
   TRIM(REPLACE([Team], "*", "")) ```

2. **Category Standardization:** Standardized team and categorical dimension naming conventions to ensure consistent filtering, grouping, and aggregation behavior across worksheets.

3. **Context Filtering:** Leveraged Tableau **Context Filters** to ensure "Top 10" calculations were applied correctly across specific season parameters.

4. **Interactive Design:** Built a coordinated dashboard where selecting a team on the bar chart instantly highlights their position on the **Pace vs. SRS Scatter Plot** and **Division    Standings** grid.

## 📖 Glossary of Metrics

*   **Simple Rating System (SRS):** A team's "report card." It measures performance based on average point differential and strength of schedule. An SRS of 0 is league average.
*   **Pace:** The estimated number of possessions per 48 minutes. It measures the "speed" or "tempo" of a team's playing style.
*   **Division Standings (1-5):** A team's rank within their specific 5-team division.
    *   *Note:* A team can have a high win total but rank 2nd in their division if they are grouped with another elite team (as seen with the Rockets and Spurs).


### Data Source
* **Kaggle Dataset:**[(A Basketball Story)](https://www.kaggle.com/code/noobiedatascientist/a-basketball-story)


