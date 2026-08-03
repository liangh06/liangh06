# Liang Hong

Economics & Mathematics (B.S., UNC Chapel Hill, May 2026). I build analytics end to end:
ingestion pipelines, SQL models, and BI dashboards. 

**Toolkit:** SQL (PostgreSQL) · Python (pandas, scikit-learn) · R · Power BI (DAX) · Tableau · Git

📍 Chapel Hill, NC · 📫 liang.hong@alumni.unc.edu · [LinkedIn](https://linkedin.com/in/liang-hong-unc)

---

# Projects

## LendingClub Credit-Risk Analysis & BI Dashboard

**Repo:** [liangh06/lendingclub-credit-risk](https://github.com/liangh06/lendingclub-credit-risk)

**Goal:** Determine which loan grades actually deliver return once defaults are priced in,
and which borrower attributes predict default at origination.

**Data:** 2.26M LendingClub loans, $34B funded, 151 columns (2007–2018).

**Approach:** Python + PostgreSQL ingestion of every source column with per-row validation
and load reconciliation, then a three-layer SQL model that separates at-origination features
from post-origination outcomes, surfaced through a four-page Power BI dashboard.

**Technology:** Python, PostgreSQL, SQL, Power BI (DAX), Git

**Skills:** ETL pipeline design, data validation and reconciliation, dimensional modeling,
data-leakage control, SQL analysis, DAX measures, dashboard development

**Results:** Dollar-weighted net return peaks at grade B and turns **negative** below grade E:
higher-yield loans do not cover their defaults. Default rate climbs from 6% (grade A) to 50%
(grade G), with FICO and debt-to-income the cleanest predictors. Every dashboard figure
reconciles to the SQL that produced it.

[![Risk and return by grade](https://raw.githubusercontent.com/liangh06/lendingclub-credit-risk/main/powerbi/screenshots/02_risk_return.png)](https://github.com/liangh06/lendingclub-credit-risk)

---

## NBA Pre-Game Win Prediction

**Repo:** [liangh06/nba-win-prediction](https://github.com/liangh06/nba-win-prediction)

**Goal:** Predict the home team's win probability before tip-off, and beat the
home-court baseline of simply always picking the home side.

**Data:** ~26,500 NBA games, reshaped to one row per team per game so form can be
rolled forward.

**Approach:** Each team's rolling 10-game form plus rest days, reduced to 8
home-minus-away gaps after an ablation showed absolute team quality adds nothing.
Rolling stats use `.shift(1)` so a game never sees its own result, the split is
chronological, and the probability calibrator is fitted on held-out data rather than
on the training set.

**Technology:** Python, pandas, scikit-learn

**Skills:** feature engineering, leakage-safe validation, chronological splitting,
model selection, probability calibration

**Results:** 60.9% accuracy against a 55.6% home-court baseline (AUC 0.648, Brier
0.232 calibrated) on a test set scored once. Ablation shows relative matchup
strength carries the signal almost entirely: the gap between two teams predicts at
AUC 0.649, while their absolute quality is close to a coin flip at 0.521.

[![What predicts a home win](https://raw.githubusercontent.com/liangh06/nba-win-prediction/main/charts/coefficients.png)](https://github.com/liangh06/nba-win-prediction)
