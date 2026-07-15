# Visualization Roadmap

## Recommended Tools & Libraries

| Tool | Best For | Example |
|------|----------|---------|
| Matplotlib / Seaborn | Static charts (bar, line, heatmap) | Win% trends by decade |
| Plotly | Interactive dashboards | Hover-over team detail maps |
| Bokeh | Web-based interactive plots | Pennant timeline slider |
| Altair | Declarative statistical viz | EDA of win distributions |
| Folium / Geopandas | Geographic mapping | Team locations & migration paths |
| Vincent Vega / Vega-Lite | Grammar-of-graphics | Reproducible chart specs |
| Jupyter Notebook + IPyWidgets | Notebooks with interactivity | Filter by era, division |

## Suggested Visualizations

### 1. Timeline of NL Pennant Winners
- Type: Gantt chart / horizontal bar
- Data: data/nl_pennant_winners_recent.csv
- Insight: Visualize which teams dominated which eras

### 2. Win Percentage Heatmap (Team x Decade)
- Type: Heatmap
- Data: data/nl_historical_performance.csv
- Insight: Identify dominant eras and declining franchises

### 3. Franchise Win Totals Bar Chart
- Type: Horizontal bar chart
- Data: data/nl_all_time_records.csv
- Insight: Giants, Dodgers, and Cards lead all-time wins

### 4. Championship Drought Analysis
- Type: Box plot / strip plot
- Data: Computed from championship trends
- Insight: Distribution of droughts between titles; Phillies as extreme outlier

### 5. Head-to-Head Matrix (Simplified)
- Type: Competitive matrix / network graph
- Insight: Rivalry intensity over time; Cubs-Cardinals, Dodgers-Giants

### 6. Moving Average Win% by Decade
- Type: Line chart
- Data: Computed from season-level totals
- Insight: League parity trends; post-2020 competitive balance

### 7. Geographic Franchise Migration Map
- Type: Geographic scatter / choropleth
- Insight: Map franchise migrations (Brooklyn to LA, Boston/Milwaukee to Atlanta, Montreal to Washington)

## Data Flow

```
data/raw/          <-- Downloaded source CSVs (SABR Lahman, etc.)
data/processed/    <-- Cleaned datasets for analysis
data/visualizations/ <-- Generated charts & plots
notebooks/         <-- Jupyter notebooks for EDA
```

## Quick-Start (Python)

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load all-time records
df = pd.read_csv('data/nl_all_time_records.csv')
df = df.sort_values('wins', ascending=True)

fig, ax = plt.subplots(figsize=(10, 8))
ax.barh(df['franchise'], df['wins'], color='steelblue')
ax.set_xlabel('All-Time NL Wins')
ax.set_title('NL Franchise All-Time Wins (through 2025)')
plt.tight_layout()
plt.savefig('visualizations/nl_all_time_wins.png', dpi=150)
plt.show()
```
