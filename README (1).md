# Steph Curry 2020–2021 NBA Season Performance Analysis

## Project Overview

This project analyzes Steph Curry's game-by-game statistics from the 2020–2021 NBA season to identify what factors drive his scoring output and how his individual performance relates to Golden State Warriors win/loss outcomes. The analysis is intended to provide insights useful for game strategy and player evaluation.

The dataset covers 28 games played between December 2020 and February 2021, spanning 20 different opponents across home and away games. Over this stretch, Curry averaged **30.1 points** and **5.0 three-pointers** per game.

---

## Business Questions

1. How does Curry's scoring and shooting efficiency vary by month throughout the season?
2. Does playing at home vs. away affect his performance and the team's win rate?
3. Which shooting categories (FG%, 3P%, FT%) most strongly correlate with winning?
4. How do his minutes played relate to points scored and overall team success?
5. What does his plus/minus (P/M) reveal about his impact on game outcomes?
6. How do his assists and turnovers relate to wins and losses?

---

## Repository Structure

```
steph-curry-analysis/
│
├── README.md                            # Project overview (this file)
├── steph_curry_analysis.ipynb           # Jupyter Notebook — full analysis & visualizations
├── Steph_Curry_Capstone_Report.pdf      # Final written report (PDF)
├── Steph_Curry_Capstone_Report.docx     # Final written report (Word)
│
├── data/
│   └── stephcurry2020-2021.xlsx         # Raw dataset
│
└── visualizations/
    ├── fig1_scoring_trend.png           # Points per game with rolling average
    ├── fig2_shooting_by_month.png       # FG%, 3P%, FT% by month
    ├── fig3_home_vs_away.png            # Home vs. away comparison
    ├── fig4_correlations.png            # Correlation rankings
    └── fig5_boxplots.png                # Win vs. loss distributions
```

---

## Dataset

**File:** `data/stephcurry2020-2021.xlsx`

**Source:** [Kaggle — Steph Curry 2020–2021 Game Log](https://www.kaggle.com/datasets)

**Description:** Game-by-game statistics for Stephen Curry during the 2020–2021 NBA regular season. Each row represents one game.

| Column | Description |
|--------|-------------|
| `OPP` | Opponent team abbreviation |
| `WEEK` | Week number of the season |
| `MONTH` | Month the game was played (DEC, JAN, FEB) |
| `MIN` | Minutes played |
| `FGM / FGA / FG%` | Field goals made, attempted, percentage |
| `3PM / 3PA / 3P%` | Three-pointers made, attempted, percentage |
| `FTM / FTA / FT%` | Free throws made, attempted, percentage |
| `OREB / DREB / REB` | Offensive, defensive, and total rebounds |
| `AST` | Assists |
| `STL` | Steals |
| `BLK` | Blocks |
| `TO` | Turnovers |
| `PF` | Personal fouls |
| `PTS` | Points scored |
| `P/M` | Plus/minus (point differential while Curry was on court) |
| `RESULT` | Game result (1 = Win, 0 = Loss) |
| `SCOREGS` | Golden State Warriors final score |
| `SCOREOPP` | Opponent final score |
| `COURT` | Home (H) or Away (A) |

**Quick Stats:**
- Games: 28 (15 wins, 13 losses)
- Scoring range: 11–62 points per game
- Months covered: December 2020, January 2021, February 2021
- Opponents: 20 unique teams

---

## How to Run the Notebook

### Requirements

- Python 3.8+
- Jupyter Notebook or JupyterLab

### Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/steph-curry-analysis.git
   cd steph-curry-analysis
   ```

2. **Install dependencies:**
   ```bash
   pip install pandas numpy matplotlib openpyxl jupyter
   ```

3. **Launch the notebook:**
   ```bash
   jupyter notebook steph_curry_analysis.ipynb
   ```

4. **Run all cells** from top to bottom (Kernel → Restart & Run All). All visualizations render inline and are saved to the `visualizations/` folder.

---

## Key Findings

- Curry's scoring peaked in **February** at 36.3 PPG with 58.3% FG and 47.6% 3P%
- **Home win rate (62%)** was 20 points higher than away (42%), despite nearly identical personal stats
- **Plus/minus** was the strongest predictor of a Warriors win (r = 0.81)
- **3-point percentage** (r = 0.27) mattered more than raw scoring (r = 0.16)
- Curry averaged **more turnovers in wins** — reflecting a more aggressive, high-reward style
- Minutes played had **zero correlation** with winning (r = 0.00)

---

## Author

**Nathan Merrill**  
Data Analytics Capstone Project  
Mountainland Technology  
