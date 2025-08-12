# 🏏 Cricket Analysis & Playing XI Selection – Power BI Dashboard
📌 Overview

This project is a data-driven cricket analysis tool built in Power BI with the primary goal of selecting the optimal Playing XI for T20 cricket matches.
It uses real-world cricket statistics scraped from ESPN Cricinfo to provide actionable insights for selectors, analysts, fantasy team players, and cricket enthusiasts.

📂 Data Collection
Source

Data was collected from the ESPN Cricinfo website, which hosts comprehensive cricket match and player statistics.
Scraping Scripts

Three JavaScript-based scraping scripts were created to collect the necessary datasets:

    t20_wc_batting_summary.js

        Extracts batting statistics for all players in T20 World Cup matches.

        Fields collected: Player Name, Matches, Innings, Runs, Average, Strike Rate, 50s, 100s, etc.

    t20_wc_bowling_summary.js

        Extracts bowling statistics.

        Fields collected: Player Name, Matches, Overs, Wickets, Average, Economy, Best Figures, etc.

    t20_wc_match_results.js

        Scrapes match-level data including team scores, winners, and match conditions.

        Useful for analyzing performance against specific teams and in specific venues.

These scripts were run in a browser console on the respective ESPN Cricinfo stats pages, and the extracted data was saved as CSV/Excel files for Power BI processing.
🔄 Data Processing & Transformation

    Imported raw CSV files into Power BI Desktop.

    Performed data cleaning:

        Removed duplicates.

        Standardized player names across datasets.

        Converted text fields to numeric types where applicable.

    Created relationships between datasets (Batting ↔ Bowling ↔ Match Results).

    Used DAX for calculated columns and measures, e.g.:

        Batting Impact Score

        Bowling Efficiency Index

        All-rounder Value



📊 Dashboard Pages & Their Role in Selecting Playing XI

Dashboard Pages & Their Role in Selecting Playing XI
Main Player Analysis Page

This is the core of the dashboard — it segments players into specialized roles needed for a balanced T20 team.
Each section provides performance metrics relevant to that role, allowing for role-based selection rather than generic stat comparisons.
1. Power Hitters

    Purpose: Identify explosive batsmen for the top and middle order who can score quickly.

    Metrics: Strike rate, boundaries per innings, powerplay performance.

    Selection Use: Choose players who can maximize runs during the powerplay and accelerate in the death overs.
   



<img width="1764" height="997" alt="Screenshot 2025-08-12 180911" src="https://github.com/user-attachments/assets/c594f4d2-525a-4100-ab92-567c7703cf0e" />


2. Anchors

    Purpose: Find consistent batsmen who can stabilize the innings.

    Metrics: Batting average, consistency %, balls faced per innings, dot-ball control.

    Selection Use: Pick players who can build the innings and rotate strike effectively under pressure.
   


<img width="1762" height="1007" alt="Screenshot 2025-08-12 180916" src="https://github.com/user-attachments/assets/72b8d8d5-796d-4282-b008-1c364303a07b" />


3. Finishers

    Purpose: Identify players who excel at closing out innings.

    Metrics: Death overs strike rate, boundary %, finishing not-outs.

    Selection Use: Select batters who can chase targets or post strong finishes in the final overs.
   

   <img width="1764" height="997" alt="Screenshot 2025-08-12 180921" src="https://github.com/user-attachments/assets/7a96b413-32ef-4d75-8aef-a14d8dff7ffc" />

5. All-Rounders

    Purpose: Highlight players contributing in both batting and bowling.

    Metrics: Combined batting & bowling impact score, versatility rating.

    Selection Use: Strengthen team depth and flexibility in both innings.
   

   <img width="1790" height="1008" alt="Screenshot 2025-08-12 180926" src="https://github.com/user-attachments/assets/f6b206e3-ff1d-4ba9-91d2-e6a2650cf2fc" />

7. Specialist Fast Bowlers

    Purpose: Pinpoint pace bowlers effective in powerplay and death overs.

    Metrics: Economy rate, wickets in powerplay, yorker accuracy, death overs performance.

    Selection Use: Select wicket-taking pacers who can control runs in key overs.
   

<img width="1787" height="1007" alt="Screenshot 2025-08-12 180931" src="https://github.com/user-attachments/assets/581d62cf-aa57-4a4e-a252-d3e0e920081a" />

8. Final XI Page

   Purpose: The selection panel for locking in your Playing XI.

   Displays the chosen players by role.

   Shows team balance indicators:

   Batting depth

   Bowling overs available

   Powerplay and death overs coverage

   Selection Use: Ensures the final squad has the right mix of aggression, stability, and bowling firepower.
   


<img width="1792" height="998" alt="Screenshot 2025-08-12 180936" src="https://github.com/user-attachments/assets/fe87d63e-a220-4271-b699-351ba0099902" />



🛠️ Tech Stack

    Power BI Desktop – Data modeling & visualization.

    JavaScript – Web scraping from ESPN Cricinfo.

    Excel / CSV – Intermediate storage for raw data.

    DAX – Calculated measures and KPIs.
