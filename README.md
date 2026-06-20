# NL Team Trends

Historical National League team performance data, trends, and visualizations across past MLB seasons.

## Overview

This repository compiles historical win-loss records, seasonal performance trends, and key statistics for every National League franchise dating back to the league's founding in **1876**. The goal is to provide a comprehensive dataset for analyzing team dominance, franchise trajectories, divisional realignments, and the evolving competitive landscape of baseball's oldest league.

## Data Sources

The data compiled here is drawn from the following authoritative sources:

| Source | Description |
|--------|-------------|
| [Baseball-Reference.com – NL Standings](https://www.baseball-reference.com/leagues/NL/) | Season-by-season standings, team statistics, and franchise histories |
| [Retrosheet.org](https://www.retrosheet.org/) | Play-by-play data and historical box scores |
| [MLB.com – National League](https://www.mlb.com/national-league) | Official MLB National League records and archives |
| [Hall of Fame – NL Exhibits](https://baseballhall.org/) | Historical context on franchise milestones |
| [SABR – National League Chapter](https://sabr.org/) | Research from the Society for American Baseball Research |
| [Baseball Almanac](https://www.baseball-almanac.com/) | Historical records and franchise timelines |

## What's Included

### `nl_historical_data.csv`
A season-by-season dataset covering **1876–2024** with the following fields:

| Column | Description |
|--------|-------------|
| `season` | MLB season year |
| `team` | Franchise name (as it existed that season) |
| `modern_name` | Current franchise name (where applicable) |
| `division` | NL East / Central / West (or "N/A" for pre-division eras) |
| `wins` | Regular-season wins |
| `losses` | Regular-season losses |
| `win_pct` | Win percentage (wins / total games) |
| `playoff_finish` | NL Pennant, World Series title, Wild Card, or "—" |

### Key Trends Covered

- **Franchise Longevity**: Tracking teams from the NL's 1876 founding (Braves, Cubs, Reds, Giants, Phillies, Pirates) through modern expansions.
- **Dominance Eras**: The late-1870s Boston/Worcester dynasty, the early-1900s Pittsburgh/Chicago rivalry, the Giants' 1910s–1920s reign, the Dodgers–Giants–Cardinals axis, the Cardinals' 2000s–2010s dominance.
- **Expansion Impact**: How the 1962, 1969, 1993, and 1998 expansions reshaped the competitive balance.
- **Divisional Realignment**: The shift from 2 divisions (1969) to 3 divisions (1994) and the introduction of the Wild Card.
- **Pennant & Championship Histories**: Every NL pennant winner and World Series champion from 1876 to present.
- **Win-Loss Ratio Analysis**: Identifying the strongest single-season performances and the most consistent franchises over decades.

## Getting Started

### Clone the Repository
```bash
git clone https://github.com/zhub9006/nl-team-trends-data.git
cd nl-team-trends-data
```

### View the Data
The primary dataset is in `nl_historical_data.csv`. You can open it in any spreadsheet application or analyze it with Python/R:

```python
import pandas as pd
df = pd.read_csv('nl_historical_data.csv')
print(df.head())
```

## Visualization Ideas

- **Timeline of Pennant Winners**: Bar chart showing NL pennant counts per franchise.
- **Win Percentage Heatmap**: Season × Team matrix colored by win percentage.
- **Franchise Win Totals**: Cumulative wins by franchise over time.
- **Dynasty Detection**: Rolling 5-year and 10-year win averages to identify dominant periods.
- **Division Dominance**: Which division has produced the most pennant winners.
- **Expansion Impact Analysis**: Win distribution before and after each expansion wave.
- **Playoff Success Rate**: Percentage of seasons that made it to postseason by era.

## Contributing

Contributions are welcome! If you have additional historical data, corrections, or new analyses, please open an issue or submit a pull request.

### Data Validation
All data should be cross-referenced with Baseball-Reference or Retrosheet. Please include source citations when adding new records.

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- The millions of play-by-play records maintained by **Retrosheet**
- The **Baseball Hall of Fame** for preserving franchise histories
- **SABR** members who have documented NL history for decades
- **Baseball-Reference** for making historical stats freely accessible