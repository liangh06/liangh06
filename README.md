## Liang Hong

Economics & Mathematics (B.S., UNC Chapel Hill, May 2026). I build data work end to end:
ingestion pipelines, SQL models, and dashboards, with a bias toward results that hold up
when someone checks them.

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

### How I work

- **Reproducibility.** Pipelines rebuild from the raw source; nothing is hand-patched.
- **Validation.** Dashboard figures reconcile to the SQL that produced them.
- **Honest scope.** Known limitations (selection bias, confounding, sample maturity) get
  documented rather than buried.
