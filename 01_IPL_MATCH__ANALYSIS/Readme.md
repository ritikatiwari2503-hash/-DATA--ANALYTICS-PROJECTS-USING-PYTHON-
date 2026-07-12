## ⭐ IPL MATCH ANALYSIS ⭐
## 📌 Overview 

Analyzed 633 IPL matches across 10 seasons (2008–2017) using a full clean → explore → visualize → report pipeline to answer real questions about what actually drives match outcomes.

**Key question explored:** Does winning the toss actually help you win the match — or does team quality matter more than the coin flip?

## 🔍 Key Findings

- Analyzed 633 IPL matches (2008–2017) to identify team performance and venue trends
- Toss outcome had only a marginal (~51%) effect on match results — team quality matters far more than winning the toss
- Mumbai Indians recorded the most wins by a clear margin (92), ahead of Chennai Super Kings (79) and Kolkata Knight Riders (77)
- M Chinnaswamy Stadium was the most-used venue (64 matches), narrowly ahead of Eden Gardens (61) and Feroz Shah Kotla (59)
- Matches per season spiked sharply between 2011–2013 (72–76 matches) before settling back to the usual 57–60 range in later seasons

## ✅ Tools Used

- **Python** — core language
- **Pandas** — data cleaning and analysis
- **NumPy** — underlying numerical operations
- **Matplotlib** — data visualization
- **Jupyter Notebook** — development environment

## 📂 Project Structure

```
01_IPL_MATCH_ANALYSIS/
├── data/
│   └── matches.csv          # raw dataset (IPL match-level data, 2008–2017)
├── ipl_analysis.ipynb       # main notebook: cleaning, EDA, visualizations
├── images/
│   ├── ipl_image1.png       # Most Match Wins by Team
│   └── ipl_image2.png       # Matches Played per Season
└── readme.md
```

## 🧹 Data Cleaning Steps

- Converted the `date` column from text to proper datetime format
- Removed 3 matches with no result (rain-affected/abandoned games)
- Standardized inconsistent team name spellings across seasons, including franchise renames (*Delhi Daredevils* → *Delhi Capitals*) and a data-entry typo (*Sunrises Hydrabad* → *Sunrisers Hyderabad*) that was silently splitting one team's win count into two
- Checked for and confirmed zero duplicate records

## 📊 Visualizations


<img width="352" height="259" alt="ipl_image1" src="https://github.com/user-attachments/assets/26b677f4-5028-459d-bdd7-3d5ccc881b17" />
<img width="349" height="273" alt="image" src="https://github.com/user-attachments/assets/18aafe9b-9ed3-4969-9115-8ea1416a9fc5" />


## 🚀 How to Run This Yourself

```bash
git clone https://github.com/ritikatiwari2503-hash/DATA-ANALYSIS-PROJECTS-USING-PYTHON.git
cd DATA-ANALYSIS-PROJECTS-USING-PYTHON/01_IPL_MATCH_ANALYSIS
pip install pandas numpy matplotlib jupyter
jupyter notebook ipl_analysis.ipynb
```
*(Double-check the repo name and folder name above exactly match what's shown in your GitHub URL — small naming differences will make this command fail.)*

## 📈 What's Next

- Extend analysis to ball-by-ball (`deliveries.csv`) data for player-level stats (strike rates, economy rates)
- Build an interactive dashboard (Streamlit) for exploring trends by team/season

## 👤 Author

**Ritika Tiwari**
Data Science and AI Student, IIT Madras
[LinkedIn](https://linkedin.com/in/ritika-tiwari-723b98370) · [GitHub](https://github.com/ritikatiwari2503-hash)

---
⭐ *If you found this project useful or interesting, feel free to star the repo!*
