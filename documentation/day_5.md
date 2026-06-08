# Day 5 — Statistics, Scorecards & Risk Modeling Foundations

## Objective

The objective of Day 5 was to introduce statistical thinking and connect it directly to banking analytics, credit scoring, portfolio risk management, and decision engines.

Unlike traditional statistics training that focuses heavily on formulas, this session focused on understanding how statistical concepts drive real business and lending decisions.

This marked the transition from:

Data → Insight → Risk → Decision

to:

Data → Statistics → Score → Probability → Decision

---

# The Big Idea of Day 5

Statistics is not about formulas.

Statistics helps answer:

- How unusual is this customer?
- How risky is this customer?
- How likely is a customer to default?
- Which customers deserve larger limits?
- Which customers require intervention?

Statistics forms the mathematical foundation for:

- Credit Scoring
- Risk Models
- Fraud Detection
- Machine Learning
- Predictive Analytics

---

# Topics Covered

## 1. Statistical Thinking

Shifted from asking:

"What happened?"

to:

"What is likely to happen?"

Important realization:

Machine Learning is essentially automated probability estimation.

---

# 2. Probability Thinking

Introduced the concept of probability through business questions.

Example:

If:

- 100 customers exist
- 10 customers default

Then:

Probability of Default = 10%

Key insight:

Credit scoring is fundamentally an attempt to estimate the probability that a customer will default.

---

# 3. Delinquency Distribution

Created delinquency buckets:

- Current
- 1–30 DPD
- 31–60 DPD
- 60+ DPD

Implemented:

```python
def delinquency_bucket(days):
```

Purpose:

Transform raw arrears values into meaningful risk categories.

Business Value:

Allows portfolio health analysis and monitoring.

---

# 4. Portfolio Health Analysis

Analyzed:

- current customers,
- delinquent customers,
- defaulted customers.

Questions explored:

- How healthy is the portfolio?
- How much exposure is currently performing?
- How much exposure is deteriorating?

Important realization:

Risk should be monitored continuously.

---

# 5. Exposure Analysis

Moved beyond customer counts.

Analyzed:

```python
groupby("dpd_bucket")
```

to determine:

Exposure by delinquency bucket.

Questions explored:

- Where is the money?
- Which risk buckets hold the most exposure?
- Is portfolio risk concentrated?

Important realization:

Money at risk matters more than customer counts.

---

# 6. Portfolio At Risk (PAR)

Introduced one of the most important banking KPIs.

Example:

PAR30

Definition:

The percentage of portfolio exposure held by customers above 30 Days Past Due.

Calculation:

```python
PAR30 = Exposure above 30 DPD
        ÷
        Total Portfolio
```

Business Value:

Measures portfolio quality and delinquency risk.

Important realization:

PAR is a critical metric used by lending institutions and risk teams.

---

# 7. Mean vs Median

Compared:

- Mean
- Median

Important realization:

Means can be distorted by outliers.

Medians often provide a better representation of customer populations.

Business Example:

A few very wealthy customers can distort average income calculations.

---

# 8. Standard Deviation

Introduced variability measurement.

Questions explored:

- How diverse are our customers?
- How much variation exists within the portfolio?

Interpretation:

Low standard deviation:
- customers behave similarly.

High standard deviation:
- multiple customer segments exist.

Business Value:

Helps determine whether separate scorecards or strategies may be required.

---

# 9. Z-Score Analysis

Introduced anomaly detection using Z-Scores.

Formula:

z = (x - mean) / standard_deviation

Purpose:

Measure how unusual a customer is relative to the population.

Applications:

- fraud detection,
- anomaly detection,
- customer monitoring,
- risk investigations.

Important realization:

Statistics can identify unusual behaviour automatically.

---

# 10. Risk Bucketing

Created risk classifications based on delinquency.

Examples:

- Current
- Watchlist
- High Risk
- Default

Purpose:

Transform raw operational data into business risk signals.

Important realization:

Raw data becomes more valuable when converted into meaningful business features.

---

# 11. Scorecard Development

Introduced scorecard thinking.

Created score bands for:

## Income

Examples:

- Low Income
- Medium Income
- High Income

Converted into points.

## Delinquency

Created points based on:

- current status,
- arrears behaviour,
- delinquency severity.

Important realization:

Credit scoring is often built by assigning points to risk characteristics.

---

# 12. Credit Score Construction

Combined:

- income score,
- delinquency score,

to create:

```python
credit_score
```

Concept:

Features
↓
Points
↓
Score

Important realization:

This mirrors the structure of traditional credit scorecards.

---

# 13. Decision Engine Logic

Converted scores into decisions.

Examples:

- Approve
- Review
- Decline

Implemented:

```python
def score_decision(score):
```

Business Value:

Transforms statistical outputs into operational actions.

Important realization:

The purpose of scoring is decision-making.

---

# 14. Decision Analytics

Analyzed:

- approval volumes,
- review volumes,
- decline volumes.

Questions explored:

- How many customers qualify?
- What exposure is approvable?
- What exposure should be reviewed?
- What exposure should be declined?

Business Value:

Supports lending policy management.

---

# 15. Probability of Default Thinking

Introduced:

```python
default_flag
```

Purpose:

Identify customers likely to default.

Important realization:

This becomes the target variable for future Machine Learning models.

---

# Important Concepts Learned

## Probability

Risk can be expressed as probability.

## Portfolio At Risk

Measures exposure held by delinquent customers.

## Standard Deviation

Measures variability within customer populations.

## Z-Scores

Measure abnormality and unusual behaviour.

## Scorecards

Transform customer characteristics into risk scores.

## Decision Engines

Transform scores into actions.

## Probability of Default

The foundation of modern credit risk modeling.

---

# Key Realizations

- Statistics supports business decisions.
- Risk can be quantified.
- Customer behaviour can be scored.
- Portfolio quality can be measured.
- Scoring systems convert features into decisions.
- Machine Learning extends scorecard concepts using historical data.

---

# Deliverables Completed

## Notebook

day_5_statistics_and_scoring.ipynb

## Delinquency Buckets

Created portfolio risk segmentation.

## PAR Analysis

Calculated portfolio-at-risk metrics.

## Z-Score Analysis

Implemented anomaly detection foundations.

## Credit Scorecard

Built a simplified credit scoring framework.

## Decision Engine

Generated lending recommendations.

## Probability Thinking

Introduced predictive analytics concepts.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Jupyter Notebook
- Git & GitHub

---

# Business & Industry Connections

Day 5 connects directly to:

- Credit Scoring
- Risk Management
- Portfolio Monitoring
- Collections Analytics
- Lending Strategy
- Digital Lending Platforms
- Decision Engines
- Machine Learning Foundations

---

# Final Massive Insight

Today marked another major transition.

The focus moved from:

Understanding Risk

to:

Quantifying Risk.

This is the beginning of scoring and predictive analytics.

Modern lending systems operate using:

Data
↓
Features
↓
Scores
↓
Probability
↓
Decision

This framework powers:

- Credit Scoring Engines
- Fraud Detection Systems
- Risk Models
- Machine Learning Models
- Digital Lending Platforms

---

# Next Session Preview (Day 6)

Topics:

- Feature Engineering
- Behavioral Features
- Risk Features
- Portfolio Features
- Feature Importance
- Preparing Data for Machine Learning

Goal:

Learn how raw data is transformed into predictive signals that can be used by scorecards and machine learning models.