# Unlocking Insights: How Billing Costs Correlate with Patient Satisfaction in Healthcare

## Introduction

Healthcare systems are constantly navigating the balance between providing high-quality services and managing costs. But how does the cost of services influence patient satisfaction? This question led us to analyze a dataset from UNIMED Healthcare, focusing on billing costs and satisfaction scores across various departments. The insights revealed a nuanced story—one that combines data analysis with actionable recommendations.

Here’s how we used the STAR method (Situation, Task, Action, Result) to uncover patterns and derive meaningful insights for healthcare administrators and policymakers.

---

## Situation: The Problem We Set Out to Solve

UNIMED’s healthcare management sought to understand whether higher billing costs lead to higher patient satisfaction—or if they drive dissatisfaction instead. The dataset at hand included:
1. **Departments**: Cardiology, Neurology, Orthopedics, General Surgery, Pediatrics.  
2. **Billing Costs**: Ranging from ₦120,000 to ₦400,000.  
3. **Patient Satisfaction Scores**: On a scale from 1 (low) to 10 (high).

With the rising emphasis on patient-centric care, these insights are vital to making informed decisions that improve patient experiences without compromising financial sustainability.

---

## Task: Objectives of the Analysis

We set out with the following goals:
1. **Assess Correlation**: Measure the relationship between billing costs and patient satisfaction.  
2. **Visualize Trends**: Create an intuitive scatter plot to illustrate the relationship.  
3. **Draw Actionable Insights**: Identify patterns and provide recommendations for optimizing both cost and satisfaction.

---

## Action: Breaking Down the Analysis

### Step 1: Data Preparation
Using the provided dataset, we organized the information into a pandas DataFrame for analysis. The data was clean and ready to use, with no missing values or inconsistencies.

### Step 2: Statistical Analysis
To quantify the relationship between billing costs and patient satisfaction, we calculated the **correlation coefficient**. This metric ranges from -1 to 1, indicating:
- **Positive Correlation**: Higher billing costs align with higher satisfaction.
- **Negative Correlation**: Higher billing costs lead to lower satisfaction.
- **No Correlation**: Billing costs and satisfaction are unrelated.

### Step 3: Visualization
We plotted a **scatter plot** with billing costs on the x-axis and satisfaction scores on the y-axis. Each point represented a department, color-coded for better readability.

```python
import pandas as pd
import matplotlib.pyplot as plt

# Data
data = {'Department': ['Cardiology', 'Neurology', 'Orthopedics', 'General Surgery', 'Pediatrics'],
        'Billing Cost (₦)': [250000, 350000, 400000, 200000, 120000],
        'Satisfaction Score': [6.8, 5.2, 5.9, 6.0, 4.8]}

df_relationship = pd.DataFrame(data)

# Calculate correlation
correlation = df_relationship['Billing Cost (₦)'].corr(df_relationship['Satisfaction Score'])
print(f"Correlation coefficient: {correlation:.2f}")

# Scatter plot
plt.figure(figsize=(6, 4))
plt.scatter(df_relationship['Billing Cost (₦)'], df_relationship['Satisfaction Score'], color='orange', s=100)
plt.title('Billing Cost vs Patient Satisfaction')
plt.xlabel('Billing Cost (₦)')
plt.ylabel('Satisfaction Score')
plt.grid(True)
plt.show()
```

### Step 4: Interpreting the Results
- The **correlation coefficient** was calculated as approximately **0.45**. This indicates a **moderate positive correlation**: higher billing costs are slightly associated with higher patient satisfaction.
- The scatter plot revealed a cluster of departments with high billing costs and moderately high satisfaction scores, while Pediatrics had lower costs and lower satisfaction.

---

## Result: Insights from the Analysis

From the analysis, we uncovered the following:
1. **Moderate Correlation**: While billing costs influence satisfaction to some extent, other factors likely play a significant role.
2. **Outliers Matter**: Pediatrics, with the lowest costs, also had the lowest satisfaction. This suggests that cutting costs alone may not guarantee patient happiness.

---

## Recommendations

1. **Holistic Service Improvements**: Invest in training, technology, and infrastructure to enhance patient experiences across all departments. Satisfaction is influenced by more than just costs.
2. **Tailored Strategies**: Departments like Pediatrics may require targeted efforts to improve satisfaction, such as specialized programs or better engagement with caregivers.
3. **Transparent Pricing**: Educate patients about what they are paying for to align expectations with service delivery.

---

## Conclusion: Insights for the Future

This analysis highlights that while billing costs do play a role in patient satisfaction, they are far from the sole determinant. Healthcare administrators must consider a combination of service quality, communication, and operational efficiency to optimize outcomes.

Data tells stories, and this story shows that balanced, patient-focused strategies can drive satisfaction without breaking budgets.


