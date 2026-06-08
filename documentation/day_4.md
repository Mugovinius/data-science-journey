# Day 4 — Exploratory Data Analysis, Risk Analytics & Decision Science

## Objective

The objective of Day 4 was to move beyond traditional descriptive analytics and begin thinking like a Data Scientist working in a banking environment.

The focus shifted from:

* reporting metrics,
* summary statistics,
* descriptive analysis,

to:

* decision analytics,
* portfolio intelligence,
* risk analytics,
* credit strategy,
* and business action generation.

This was the first day where analytics became directly linked to operational and credit decisions.

---

# The Big Idea of Day 4

Most beginners use data to answer:

"What happened?"

Professional Data Scientists use data to answer:

"What should we do next?"

This distinction is critical.

Data becomes valuable only when it influences:

* lending decisions,
* collections decisions,
* risk decisions,
* pricing decisions,
* customer management strategies.

---

# Topics Covered

## 1. Exploratory Data Analysis (EDA)

Created a banking-style portfolio dataset containing:

* customer demographics,
* monthly income,
* loan amounts,
* days in arrears.

Performed:

```python
df.describe()
```

Learned that descriptive statistics are not the final goal.

Instead, every statistic should trigger a business question.

Examples:

* Is the average income representative?
* Are there dangerous outliers?
* Is the portfolio concentrated?
* Is risk increasing?

---

# 2. Descriptive Statistics Reframed

Moved beyond:

* maximum values,
* minimum values,
* averages.

Shifted toward:

* portfolio exposure,
* affordability,
* customer risk,
* business impact.

Important realization:

A statistic is only useful when it supports a decision.

---

# 3. Portfolio Intelligence

Introduced portfolio-level thinking.

Key questions explored:

* How much exposure exists in the portfolio?
* Which customers contribute most exposure?
* Is exposure concentrated among a few customers?
* Which segments drive portfolio value?

Important realization:

Exposure concentration is often more important than simple averages.

---

# 4. Loan-to-Income Analysis

Created:

```python
df["loan_to_income_ratio"] = (
    df["loan_amount"] /
    df["monthly_income"]
)
```

Business interpretation:

Loan Amount = Exposure

Income = Repayment Capacity

Loan-to-Income Ratio = Affordability Indicator

Important realization:

Two customers may have the same loan amount but vastly different risk profiles.

This metric introduced affordability analysis and credit risk thinking.

---

# 5. Risk Categorization

Created customer risk categories based on affordability and repayment behaviour.

Examples:

* Low Risk
* Medium Risk
* High Risk

Important realization:

Risk categories are not final outputs.

They become inputs into decision-making.

---

# 6. Decision Analytics

Created:

```python
next_decision
```

Examples:

* Approve
* Review
* Review Limit to Ksh 0
* Collections
* List Customer to CRB

This was one of the most important concepts of Day 4.

The focus shifted from:

"What is the customer's risk?"

to:

"What action should the institution take?"

Important realization:

Decision analytics transforms data into operational actions.

---

# 7. Decision Engine Thinking

Implemented logic using:

```python
np.where()
```

to automatically determine customer treatment strategies.

Example workflow:

Risk Signals
→ Risk Category
→ Decision Logic
→ Recommended Action

This mirrors how many digital lending systems operate.

Important realization:

This is the foundation of automated decisioning platforms.

---

# 8. Portfolio at Risk (PAR)

Introduced Portfolio at Risk concepts.

Example:

```python
PAR30
```

Measures:

Portfolio exposure held by customers above 30 Days Past Due.

Questions explored:

* What percentage of the portfolio is distressed?
* Which customers drive portfolio risk?
* Which segments contribute most delinquency?

Important realization:

Risk exposure matters more than customer counts.

---

# 9. Risk Concentration Analytics

Analyzed:

* exposure by risk category,
* exposure by decision category,
* exposure by delinquency bucket.

Questions explored:

* Are risky customers holding large balances?
* Is portfolio risk concentrated?
* Which segments should be monitored closely?

Important realization:

Money at risk is often more important than customer volume.

---

# 10. Affordability Analytics

Created affordability classifications based on:

```python
loan_to_income_ratio
```

Potential classifications:

* Healthy
* Moderate
* Risky
* Severely Overleveraged

Questions explored:

* Which customers can comfortably repay?
* Which customers are overleveraged?
* Which customers require intervention?

---

# 11. Customer Segmentation

Segmented customers using:

* income,
* exposure,
* risk,
* repayment behaviour.

Questions explored:

* Which customers deserve premium treatment?
* Which customers qualify for higher limits?
* Which customers require monitoring?

Important realization:

Segmentation drives business strategy.

---

# 12. Credit Strategy Analytics

Introduced lending policy questions.

Examples:

* Should limits be increased?
* Should limits be reduced?
* Which customers qualify for new lending?
* Which customers should be blocked?

Important realization:

Analytics should support credit policy decisions.

---

# 13. Collections Analytics

Introduced collections-oriented thinking.

Questions explored:

* Which customers require immediate follow-up?
* Which accounts should enter collections?
* Which accounts should be reported to CRB?

Important realization:

Analytics should support operational recovery strategies.

---

# 14. Executive Reporting Thinking

Shifted from:

"What is the maximum loan amount?"

to:

"Which portfolio segment carries the greatest exposure and risk?"

This is the mindset used in:

* Credit Committees,
* Risk Committees,
* Executive Management Reporting.

---

# Important Concepts Learned

## Portfolio Exposure

Loan balances represent institutional exposure.

## Repayment Capacity

Income provides context for lending decisions.

## Affordability

Loan-to-income ratios help assess customer sustainability.

## Risk Analytics

Risk should be measured by exposure, not only customer counts.

## Decision Analytics

The purpose of analytics is to drive action.

## Portfolio at Risk

PAR metrics quantify portfolio health.

## Decision Engines

Risk signals can be transformed into automated decisions.

---

# Key Realizations

* Data Science is not about reporting numbers.
* Analytics should influence business decisions.
* Risk categories are intermediate outputs.
* Decisions are the final outputs.
* Exposure matters more than counts.
* Banking analytics revolves around risk, profitability, and action.

---

# Deliverables Completed

## Notebook

```text
day_4_eda_and_statistics.ipynb
```

## Risk Categorization

Created customer risk classifications.

## Loan-to-Income Analysis

Implemented affordability analytics.

## Decision Engine

Generated automated next-action recommendations.

## Portfolio Risk Analysis

Introduced Portfolio at Risk concepts.

## Credit Strategy Analytics

Linked analytics outputs to lending decisions.

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Jupyter Notebook
* Git & GitHub

---

# Business & Industry Connections

Day 4 connects directly to:

* Credit Risk Analytics
* Digital Lending
* Portfolio Management
* Collections Strategy
* Credit Decision Engines
* Risk Management
* Banking Analytics
* Decision Science

---

# Final Massive Insight

Today marked another major transition.

The focus moved from:

"Understanding the data"

to:

"Determining what action should be taken."

This is the beginning of Decision Science.

Data becomes truly valuable when it helps an organization decide:

* who to lend,
* how much to lend,
* who to review,
* who to collect from,
* and where risk exists.

This is the mindset of professional banking analytics and modern Data Science.

---

# Next Session Preview (Day 5)

Planned topics:

* Probability
* Statistical Thinking
* Normal Distributions
* Z-Scores
* Risk Modeling Foundations
* Statistical Decision Making
* Foundations for Machine Learning

Goal:

Begin understanding the mathematics and statistical reasoning that power predictive models and credit scoring systems.
