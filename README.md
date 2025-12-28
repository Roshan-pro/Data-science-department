# 📊 Uber Ride Analytics – Statistical Hypothesis Testing

# **📌 Project Overview**
This project analyzes Uber ride data from 2024 to answer key business questions using statistical hypothesis testing. The dataset contains 148,770 bookings with information on booking values, payment methods, ride times, distances, and booking statuses.

# 🔍 Key Questions Investigated
**1. Average Booking Value Check**
  - **Question:** Is the average booking value significantly higher than ₹350?
  - **Method:** One-sample t-test
  - **Result:** ✅ Yes – Average booking value (₹508.30) is significantly higher than ₹350 (p <     0.05)
  - **Confidence Interval:** ₹312.94 to ₹646.76

**2. Payment Method Comparison**
  - **Question:** Does booking value differ between UPI and Cash payments?
  - **Method:** Independent t-test + Mann–Whitney U test
  - **Result:** ✅ No significant difference found between payment methods

**3. System Update Impact**
  - **Question:** Did average vehicle arrival time (VTAT) reduce after a system update?
  - **Method:** Wilcoxon signed-rank test (paired before/after analysis)
  - **Result:** ✅ No significant reduction – System update didn't improve arrival times

**4. Payment & Booking Status Relationship**
  - **Question:** Is there an association between payment method and booking status?
  - **Method:** Chi-square test of independence
  - **Result:** ✅ No significant association found

**5. Distance vs Fare Analysis**
  - **Question:** Does ride distance affect fare amount?
  - **Method:** Spearman's rank correlation
  - **Result:** ✅ No significant correlation found

# 📁 Dataset Details
  - Source: Kaggle – [Uber Ride Analytics Dashboard](https://www.kaggle.com/datasets/yashdevladdha/uber-ride-analytics-dashboard/data)
  - Records: 148,770 bookings
  - Time Period: 2024
  - Missing Values: 7.49% (handled via removal for analysis)
  - Key Variables: Booking Value, Payment Method, Avg VTAT, Ride Distance, Booking Status

# 🛠️ Technical Implementation
**Libraries Used**
```
import pandas as pd
import numpy as np
import scipy.stats as stats
from scipy.stats import wilcoxon, mannwhitneyu, chi2_contingency, spearmanr
import seaborn as sns
import matplotlib.pyplot as plt
```

## Statistical Tests Applied
  - One-sample t-test
  - Independent t-test
  - Mann–Whitney U test
  - Wilcoxon signed-rank test
  - Chi-square test
  - Spearman's correlation

# 📊 Key Findings Summary


| Question                         | Test Used                     | Result | Business Insight                                   |
|----------------------------------|-------------------------------|--------|---------------------------------------------------|
| Booking Value > ₹350?            | One-sample t-test             | ✅ Yes | Average ride value is healthy                     |
| UPI vs Cash difference?          | T-test + Mann–Whitney U       | ❌ No  | Payment method doesn't affect booking value       |
| VTAT improved after update?      | Wilcoxon Signed-Rank Test     | ❌ No  | System update didn’t reduce waiting time          |
| Payment affects booking status?  | Chi-square test               | ❌ No  | Payment choice doesn’t impact completion status   |
| Distance affects fare?           | Spearman Correlation          | ❌ No  | Fare is not strongly tied to distance             |

# 📚 References
  - **Dataset:** [Uber Ride Analytics Dashboard on Kaggle](https://www.kaggle.com/datasets/yashdevladdha/uber-ride-analytics-dashboard/data)
  - **Statistical Methods:** [Scipy Documentation](https://docs.scipy.org/doc/scipy/)
  - **Visualization:** [Seaborn](https://seaborn.pydata.org/) & [Matplotlib](https://matplotlib.org/stable/index.html)
