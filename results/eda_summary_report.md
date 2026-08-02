## Automated EDA Insights Summary
*Generated from n=442 events (BSAI excluded, RKTO held out).*

### A. Correlation Analysis
- No numeric predictor shows more than a weak association with CAR_short (max |r| = 0.24, variable: alpha).
- Strongest positive association: **rd_intensity** (Spearman r = 0.175, weak).
- Strongest negative association: **alpha** (Spearman r = -0.236, weak).
- This absence of strong bivariate correlation is *consistent with* RQ3's near-zero R-squared -- no single continuous feature meaningfully explains CAR_short in isolation, which supports rather than contradicts the regression finding.

### B. Sector-Wise Comparison
- Kruskal-Wallis across sectors with n>=5 finds no statistically significant difference in CAR_short (H=11.50, p=0.243).
- Highest median CAR_short: **Healthcare** (1.47%, n=73).
- Lowest median CAR_short: **Basic Materials** (-9.04%, n=5).
- Interpretation should stay descriptive: this sector-level view is exploratory and does not replace RQ4's confirmatory tech/non-tech test.

### C. Temporal Patterns
- Event volume by year: {2024: 97, 2025: 176, 2026: 169} (activity has increased over the sample window).
- Mean CAR_short by year: 2024: 2.95%, 2025: -1.74%, 2026: 1.17%.
- The sign of the average yearly reaction changes 2 time(s) across 2024-2026, indicating the market's response to AI announcements has not been stable over the sample window -- worth flagging as a limitation on generalizing a single pooled CAAR across the full period.

### D. Feature Relationships
- **rd_intensity** shows a statistically significant association with CAR_short (r=0.175, p=0.003).

### E. Sector x Announcement-Type Interaction
- Highest mean CAR_short combination: **partnership** announcements from **Technology** firms (9.11%).
- Lowest mean CAR_short combination: **partnership** announcements from **Non-Technology** firms (-2.92%).
- This pattern is descriptive context for RQ3's formal interaction test, not a substitute for it (cell sizes are uneven and this view is unadjusted for firm size as a continuous variable).