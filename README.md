# Ipl_dashboard
# 🚀 IPL Analysis Dashboard (2005–2025) | Power BI Project

![IPL Dashboard Banner](assets/banner.png)

> An end-to-end data analytics project analyzing **20 years of IPL data** — from season-wise trends to player performance and team standings.

---

## 📊 Project Overview

This Power BI dashboard provides comprehensive insights into the Indian Premier League (IPL) from its inaugural season in 2008 through 2025. The project demonstrates advanced data modeling, DAX calculations, and interactive visualization techniques.

---

## 🔍 Key Highlights

| Feature | Description |
|---|---|
| 📅 Season-wise Performance | Year-by-year match trends, win rates, and team comparisons |
| 🟠 Orange Cap | Top run-scorers per season with batting stats |
| 🟣 Purple Cap | Top wicket-takers per season with bowling stats |
| 🏆 Team Standings | Points table with NRR, wins, losses breakdown |
| 🏏 Player Performance | Runs, Wickets, Fours, Sixes at player level |
| 🏟️ Match Insights | Total matches, venues, centuries, super overs |

---

## 🛠️ Tools & Skills Used

- **Power BI Desktop** — Data Modeling, DAX, Interactive Visualization
- **Power Query** — Data Cleaning & Transformation
- **DAX** — Custom measures and calculated columns
- **Excel / CSV** — Raw data sources
- **Interactive Dashboard Design** — Drill-throughs, slicers, bookmarks

---

## 📁 Project Structure

```
ipl-analysis-dashboard/
│
├── 📂 data/
│   ├── ipl_matches.csv          # Match-level data (2008–2025)
│   ├── ipl_deliveries.csv       # Ball-by-ball delivery data
│   ├── ipl_players.csv          # Player metadata
│   └── ipl_teams.csv            # Team information
│
├── 📂 assets/
│   ├── banner.png               # Project banner image
│   └── screenshots/             # Dashboard screenshots
│
├── 📂 docs/
│   ├── DAX_Measures.md          # All DAX formulas used
│   └── Data_Dictionary.md       # Column descriptions
│
├── IPL_Dashboard.pbix           # Main Power BI file
├── dashboard_preview.html       # Interactive HTML preview
└── README.md
```

---

## 📸 Dashboard Preview

### Main Overview Page
![Overview](assets/screenshots/overview.png)

### Player Performance Page
![Players](assets/screenshots/players.png)

### Team Standings Page
![Standings](assets/screenshots/standings.png)

---

## 📐 DAX Measures (Key Examples)

```dax
-- Total Runs
Total Runs = SUM(Deliveries[total_runs])

-- Strike Rate
Strike Rate = 
DIVIDE([Total Runs], [Total Balls Faced], 0) * 100

-- Economy Rate
Economy Rate = 
DIVIDE([Total Runs Conceded], [Total Overs Bowled], 0)

-- Win %
Win % = 
DIVIDE([Total Wins], [Total Matches], 0) * 100

-- Orange Cap (Season)
Orange Cap Player = 
CALCULATE(
    FIRSTNONBLANK(Players[player_name], 1),
    TOPN(1, VALUES(Players[player_name]), [Total Runs], DESC)
)
```

---

## 🗂️ Data Sources

The dataset is sourced from publicly available IPL datasets:
- [Kaggle IPL Dataset](https://www.kaggle.com/datasets/nowke9/ipldata)
- Official BCCI records
- ESPNcricinfo

> **Note:** Data has been cleaned and transformed using Power Query before loading into the model.

---

## 🚀 How to Use

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/ipl-analysis-dashboard.git
   cd ipl-analysis-dashboard
   ```

2. **Open Power BI file**
   - Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
   - Open `IPL_Dashboard.pbix`

3. **Refresh Data** *(if updating dataset)*
   - Go to `Home → Transform Data → Refresh`
   - Ensure CSV paths point to the `/data` folder

4. **Explore the Dashboard**
   - Use slicers to filter by Season, Team, or Player
   - Click on visuals for drill-through details
   - Toggle bookmarks for different views

---

## 📈 Insights Discovered

- **Mumbai Indians** have the highest win percentage across all seasons
- **Virat Kohli** holds the record for most runs in a single IPL season (2016)
- **Wankhede Stadium** has hosted the most IPL matches
- Average first innings score has increased by ~25 runs over 20 years
- Death-over scoring rates have improved significantly post-2015

---

## 🤝 Contributing

Contributions are welcome! If you have updated data or new visualizations:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-analysis`)
3. Commit your changes (`git commit -m 'Add: 2025 season data'`)
4. Push and open a Pull Request

---

---

## 🙋 Connect With Me

If you found this project helpful, drop a ⭐ on GitHub!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://linkedin.com/in/karan-garje-3b949a375)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=flat&logo=github)](https://github.com/karangarje48-lab/desktop-tutorial)

---

*Built with ❤️ using Power BI | Data Analytics Portfolio Project*
