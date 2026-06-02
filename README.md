# Loan-Default-Risk-Analysis
In this project, we explore borrower demographics, loan characteristics, and repayment outcomes to identify the key risk factors that predict loan defaults. 

# Project Overview

Horizon Financial Group is a mid-size consumer lending company.

The Management is concerned about the rising default rate on personal loans and wants data-driven insights to improve the underwriting process. 

In this project, I explore borrower demographics, loan characteristics, and repayment outcomes to identify the key risk factors that predict loan defaults.

The project addresses about the rising default rate on personal loans and gives data-driven insights to improve the underwriting process.

#Table of Contents

Project background
Project Description
Workflow
Tech-Stack
Insights
Recommendations


# Project:

# Background
Horizon Financial Group is a mid-size consumer lending company. Management is concerned about the rising default rate on personal loans and wants data-driven insights to improve the underwriting process.

In this project we will explore borrower demographics, loan characteristics, and repayment outcomes to identify the key risk factors that predict loan defaults.

# Description
Horizon Financial Group has issued over 600 personal loans across 2024 and 2025. The company has noticed that roughly 1 in 4 loans are defaulting, which is well above their target of 12%. 

The VP of Risk has asked me to analyse the existing loan book and borrower data to answer key questions about what is driving defaults. 
My analysis will directly inform changes to their credit scoring model and loan approval thresholds. 

# Workflow

- Imported and Explored (both datasets)
Loaded both CSVs.
Checked for nulls, data types, and basic stats.
Joined the two tables on borrower id.

- Segment Analysis:
Created credit score buckets and calculate default rates for each.
Did the same for DTI ranges, employment status, and loan purpose.

- Correlation Analysis:
Identified which numeric variables (credit score, DTI, income, loan amount, interest rate) have the strongest correlation with defaults.

- Visualization:
Built charts showing default rate by credit score range, a scatter plot of DTI vs. default status, and a bar chart comparing loan purposes.
Outcomes

# Tech-Stack:

Python-Pandas

# Insights:

Overall Default Rate:
The overall default rate across all loan applications is 24.29%.

1. Credit Score(View [HERE](https://github.com/DataDonRowam23/Loan-Default-Risk-Analysis/blob/main/CR%20score%20Default%20rate%20Bar%20chart.jpg))
   
Highest Risk Segment: 

The credit score range of 300 599 has the highest default rate at 49.14%.

Lower Risk Segments:

Default rates significantly decrease with higher credit scores: 600 649 (29.03%), 650 699 (28.00%), 700 749 (16.28%), and 750+ (11.69%).


2. Debt-to-Income (DTI) Ratio:(View HERE)
   
Relationship:

There is a clear relationship between DTI and default likelihood. 

Borrowers with a DTI of 45%+ exhibit a significantly higher default rate of 39.58%, compared to lower DTI ranges (e.g., 0 15% at 21.05%, 16 25% at 24.81%).

3. Loan Purpose:(View HERE)
   
Highest Risk Purposes: 

Loans for Wedding (32.14%), Home Improvement (28.57%), and Auto Loan (27.12%) show the highest default rates.

Average Loan Amounts (Defaulted vs. Non-Defaulted): For some high-risk purposes, the average loan amount for defaulted loans is notably higher than for non-defaulted loans (e.g., Debt Consolidation: $29,036 for defaulted vs. $$29,036 for defaulted vs. $21,030 for non-defaulted; Education: $29,183 vs. $$29,183 vs. $17,114; Medical Expenses: $30,421 vs. $$30,421 vs. $21,298. However, for others, the pattern is reversed (e.g., Auto Loan: $22,643 vs. $$22,643 vs. $18,404 for defaulted vs. non-defaulted respectively).

This suggests that higher loan amounts for specific purposes may be a contributing factor to default.

4. Employment Status and Years Employed:

Employment Status:
While there are variations, all employment statuses show significant default rates (ranging from 22.73% for 'Contract' to 27.69% for 'Part-Time'). 

There isn't a stark difference between employment types, suggesting that employment *status alone* might not be the strongest predictor of default compared to other factors like credit score.

Years Employed:

Borrowers with less than 2 years of employment have a default rate of **34.52% (n=84), which is notably higher than the overall default rate of 24.29%.

# Recommendations:

1. Implement a minimum credit score threshold of 700. Loans to borrowers with credit scores below 700 should be subject to stricter scrutiny or additional qualifying criteria, given the notable increase in default rates below this threshold.

2. Set a maximum DTI threshold of 45%. Applicants with DTI ratios exceeding 45% should generally be declined, or at minimum, require extensive additional risk mitigation factors.
   
3. Apply stricter underwriting standards or higher interest rates for loans purposed for Wedding, Home Improvement, Education, Debt Consolidation, and Medical Expenses, especially when the loan amount is higher than the average for that purpose.
   
4. Years Employed Threshold: Implement a minimum employment history requirement, perhaps requiring at least 2 years of continuous employment for standard loan approvals. Applicants with less than 2 years of employment should undergo enhanced risk assessment, potentially facing stricter eligibility criteria, lower loan amounts, or higher interest rates due to their significantly elevated default risk.
