# Cricklytics – IPL Match Analytics Engine

Cricklytics is a powerful data analytics engine that processes, analyzes, and visualizes **1100+ IPL matches** using YAML match files. It transforms raw match data into strategic insights, powering detailed player reports, fantasy suggestions, pitch analysis, and more — all using Python and SQLite3.

---

## Table of Contents
- [What It Does](#-what-it-does)
- [Tech Stack](#-tech-stack)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Setup & Usage](#-setup--usage)
- [Sample Output](#-sample-output)
- [Contributing](#-contributing)
- [License](#-license)
- [Author](#-author)

---

## What It Does

- Parses YAML files containing match details from IPL seasons
- Loads structured data into a relational SQLite3 database
- Enables advanced cricket analytics via Python scripts and (optional) GUI
- Generates insights on players, venues, partnerships, and fantasy picks

---

##  Tech Stack

| Layer        | Technology                      |
|--------------|----------------------------------|
| Language     | Python 3                         |
| Backend DB   | SQLite3                          |
| Parsing      | PyYAML                           |
| Frontend     | Flask, HTML/CSS (WIP)            |
| Analytics    | NumPy, Custom Modules            |
| Visualization| Matplotlib, Seaborn (planned)    |

---

## Features

### Core Modules:
- **Match Parser** – Extracts teams, overs, players, and performance from raw YAML
- **SQLite Loader** – Inserts structured match data into a database
- **Player Analytics** – Batting, bowling, and all-round reports
- **Venue Inference** – Pitch behavior and scoring trends at stadiums
- **Batsman vs Bowler Matchups** – H2H analysis with averages & dismissals

### Advanced Features:
- **Fantasy Suggestions** – Based on recent form, matchups, and opposition
- **Milestone Tracker** – Highlights nearing records (runs, wickets, etc.)
- **Impact Player Finder** – Who steps up under pressure
- **Clutch Performance** – Identifies match finishers
- **Partnership Analytics** – Best batting pairs, collapses, streaks
- **Team Overviews** – Season-wise best/worst performances
- **AI Integration** (planned) – Predictive metrics and smart recommendations

---

## 📁 Project Structure

```
cricklytics/
│
├── data/
│   └── yaml/                  # 1100+ raw IPL match YAML files
│
├── db/
│   └── cricklytics.db         # SQLite3 database (auto-generated)
│
├── src/
│   ├── parser.py              # YAML-to-SQLite parser
│   ├── analyzer/
│   │   ├── player_stats.py
│   │   ├── venue_report.py
│   │   ├── fantasy_engine.py
│   │   └── clutch_analyzer.py
│   └── utils.py               # Common helper functions
│
├── gui/                       # Flask based Web App
│   └── main.py
│
├── outputs/                   # Exported reports and graphs
├── requirements.txt
├── README.md
└── LICENSE
```

---

## ⚙️ Setup & Usage

### 1. Clone the Repo
```bash
git clone https://github.com/your-username/cricklytics.git
cd cricklytics
```

### 2. Install Requirements
```bash
pip install -r requirements.txt
```

### 3. Run the Parser (to build DB)
```bash
python src/parser.py
```

### 4. Launch GUI (optional)
```bash
python gui/main.py
```

---

## 🧪 Sample Output

```bash
> Most Runs at M. Chinnaswamy Stadium
1. Virat Kohli     – 921 runs
2. AB de Villiers  – 834 runs
3. Chris Gayle     – 775 runs

> Bumrah vs Dhoni Head-to-Head
Matches: 14 | Dismissals: 3 | Avg: 19.8 | SR: 87.5

> Fantasy Picks for Today’s Match
Top Batsmen: Rahul, Samson
Top Bowlers: Rashid, Chahar
X-Factor: Jitesh Sharma
```

---

## 🧾 requirements.txt

```txt
pyyaml
numpy
sqlite3
flask
```

---

## 🤝 Contributing

Have ideas to improve Cricklytics? Want to fix a bug or add a module?

1. Fork the repo
2. Create a new branch
3. Make your changes
4. Submit a Pull Request (PR)

Coming soon: `CONTRIBUTING.md` & code documentation

---

## 📜 License

This project is licensed under the **MIT License** — you're free to use, modify, and share it with proper credit.

---

## 👨‍💻 Author

**Akhilesh Kancharla**  
*CSE @ MGIT '28 | Python/C Dev | Data + Sports Analytics Enthusiast | Project-Driven Learner*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Akhilesh_Kancharla-blue?logo=linkedin)](www.linkedin.com/in/akhilesh-kancharla-63b5b6327)  
[![GitHub](https://img.shields.io/badge/GitHub-AkhileshKancharla-black?logo=github)](https://github.com/Akhilesh-Kancharla)

---

> ⚠️ NOTE: This project is currently in active development. Expect new features and updates weekly!
