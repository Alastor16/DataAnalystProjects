# AAB Test Project

## Overview
This project focuses on conducting an AAB test to evaluate user behavior and analyze a sales funnel. The dataset includes user interactions categorized into three groups: Group A (split into two for A/A testing) and Group B. The primary objective is to identify statistical differences between the groups and evaluate the effectiveness of a new letter style in influencing conversion rates.

The analysis involves defining the sales funnel, understanding user behavior at each stage, and determining if the new letter style impacts user retention or conversion. The funnel includes these key events:

1. **Main screen appears**
2. **Offer screen appears**
3. **Cart screen appears**
4. **Payment successful**

A non-core event, "Tutorial," is excluded from the funnel as it is not relevant to the majority of users.

---

## Tools Used
- Python
- Statistical Analysis Packages

---

## Steps Undertaken

### 1. Data Cleaning and Preparation
- Inspected the dataset for anomalies or missing values.
- Cleaned data to ensure consistency and accuracy, particularly for unique user counts and event tracking.

### 2. Preliminary Analysis
- Analyzed the total number of users, their activity levels, and distribution across events.
- Identified key drop-off points in the funnel based on user retention rates between stages.

### 3. Sales Funnel Analysis
Defined the funnel stages and calculated user retention and drop-off rates:
- **Visitors to Offer Screen:** 56% retention (4201 out of 7419 unique visitors)
- **Offer to Cart:** 42% retention (1767 out of 4201) 
- **Cart to Payment:** 25% retention (454 out of 1767)

The most significant drop-off was observed at the cart-to-payment stage, warranting closer investigation.

### 4. AAB Test Analysis
The AAB test compared the three groups:
- Checked for population balance in groups A (split into A1 and A2 for A/A testing) and B.
- Evaluated statistical significance between A1 and A2 to confirm randomization quality.
- Analyzed user behaviors and event popularity across groups, with a particular focus on conversion rates.

---

## Key Findings and Analysis

### Summary of Observations
- High drop-off rates were observed at the cart-to-payment stage, a critical point for user retention.
- The AAB test showed no statistically significant differences between A1 and A2 groups, confirming proper randomization.
- No significant differences were found between Group A and Group B, indicating that the new letter style did not influence user behavior or conversions.

### AAB Test Results
Conversion rates and behaviors remained consistent across groups. The experiment failed to demonstrate an advantage for the new letter style, with no evidence of it improving retention or purchase likelihood.

---

## Conclusions

### 🔍 Key Findings
- The AAB test showed no statistically significant impact of the new letter style on user behavior or conversion rates.
- The sales funnel analysis highlighted a critical drop-off point at the cart-to-payment stage, which requires further investigation to improve conversions.

### 🎯 Relation to Objectives
- The analysis addressed the project's primary goals by evaluating the effectiveness of the new letter style and examining the user journey through the sales funnel.

### 🚀 Recommendations
- Discontinue the current AAB test as it does not provide any actionable advantage or insights regarding the new letter style.
- Focus future efforts on understanding and addressing the high drop-off rates at the cart-to-payment stage.

### 📝 Final Thoughts
This project underscores the importance of funnel optimization over cosmetic changes like letter styles. To improve conversion rates, consider investigating factors like cart usability, payment process friction, or alternative incentives to reduce drop-offs.
