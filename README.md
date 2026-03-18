# Octopus Energy: Italian Energy Market Analytics

## Project Overview
 This repository contains a comprehensive marketing analytics project designed to evaluate the market positioning and potential growth strategies for Octopus Energy .  The analysis utilizes supervised and unsupervised machine learning methods, Natural Language Processing (NLP), and statistical market research techniques to process consumer data and generate actionable business intelligence. For a deeper understanding please read the report file.

## Repository Structure

*  **`/Sentiment_analysis`**: Contains scripts for web scraping and NLP. 
    * Extracts Trustpilot reviews using Selenium and Chrome WebDriver.
    *  Utilizes CountVectorizer for feature extraction and Latent Dirichlet Allocation (LDA) for topic modeling.
    *  Applies K-Means clustering to classify reviews into categories: Pricing, Customer Service, and Product Quality.
* **`/Interviews_survey`**: Contains the raw data and structural methodology for the multi-phase data collection process.
    * Details the 12 qualitative interviews used to infer initial attributes.
    *  Outlines the 4-section survey design capturing demographics, brand ratings, consumption habits, and conjoint bundles.
*  **`/Conjoint_analysis`**: Contains the part-worth utility calculations and market-share simulations.
    *  Analyzes consumer preferences across 4 attributes: digital monitoring tools, tariff flexibility, activation speed, and technical assistance.
    *  Simulates market share for 4 theoretical tariff plans: Standard, Premium, Low-Cost, and Balanced.
* **`/Segmentation`**: Contains the clustering models used to identify distinct consumer profiles.
    *  Implements K-Means (k=4 determined via the elbow method, silhouette score, and Calinski Harabasz score) and Hierarchical clustering.
    *  Utilizes t-SNE (t-distributed Stochastic Neighbor Embedding) for clear visualization and dimensionality reduction.
* **`/Comparative_positioning`**: Contains the code and data for analyzing brand perception.
    * Generates two-dimensional perceptual maps to compare Octopus Energy against established competitors (Enel, A2A).
    *  Evaluates brands across dimensions such as Popularity, Sustainability, Pricing, and Clarity of Contract.
*  **`/Complementary`**: Contains advanced predictive and attribution models.
    * **RFM Analysis:** Segments customers based on Recency, Frequency, and Monetary value.
    *  **Marketing Attribution:** Compares Last-Click, Shapley, and Markov models over a 30-day window to evaluate channel effectiveness.
    *  **Churn Prediction:** Deploys Support Vector Machine (SVM) and Logistic Regression models (with 5-fold cross-validation) on preprocessed and scaled customer subscription data.

## Installation & Usage

 To run the notebooks and scripts in this repository, you will need a standard Python data science environment. 
 For the Conjoint Analysis (R): Ensure you have an R environment configured with these packages installed:
"
 `radiant`
 `tidyverse`
 `reshape2`
 `readxl`
"
1.  **Web Scraping:** `selenium` is required for automating browser interactions, alongside a compatible Chrome WebDriver instance.
2.  **Data Manipulation:** `pandas` is used extensively for cleaning data and formatting DataFrames.
3.  **Machine Learning & NLP:** `scikit-learn` is required for executing the analytical models, including CountVectorizer, LDA, K-Means clustering, PCA, t-SNE, StandardScaler, SVM, and Logistic Regression.

## Key Business Insights

### Marketing Channel Attribution
 A multi-touch attribution analysis utilizing Last-Click, Shapley Value, and Markov models revealed that Referral and Organic Search are the dominant drivers of conversions.  Direct traffic's value is more accurately captured when accounting for multi-touch journeys (Markov). 

| Channel | Last-Click Attribution | Shapley Value | Markov Model |
| :--- | :--- | :--- | :--- |
| **Referral** | 45.06% | 43.68% | 42.40% |
| **Organic Search** | 30.67% | 31.06% | 31.11% |
| **Direct** | 16.85% | 18.40% | 18.98% |
| **Paid Search** | 4.24% | 4.48% | 4.35% |
 *(Data extracted from attribution model comparison)* 

### RFM Customer Segmentation
 Transactional data was analyzed to classify customers based on purchasing behavior (Recency, Frequency, Monetary value).  The analysis highlights that a few high-value customers contribute significantly to revenue, requiring targeted retention strategies.

| Customer Segment | Share of Base | Count | Strategic Recommendation |
| :--- | :--- | :--- | :--- |
| **Others** | 68.1% | 88,429 | General monitoring and retention. |
| **Big Spenders** | 13.5% | 17,524 | - |
| **Lost Cheap Customers** | 5.4% | 7,005 | - |
| **Best Customers** | 5.3% | 6,918 | Nurture with exclusive rewards. |
| **Almost Lost** | 3.6% | 4,613 | Deploy re-engagement strategies. |
| **Lost Customers** | 2.6% | 3,406 | Deploy re-engagement strategies. |
| **Loyal Customers** | 1.5% | 1,956 | Nurture with exclusive rewards. |
 *(Data extracted from Customer Segmentation status distribution)* 

### Market Positioning & Consumer Priorities
* **Positioning:** Octopus Energy currently exhibits low brand popularity and a weak sustainability perception compared to incumbent providers. Strategic marketing investments and rebranding campaigns are required to improve brand awareness and environmental positioning.
*  **Consumer Priorities:** Across multiple analytical models and consumer segments, efficient technical assistance emerged as a critical factor in consumer decision-making and utility maximization.

## Installation & Usage

 To run the notebooks and scripts in this repository, you will need a standard Python data science environment. 
 For the Conjoint Analysis (R): Ensure you have an R environment configured with these packages installed:
"
 `radiant`
 `tidyverse`
 `reshape2`
 `readxl`
"
1.  **Web Scraping:** `selenium` is required for automating browser interactions, alongside a compatible Chrome WebDriver instance.
2.  **Data Manipulation:** `pandas` is used extensively for cleaning data and formatting DataFrames.
3.  **Machine Learning & NLP:** `scikit-learn` is required for executing the analytical models, including CountVectorizer, LDA, K-Means clustering, PCA, t-SNE, StandardScaler, SVM, and Logistic Regression.

```bash
git clone [https://github.com/Pooya-s/OctopusEnergy-Analytics.git](https://github.com/Pooya-s/Marketing_Analysis.git)
cd OctopusEnergy-Analytics
pip install -r requirements.txt
