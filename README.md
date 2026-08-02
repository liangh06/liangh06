## Liang Hong

Economics & Mathematics (B.S., UNC Chapel Hill, May 2026). I build data work end to end:
ingestion pipelines, SQL models, and dashboards, with a bias toward results that hold up
when someone checks them.

**Toolkit:** SQL (PostgreSQL) · Python (pandas, scikit-learn) · R · Power BI (DAX) · Tableau · Git

---

### Featured: [LendingClub Credit Risk](https://github.com/liangh06/lendingclub-credit-risk)

End-to-end credit-risk analysis of **2.26M loans ($34B funded)**: raw CSV → PostgreSQL →
typed SQL model → a validated four-page Power BI dashboard.

| | |
|---|---|
| **Pipeline** | Python + PostgreSQL ingestion of all 151 columns with per-row validation and load reconciliation, for zero data loss |
| **Model** | Three-layer SQL schema with a structural data-leakage boundary separating at-origination features from post-origination outcomes |
| **Dashboard** | 13 DAX measures, every figure reconciled back to the SQL that produced it |
| **Finding** | Dollar-weighted net return peaks at grade B and turns **negative** below grade E: higher-yield loans do not cover their defaults |

[![Risk and return by grade](https://raw.githubusercontent.com/liangh06/lendingclub-credit-risk/main/powerbi/screenshots/02_risk_return.png)](https://github.com/liangh06/lendingclub-credit-risk)

---

### What I care about

- **Reproducibility.** Pipelines rebuild from the raw source; nothing is hand-patched.
- **Validation.** Dashboard figures reconcile to the SQL that produced them.
- **Honest scope.** Known limitations (selection bias, confounding, sample maturity) get
  documented rather than buried.

---

📍 Chapel Hill, NC · 📫 liang.hong@alumni.unc.edu · [LinkedIn](https://linkedin.com/in/liang-hong-unc)
