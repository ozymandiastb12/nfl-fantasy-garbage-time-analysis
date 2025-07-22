NFL Fantasy Garbage Time Analysis
An R-based analysis identifying which NFL wide receivers get the highest percentage of their fantasy points during "garbage time" situations using 2024 season data.
Repository Name Suggestion
nfl-fantasy-garbage-time-analysis
Overview
This project analyzes NFL receiving data to identify players who accumulate disproportionate fantasy points when games are effectively decided. Using advanced win probability metrics rather than simple score differentials, we can pinpoint receivers who pad stats during prevent defense situations.
Key Findings (2024 Season)
Top Garbage Time Fantasy Receivers:

Keenan Allen: 42.9% of fantasy points from garbage time (185 total FP)
Antonio Brown: 33.4% of fantasy points from garbage time (178 total FP)
Rome Odunze: 27.3% of fantasy points from garbage time (145 total FP)

League Averages:

Average garbage time percentage: 14.3%
Only 1 receiver exceeded 30% garbage time dependency
Minimum thresholds: 100 fantasy points, 50 targets

Methodology
Garbage Time Definition

Win Probability < 5% for either team (superior to score-based methods)
Accounts for time remaining, field position, and game context
More accurate than arbitrary score differential thresholds

Fantasy Scoring

PPR (Point Per Reception) format
1 point per reception
0.1 points per receiving yard
6 points per touchdown

Sample Criteria

Minimum 100 PPR fantasy points (season)
Minimum 50 targets (ensures meaningful sample size)
2024 NFL regular season data

Data Sources

nflfastR: Play-by-play NFL data with win probability calculations
Includes all passing and rushing plays for receivers
Real-time win probability modeling accounts for game context

Requirements
r# Required R packages
library(nflfastR)
library(dplyr)
library(tidyr)
library(ggplot2)
library(DT)
Usage

Clone the repository
Install required packages: install.packages(c("nflfastR", "dplyr", "tidyr", "ggplot2", "DT"))
Run the analysis script: source("garbage_time_analysis.R")
View results in console and generated visualizations

Output

Console Results: Top 15 receivers ranked by garbage time percentage
Summary Statistics: League averages and distribution metrics
Interactive Table: Detailed breakdown for all qualifying receivers
Visualization: Bar chart of top 20 receivers (when plot renders successfully)

Interpretation
High Garbage Time Dependency Indicates:

Players on frequently blown-out teams
Receivers who maintain target share in hopeless situations
Potential "stat padding" during prevent defense
Fantasy output inflated by non-competitive game situations

Fantasy Implications:

Negative: Production may not be sustainable or meaningful
Positive: Volume in garbage time still counts for fantasy
Context: Consider team strength and game script dependency

Methodology Advantages

Win Probability > Score Differential: Captures true game context
Time-Aware: 10-point deficit means different things with 2 vs 12 minutes left
Field Position Sensitive: Accounts for down, distance, and field position
Prevents False Positives: Avoids labeling comeback attempts as garbage time

Limitations

Single season analysis (2024 only)
Doesn't distinguish WRs from TEs/RBs in current implementation
No adjustment for team-level garbage time frequency
Doesn't account for opponent prevent defense tendencies

Future Improvements

 Multi-season analysis (2021-2024) for trend identification
 Player position filtering using roster data
 Team-level garbage time frequency analysis
 Opponent defensive scheme adjustments
 Late-and-close situation comparison analysis
 Predictive modeling for future garbage time dependency

Files

garbage_time_analysis.R - Main analysis script
README.md - This documentation
results/ - Output directory for generated files# nfl-fantasy-garbage-time-analysis
