# NFL Fantasy Garbage Time Analysis

## Overview

Analysis of NFL wide receivers to identify which players get the highest percentage of their fantasy points during "garbage time" situations using 2024 season data and win probability metrics.

## Key Findings

- Keenan Allen leads with 42.9% of fantasy points from garbage time (185 total FP)  
- Antonio Brown at 33.4% garbage time dependency (178 total FP)  
- Rome Odunze at 27.3% for rookie season (145 total FP)  
- League average garbage time percentage: 14.3%  
- Only 1 receiver exceeded 30% garbage time dependency

## Data Source

nflfastR play-by-play data with win probability calculations

## Tools Used

- R with nflfastR, dplyr, tidyr, ggplot2, DT  
- Win probability modeling for garbage time identification  
- PPR fantasy scoring system

## Methodology

- **Garbage Time**: Win probability < 5% for either team  
- **Minimum Thresholds**: 100 fantasy points, 50 targets  
- **Scoring**: 1 pt per reception + 0.1 per yard + 6 per TD

## Files

- `garbage_time_analysis.R` - Main analysis script  
- `README.md` - This documentation
