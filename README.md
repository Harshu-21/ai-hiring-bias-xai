⚖️ Auditing Bias in AI Hiring Systems using Fairness Metrics
📌 Project Overview

AI-driven hiring systems are increasingly used to screen resumes and support recruitment decisions. While these systems can improve efficiency, they also risk introducing or amplifying bias, especially when trained on imperfect or incomplete data.

This project focuses on auditing bias in an AI-based hiring model, evaluating its fairness across demographic groups, and applying bias mitigation strategies to improve equitable outcomes.

Rather than optimizing for accuracy alone, the project emphasizes:

Fairness

Explainability

Responsible AI practices

🎯 Objectives

The main goals of this project are:

Build a baseline hiring prediction model

Identify bias across demographic groups using formal fairness metrics

Quantify unfairness using:

Demographic Parity

Disparate Impact

Equal Opportunity (True Positive Rate)

Apply a bias mitigation strategy

Compare before vs after fairness outcomes

📌 Dataset Description

The dataset represents resume-level candidate information used for hiring decisions, including:

Years of experience

Education and skills information

AI-generated resume score

Project count

Salary expectation

📌 Important Notes on the Dataset

The original dataset contained only positive hiring decisions

To enable supervised learning and fairness auditing:

Controlled negative samples were introduced

A synthetic gender attribute was added solely for fairness analysis

All such assumptions are explicitly documented and used only for methodological demonstration

This approach is common in research-oriented fairness audits.

📌 Methodology
1️⃣ Data Preprocessing

Standardized column names

Encoded target variable

Added synthetic demographic attribute

Introduced controlled negative samples

Generated a final, locked dataset

2️⃣ Exploratory Data Analysis (EDA)

Analyzed hiring distribution

Compared feature distributions

Observed differences across demographic groups

Formulated a bias hypothesis

3️⃣ Baseline Model

Logistic Regression used as an interpretable baseline

Automatic feature type detection

Pipeline-based preprocessing (scaling + encoding)

Evaluation using accuracy and confusion matrix

4️⃣ Fairness Evaluation

Bias was evaluated using the following metrics:

Demographic Parity
Measures differences in selection rates across groups

Disparate Impact
Ratio of minimum to maximum selection rate

Equal Opportunity (TPR)
Measures fairness in correctly selecting qualified candidates

Group-wise accuracy was also analyzed for completeness.

5️⃣ Bias Mitigation

A simple and defensible mitigation strategy was applied:

Removal of the protected attribute from training features

This approach evaluates how much bias is directly influenced by sensitive attributes.

6️⃣ Before vs After Comparison

Fairness metrics were computed:

Before mitigation

After mitigation

Results were compared to assess:

Reduction in disparity

Trade-offs between fairness and performance

📌 Key Findings

The baseline model exhibited unequal selection rates across demographic groups

Disparate Impact values indicated potential bias

After mitigation:

Selection rates became more balanced

Equal Opportunity improved

A small fairness–accuracy trade-off was observed

These results highlight the importance of evaluating models beyond accuracy.

📌 Key Takeaways

Bias can exist even in models with reasonable accuracy

Fairness metrics are essential for auditing real-world AI systems

Simple mitigation strategies can significantly improve equity

Responsible AI requires measurement, transparency, and iteration

📌 Technologies Used

Python

Pandas

NumPy

Scikit-learn

Matplotlib

📌 Future Work

Apply advanced mitigation techniques (reweighing, threshold optimization)

Add explainability using SHAP values

Extend analysis to additional protected attributes

Evaluate long-term fairness vs performance trade-offs

📌 Final Note

This project is intended as a responsible AI case study, demonstrating how fairness auditing and mitigation can be systematically integrated into machine learning workflows.

It emphasizes thinking critically about AI systems, not just building them.
