# Health & Fitness App Analytics  
Subscription Metrics • Cohort Retention • Aha! Moment Discovery

## Project Description

This portfolio project delivers end-to-end product and growth analytics for a **health & fitness mobile application** using real-world data sources:

- ~2,000 users  
- subscription records  
- ~28,300 behavioral events  

The analysis combines classical SaaS financial metrics (MRR, churn, LTV), cohort-based retention diagnostics, and behavioral driver discovery to uncover what actually drives long-term user retention and revenue sustainability.

Built entirely in Python (pandas, matplotlib, seaborn) using Jupyter Notebooks.

## Core Business Problems Addressed

1. **Unclear subscription revenue trajectory and retention health**  
   Rapid early MRR growth was accompanied by very high initial churn — making it difficult to assess long-term business viability.

2. **Lack of visibility into retention patterns over time**  
   No clear understanding of how retention decayed across different user signup cohorts or whether product-market fit was improving month over month.

3. **Unknown early behaviors that predict long-term retention**  
   Many possible onboarding actions exist (logging meals, workouts, sessions, profile updates), but it was unclear which early behaviors most strongly predicted users returning after 30 days.

## Solutions Delivered

1. **Subscription Health & Financial KPIs**  
   - Calculated monthly MRR (including new, expansion, contraction, churn components)  
   - Tracked customer & revenue churn rates month-over-month  
   - Computed average ARPU and simple LTV  
   → Uncovered strong revenue scaling together with dramatic churn improvement (from ~20% to ~4% within months)

2. **Cohort-based Retention Analysis**  
   - Assigned monthly cohorts based on first activity timestamp  
   - Built relative-time retention matrix (Month 0, 1, 2, …)  
   - Visualized retention decay using annotated heatmaps  
   → Enabled direct comparison of retention curves across signup periods and identification of typical drop-off points

3. **Aha! Moment & Behavioral Driver Discovery**  
   - Engineered count-based features from the first 7 days (meals logged, workouts logged, sessions started, profile updates)  
   - Measured Pearson correlation with Day 30 retention  
   - Performed binned analysis to quantify uplift by behavior intensity  
   → Identified **logging 2–3 meals in the first week** as the dominant early predictor of 30-day retention (increasing from ~31% baseline to 48–72%+)

## Key Recommendations

| Area                     | Recommendation                                                                                 | Expected Impact Potential |
|--------------------------|------------------------------------------------------------------------------------------------|------------------------|
| Onboarding experience    | Prioritize fast, repeated meal logging in the first week (guided flows, templates, quick wins) | **High**               |
| Early user nudges        | Send targeted reminders/pushes specifically encouraging the 2nd and 3rd meal log               | **High**               |
| Feature sequencing       | Guide users toward meal logging before emphasizing workouts or profile completion              | **Medium–High**        |
| Internal success metric  | Track “meals logged in first 7 days” as a leading indicator / proxy for retention health       | **Medium–High**        |
| Experimentation roadmap  | Run A/B tests of onboarding variants focused on accelerating 2+ meal logs vs current flow     | **High**               |
| Retention segmentation   | Monitor Day 30 retention broken down by early meal-logging behavior                            | **Medium**             |

## Core Insight (One-Liner)

**The moment a user logs their second or third meal in the first week appears to be the strongest “Aha!” moment** — dramatically increasing the probability they will still be active 30 days later.

## Repository Contents

- notebooks → 01_SubscriptionKPIs, 02_Cohort_Analysis, 03_Aha_Moment_Discovery  
- visuals → saved heatmaps, retention curves, bar charts  
- data → users.csv, subscriptions.csv, events.csv (sample or anonymized)
