⭐ Engagement & Risk Scoring Engine ⭐

🔍 Overview

Built a composite scoring engine that tracks entities over time, flags the ones trending toward risk, and visualizes exactly when things started declining. Demonstrated on real student data (395 records, UCI Student Performance Dataset) — cleaning, normalizing, and scoring multiple weak signals into one risk-ranked output.

The engine itself is domain-agnostic: the same normalize → weight → threshold → flag-decline pipeline applies anywhere you're tracking many entities over time and need to surface the ones needing attention — e.g. overdue compliance filings, customer churn, support-ticket escalation.

---

🎯 Objective

Most basic "student data" projects stop at descriptive stats and a couple of bar charts. This project goes a step further by building a reusable scoring system that:
- Combines multiple weak signals into one defensible composite score
- Classifies risk into Low / Medium / High
- Detects genuine declining trends (not just a single bad snapshot)
- Outputs a ranked, ready-to-act-on list

---

📊 Dataset

Source: UCI Machine Learning Repository — Student Performance Dataset (Cortez & Silva, 2008)
Link: https://archive.ics.uci.edu/dataset/320/student+performance

- 395 real student records from two Portuguese secondary schools
- Signals used: attendance (absences), study time, going-out frequency (participation proxy), school/family support, and grades across 3 grading periods (G1, G2, G3)
- The three grading periods act as the time dimension, enabling trend detection across periods rather than a single snapshot

---

🛠️ Approach

1. Load & Clean — read raw CSV, drop duplicates, handle missing values
2. Normalize — scale every signal to a common 0–1 range
3. Composite Score — weighted combination of signals, computed separately per grading period
   - Weights: Attendance 0.30 · Grades 0.25 · Study Time 0.20 · Participation 0.15 · Support 0.10
   - Attendance is weighted highest as a leading indicator (changes before grades do); grades are weighted lower since they're a lagging/outcome signal
4. Risk Classification — Low / Medium / High based on the latest period's score
5. Decline Detection — ✅  flags entities whose score dropped across two consecutive periods, not just one dip
6. Visualization —     ✅  score distribution, risk breakdown, and trend lines for declining cases
7. Export —            ✅  ranked CSV of flagged entities, sorted by risk🔍🌸💫📊⭐🖤😌🪶✨📈👤

---

📈 Key Outputs

- flagged_students.csv — ranked list of students needing attention
- score_distribution.png — spread of composite scores across all students
- risk_breakdown.png — Low / Medium / High counts
- declining_trends.png — score trajectories for students in genuine decline

---

⭐Tech Stack
1.  Python 
2.  Pandas
3.  NumPy
4.  Matplotlib

---

🚀 How to Run

pip install -r requirements.txt
python engagement_risk_engine.py

Outputs are generated in the output/ folder.

---

💡 Why This Design

The core logic — normalize signals, weight them, threshold into risk tiers, flag sustained decline — isn't specific to education. Swap the input signals (e.g. filing-deadline proximity and document completeness instead of attendance and grades) and the same engine becomes a compliance-risk flagging tool. This project is built to demonstrate that transferable systems-thinking, not just a one-off analysis.

---

* Note on Scope

This is an independent personal project using a public, well-known academic dataset. It is not affiliated with, or built using, any institution's internal or private student data.

📌 About me
👤🌸Ritika Tiwari —>
first-year , IIT Madras⭐ BS in Data Science and AI .
