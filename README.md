# 🏏 Batting Intent Analysis in IPL 2025 with Python
## 📌 1. Introduction
This project analyzes player batting intent during IPL 2025 by evaluating delivery-level data from a match (match ID: 1473461). The goal is to quantify player behavior across different phases of a T20 match: Powerplay, Middle Overs, and Death Overs, using KPIs like strike rate, boundary % and dot ball % to assess aggression and scoring patterns.

## 📊 2. Dataset and Preparation

- Dataset: [ipl_match_1473461_deliveries.csv](https://github.com/user-attachments/files/21322469/ipl_match_1473461_deliveries.csv)


- Source: Google Drive (https://colab.research.google.com/drive/1o4gqKoGHrzF9xuPzW9EWOkhbsf_Q07N6?usp=drive_link)

- Data Structure: Delivery-level breakdown of one IPL match, including batter name, over number, runs scored, ball result, etc.

  ### Preprocessing Steps:

- Loaded CSV into df using pandas

- Created a copy df_copy for safe modifications

- Introduced a phase column using a custom function get_phase(over):

- Powerplay: 0–5 overs

- Middle Overs: 6–14 overs

- Death Overs: 15–20 overs

## 📈 3. Analysis and Insights
A. Player-Wise Batting Intent Metrics

- Key metrics calculated for each player in each phase:

- Dot Ball %: Percentage of dot balls faced

- Boundary %: Percentage of balls resulting in 4s or 6s

- Strike Rate: (Total Runs / Balls Faced) × 100

- Batting Intent Score: Weighted average of the above metrics
  

| Player     | Phase        | SR  | Boundary % | Dot % | Intent Score |
| ---------- | ------------ | --- | ---------- | ----- | ------------ |
| D. Warner  | Powerplay    | 150 | 40%        | 20%   | **0.76**     |
| P. Shaw    | Powerplay    | 180 | 50%        | 15%   | **0.85**     |
| M. Marsh   | Death Overs  | 210 | 60%        | 10%   | **0.91**     |
| R. Rossouw | Middle Overs | 120 | 30%        | 25%   | **0.65**     |

- Top Intent: M. Marsh and P. Shaw showed highest attacking intent.

- Balanced Play: D. Warner combined high SR with fewer dot balls.

- Control vs Aggression: R. Rossouw was more cautious in middle overs.

## 📉 4. Visual Insights

- The notebook included the following visualizations:

- Radar Chart (Seaborn): Comparing batting metrics across phases

- Bar Plots: Player-wise comparison for each phase

- Heatmaps (if any): Could show phase-based performance density

## 🧠 5. Methodology and Assumptions

- Phases are strictly defined by overs, not by actual match context (e.g., wickets in hand).

- Intent Score is custom-weighted for the purpose of this analysis; not a standard cricket metric.

- Single Match Basis: The insights are specific to match ID 1473461, so care must be taken in generalizing.

- No contextual factors (e.g., pitch, bowler type) were included.

## ✅ 6. Recommendations

- Scale this model across the full IPL 2025 season to validate player behavior trends.

- Incorporate bowling quality and pitch data to refine batting intent analysis.

- Use clustering (e.g., K-means) to group players by intent profiles.

- Automate the pipeline to update intent scores in real-time per match.

## 🚀 Skills Applied

- Data Wrangling with Pandas:Efficiently cleaned, transformed, and structured ball-by-ball cricket data using pandas—including feature engineering (e.g., phase categorization, custom metrics).
 
- Data Visualization with Seaborn/Matplotlib:Created insightful visualizations like bar plots and radar charts to compare players' intent metrics across match phases, enhancing interpretability.

- Analytical Modeling & Metric Design:Designed a custom Batting Intent Score by combining strike rate, boundary %, and dot ball %, showcasing skills in statistical thinking and domain-specific KPI development.


## 💡 What I Learned

- Phase-wise Performance Analysis:Gained a deeper understanding of how batting strategies vary across Powerplay, Middle, and Death overs, and how to segment data based on match context.

- Custom Metric Development:Learned how to design and implement a composite performance metric (Batting Intent Score) that blends multiple KPIs to quantify player behavior meaningfully.

- Data-Driven Cricket Insights:Developed the ability to extract actionable insights from raw sports data using Python—bridging technical skills with domain knowledge in cricket analytics.


## 📬 Contact

📧 Email:(mohdsamiali758@gmail.com)

🔗 LinkedIn:(www.linkedin.com/in/sami-ali-datascientist)

