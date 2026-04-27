# La Liga Match Outcome Prediction — ML

> Multi-model machine learning pipeline to predict Spanish La Liga match results (Win/Draw/Loss) using 6 seasons of data (2019–2025), with xG features, form engineering, and neural network comparison.

---

## Results at a glance

| Model | Accuracy | F1 (macro) |
|-------|----------|------------|
| Logistic Regression (baseline) | 56.2% | 0.47 |
| Random Forest | 61.8% | 0.54 |
| Gradient Boosting | 63.4% | 0.56 |
| **Neural Network (MLP)** | **65.1%** | **0.58** |

> Predicting football matches is hard — 65% accuracy on a 3-class problem (W/D/L) substantially beats the 44.6% naive home-win baseline.

---

## Dataset

- **Source:** Kaggle — La Liga 2019/20 → 2024/25
- **Records:** 4,318 team-match records (2,159 unique fixtures)
- **Teams:** 27 La Liga clubs
- **Features:** Goals (GF/GA), Expected Goals (xG/xGA), possession %, shots, shots on target, venue, referee, attendance, day of week

---

## Key findings

| Insight | Value |
|---------|-------|
| Home win rate | **44.6%** vs 27.9% away |
| Real Madrid win rate (best team) | 67.6% |
| FC Barcelona win rate | 65.7% |
| Possession for winners (avg) | 51.2% |
| Possession for losers (avg) | 48.8% |
| Sunday average attendance | ~32,400 (highest) |

**Takeaway:** possession alone barely separates winners from losers — xG and shot quality are stronger signals.

---

## Feature engineering

- **Form streaks:** rolling 5-match win/draw/loss ratio
- **Efficiency ratios:** goals per shot, xG accuracy (goals / xG)
- **Head-to-head:** historical win rate between opponent pairs
- **Schedule density:** days since last match (fatigue proxy)
- **Venue encoding:** home / away / neutral

---

## Pipeline

```
Raw CSV (Kaggle)
    │
    ├── Missing value imputation (attendance: 22.6% missing → median fill)
    ├── Feature engineering (form, efficiency, H2H)
    ├── Encoding (venue, referee, day-of-week → one-hot)
    ├── 80/20 chronological train-test split
    │
    ├── Logistic Regression  ──┐
    ├── Random Forest          ├── GridSearchCV hypertuning
    ├── Gradient Boosting      │   5-fold cross-validation
    └── MLP Neural Network  ───┘
            │
    Evaluation: accuracy, F1-macro, confusion matrix, feature importance
```

---

## Quick start

```bash
# Open the notebook
jupyter notebook fcb.ipynb
```

All analysis, EDA, feature engineering, model training, and evaluation is in the single notebook `fcb.ipynb`.

---

## Author

**Kyaw Linn Khant** — Robotics & AI Engineer  
[Portfolio](https://kyawlinnkhant.github.io/my_portfolio/) · [LinkedIn](https://linkedin.com/in/kyawlinnkhant)
