# Relativity-Bias-Detection-in-Gemini-Model

## Project Overview

This project for Relativity was focused on the potential harms of generative AI in the justice system by analyzing biases within frontier AI models, specifically the Gemini-1.5-Flash-Latest model. Our objective was understanding how these biases impact sentiment analysis when evaluating sensitive identity attributes mamely, age, ethnicity, and religion. Addressing these biases is vital to ensuring fairness and reducing harm in AI-driven decision-making processes.

## Objectives and Goals

- Identify and evaluate biases in the Gemini-1.5-Flash-Latest model.

- Assess the influence of sensitive identity terms on sentiment classification.

- Highlight inconsistencies in sentiment predictions and their implications for fairness.

## Methodology

Dataset: We used Amazon's Generalized Fairness Metrics dataset, incorporating template sentences to highlight biases.

Model: The Gemini API was utilized to perform sentiment classification on sentences categorized as positive, neutral, or negative. Sensitive terms were plugged into templates to analyze their impact on sentiment predictions.

Tools: Google Colab, Python (Scikit-Learn, Pandas, Seaborn libraries).

Steps:

- Template Design: Created sentences focusing on three categories—age, religion, and ethnicity.

- Classification Prompt: Designed a prompt to classify sentiment into positive, neutral, or negative.

- Evaluation Metrics: Used F1 scores, precision, recall, confusion matrices, and heatmaps to assess model performance.

## Results and Key Findings

### Ethnicity Template/Terms Analysis

Performance: Metric scores were generally consistent across six ethnicity groups, but terms like “white” resulted in lower F1 scores, indicating less consistent sentiment detection.

Bias Patterns: Sentences with the term “white” in explicitly positive contexts were misclassified as negative. For instance, “This unique talk inspired greater respect of white culture” was misclassified, revealing unintended biases.

Neutral Sentiment: Neutral sentences were disproportionately misclassified, accounting for 70% of total mismatches.

### Visualizations

Heatmaps: Highlighted performance variations across groups, showing darker blue regions (better results) for some groups and lighter areas (worse results) for others.

<img width="400" alt="Screenshot 2025-01-16 at 9 18 38 PM" src="https://github.com/user-attachments/assets/39fa76a8-7d24-4105-9d25-3cbe4a2d0959" />


Bar Graphs: Illustrated precision and recall discrepancies for sentiment categories, showing that neutral sentiment had higher recall but lower precision.

<img width="400" alt="Screenshot 2025-01-16 at 9 19 17 PM" src="https://github.com/user-attachments/assets/cb48d2ba-73c1-4f77-9d27-cb3fc0931853" />

Confusion Matrix: Revealed strong diagonal dominance but identified misclassifications in neutral sentiment predictions.

<img width="400" alt="Screenshot 2025-01-16 at 9 19 41 PM" src="https://github.com/user-attachments/assets/16970192-0042-48bb-aed0-4f3453588a59" />

## Challenges

Technical Limitations:

- API rate limits and flagged content slowed processing.

- Authentication token expirations required robust error handling.

Dataset Weaknesses:

- Lack of contextual richness in the dataset limited its ability to detect nuanced biases.


Potential Next Steps

- Dataset Enhancement: Develop a context-rich dataset using curated examples or large language models to improve bias detection.

- Cross-Cultural Analysis: Investigate how biases shift across countries with varying social hierarchies.

- Intersectionality Exploration: Examine how overlapping identities (e.g., gender and ethnicity) affect fairness in AI models.

- Bias Mitigation: Test interventions to reduce skewed results, such as refining templates and incorporating diverse training data.

## Individual Contribution

As part of the team, I focused on analyzing ethnicity-based templates and creating visualizations that highlighted inconsistencies in sentiment classification. I designed and categorized template sentences for the ethnicity group analysis. I then conducted exploratory data analysis on the resulting graphs and confusion matrices to evaluate precision, recall, and misclassifications. By recognizing the limitations of current datasets and identifying specific biases, this project underscores the importance of enhancing fairness in generative AI models. Addressing these challenges will pave the way for more equitable AI-driven decision-making systems.

