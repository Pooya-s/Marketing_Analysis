# Octopus Energy: Italian Market Entry Analytics

## Project Overview
[cite_start]This repository contains a comprehensive marketing analytics project designed to evaluate the market positioning and potential growth strategies for Octopus Energy upon its entry into the Italian energy sector[cite: 108]. [cite_start]The analysis utilizes supervised and unsupervised machine learning methods, Natural Language Processing (NLP), and statistical market research techniques to process consumer data and generate actionable business intelligence[cite: 109, 118, 121, 319].

## Repository Structure

* [cite_start]**`/Sentiment_analysis`**: Contains scripts for web scraping and NLP[cite: 374]. 
    * Extracts Trustpilot reviews using Selenium and Chrome WebDriver[cite: 150, 153, 154].
    * [cite_start]Utilizes CountVectorizer for feature extraction and Latent Dirichlet Allocation (LDA) for topic modeling[cite: 326, 329].
    * [cite_start]Applies K-Means clustering to classify reviews into categories: Pricing, Customer Service, and Product Quality[cite: 323, 337, 343].
* **`/Interviews_survey`**: Contains the raw data and structural methodology for the multi-phase data collection process[cite: 408, 120].
    * Details the 12 qualitative interviews used to infer initial attributes[cite: 126, 127].
    * [cite_start]Outlines the 4-section survey design capturing demographics, brand ratings, consumption habits, and conjoint bundles[cite: 379, 380, 389, 398, 406].
* [cite_start]**`/Conjoint_analysis`**: Contains the part-worth utility calculations and market-share simulations[cite: 488, 490].
    * [cite_start]Analyzes consumer preferences across 4 attributes: digital monitoring tools, tariff flexibility, activation speed, and technical assistance[cite: 415, 417, 420, 424].
    * [cite_start]Simulates market share for 4 theoretical tariff plans: Standard, Premium, Low-Cost, and Balanced[cite: 490, 502].
* **`/Segmentation`**: Contains the clustering models used to identify distinct consumer profiles[cite: 525, 576].
    * [cite_start]Implements K-Means (k=4 determined via the elbow method, silhouette score, and Calinski Harabasz score) and Hierarchical clustering[cite: 531, 532, 548].
    * [cite_start]Utilizes t-SNE (t-distributed Stochastic Neighbor Embedding) for clear visualization and dimensionality reduction[cite: 573].
* **`/Comparative_positioning`**: Contains the code and data for analyzing brand perception[cite: 1018].
    * Generates two-dimensional perceptual maps to compare Octopus Energy against established competitors (Enel, A2A)[cite: 642, 916].
    * [cite_start]Evaluates brands across dimensions such as Popularity, Sustainability, Pricing, and Clarity of Contract[cite: 861].
* [cite_start]**`/Complementary`**: Contains advanced predictive and attribution models[cite: 1092].
    * **RFM Analysis:** Segments customers based on Recency, Frequency, and Monetary value[cite: 1020, 1021].
    * [cite_start]**Marketing Attribution:** Compares Last-Click, Shapley, and Markov models over a 30-day window to evaluate channel effectiveness[cite: 1042].
    * [cite_start]**Churn Prediction:** Deploys Support Vector Machine (SVM) and Logistic Regression models (with 5-fold cross-validation) on preprocessed and scaled customer subscription data[cite: 1088, 1089].

## Installation & Usage

[cite_start]To run the notebooks and scripts in this repository, you will need a standard Python data science environment[cite: 152]. 

1. [cite_start]**Web Scraping:** `selenium` is required for automating browser interactions, alongside a compatible Chrome WebDriver instance[cite: 150, 153, 154].
2. [cite_start]**Data Manipulation:** `pandas` is used extensively for cleaning data and formatting DataFrames[cite: 164].
3. [cite_start]**Machine Learning & NLP:** `scikit-learn` is required for executing the analytical models, including CountVectorizer, LDA, K-Means clustering, PCA, t-SNE, StandardScaler, SVM, and Logistic Regression[cite: 326, 329, 337, 572, 573, 1088, 1089].

## Key Business Insights

### Marketing Channel Attribution
[cite_start]A multi-touch attribution analysis utilizing Last-Click, Shapley Value, and Markov models revealed that Referral and Organic Search are the dominant drivers of conversions[cite: 1042, 1045]. [cite_start]Direct traffic's value is more accurately captured when accounting for multi-touch journeys (Markov)[cite: 1048]. 

| Channel | Last-Click Attribution | Shapley Value | Markov Model |
| :--- | :--- | :--- | :--- |
| **Referral** | 45.06% | 43.68% | 42.40% |
| **Organic Search** | 30.67% | 31.06% | 31.11% |
| **Direct** | 16.85% | 18.40% | 18.98% |
| **Paid Search** | 4.24% | 4.48% | 4.35% |
[cite_start]*(Data extracted from attribution model comparison)* [cite: 1048, 1056, 1059, 1061, 1062, 1064, 1065]

### RFM Customer Segmentation
[cite_start]Transactional data was analyzed to classify customers based on purchasing behavior (Recency, Frequency, Monetary value)[cite: 1020, 1021]. [cite_start]The analysis highlights that a few high-value customers contribute significantly to revenue, requiring targeted retention strategies[cite: 1025].

| Customer Segment | Share of Base | Count | Strategic Recommendation |
| :--- | :--- | :--- | :--- |
| **Others** | 68.1% | 88,429 | General monitoring and retention. |
| **Big Spenders** | 13.5% | 17,524 | - |
| **Lost Cheap Customers** | 5.4% | 7,005 | - |
| **Best Customers** | 5.3% | 6,918 | Nurture with exclusive rewards. |
| **Almost Lost** | 3.6% | 4,613 | Deploy re-engagement strategies. |
| **Lost Customers** | 2.6% | 3,406 | Deploy re-engagement strategies. |
| **Loyal Customers** | 1.5% | 1,956 | Nurture with exclusive rewards. |
[cite_start]*(Data extracted from Customer Segmentation status distribution)* [cite: 1026, 1029, 1030, 1033, 1034, 1035]

### Market Positioning & Consumer Priorities
* **Positioning:** Octopus Energy currently exhibits low brand popularity and a weak sustainability perception compared to incumbent providers[cite: 1010]. Strategic marketing investments and rebranding campaigns are required to improve brand awareness and environmental positioning[cite: 1017].
* [cite_start]**Consumer Priorities:** Across multiple analytical models and consumer segments, efficient technical assistance emerged as a critical factor in consumer decision-making and utility maximization[cite: 422, 600, 627, 638].
