# econometric-models-quantile-heterogeneity-logit

# **Predictive Analytics: Quantile Analysis, Treatment Effect Heterogeneity, and Logit Models with Stata**

This project applies various econometric models and causal inference techniques using **Stata** to analyze key business and behavioral metrics. The objectives include assessing content engagement at different quantiles, testing for heterogeneity in treatment effects, and estimating the probability of passing an exam using logit models.

---

## **Technologies Used**
**Stata**:
Statistical software used to perform various analyses including quantile regressions, hypothesis testing, and logistic regressions.

**Quantile Analysis (Exploratory Causal Analysis)**:
Examines how a specific percentile of a distribution (e.g., 80th percentile) responds to changes, offering insights into retention and engagement strategies.

**Heterogeneity Testing (Causal Inference Technique)**:
Tests for variation in treatment effects across groups, helping isolate differential impacts of new content strategies.

**Logistic Regression (Logit) with Marginal Effects (Causal Inference Technique)**:
Models binary outcomes (e.g., pass/fail) while keeping predicted probabilities within the valid range of 0 to 1. Marginal effects show how incremental changes in predictors affect the likelihood of success.



---

## **Project Overview**

### **1. Content Engagement Analysis (Amazon Data)**
- **Goal**: Evaluate how new content affects viewing time for high-consumption customers (e.g., those at the 80th percentile).
- **Key Findings**:  
  - New content leads to a 46-minute increase in viewing time for customers at the 80th percentile.  
  - Amazon may prioritize lower percentiles for intervention to retain customers with lower initial engagement levels.

---

### **2. Testing for Heterogeneity in Treatment Effects**
- **Goal**: Assess whether the effects of new content vary across different customer groups.  
- **Methodology**: Variance ratio test using `sdtest ViewTime, by(NewContent)`.
- **Key Findings**:  
  - The test reveals a variance ratio of **0.4454** with a **p-value of 0**, indicating significant heterogeneity in treatment effects.

---

### **3. Exam Performance Analysis (Pass/Fail Data)**
- **Goal**: Model the probability of passing a test based on hours studied using a logit model.
- **Models Used**:
  - **Logit Regression**: Predicts binary outcomes with bounded probabilities between 0 and 1.
  - **Marginal Effects**: Calculates the impact of additional study hours on passing probability.

- **Key Findings**:  
  - Each additional hour of study increases the probability of passing by **11.7%** on average.  
  - From 5 to 6 hours studied, the probability increases by **0.434%**.  
  - From 14 to 15 hours, it increases by **1.08%**, suggesting diminishing returns at higher study hours.

---

## **Data Overview**

The project uses two datasets:

1. **Amazon Content Engagement Data**:  
   Contains viewing time and content information, segmented by treatment (new content exposure).

2. **Test Pass/Fail Data**:  
   Includes hours studied and test outcomes to model binary probabilities.

---

## **Results Summary**

### **Content Engagement**
- High-engagement customers (80th percentile) show a significant increase in viewing time due to new content.
- Amazon may prioritize lower engagement levels to reduce churn.

### **Treatment Effect Heterogeneity**
- The ratio of variances confirms significant differences between treatment groups, rejecting the hypothesis of no heterogeneity.

### **Exam Performance**
- The logit model indicates that study hours have a diminishing but positive effect on the probability of passing.
- Marginal effects highlight the varying impact of study time across different hour ranges.
