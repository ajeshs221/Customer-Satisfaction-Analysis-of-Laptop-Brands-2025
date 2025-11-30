Customer Satisfaction Analysis of Laptop Brands

A Data-Driven NLP Study Using Web Scraping, Transformer Sentiment Analysis, Wilson Score, and Power BI

Overview

This project analyzes customer satisfaction across four major laptop manufacturers:

Acer

ASUS

Dell

Lenovo

The goal is to evaluate which brand delivers the best user experience using real customer reviews, not influencer or marketing claims.

The analysis combines:

Web Scraping (Selenium)

Transformer-based Sentiment Analysis (HuggingFace)

Rating Normalization & Satisfaction Score

Wilson Lower Bound Confidence Scoring

Interactive Visualization using Power BI

This repository contains all datasets, code, visualizations, and documentation needed to fully reproduce the study.

Key Features

Web Scraping
Scraped verified customer reviews using Selenium WebDriver from product review pages of each manufacturer.

NLP Sentiment Analysis
Used a TensorFlow DistilBERT model to compute sentiment probability from review text.

Satisfaction Score

Combined normalized star rating and sentiment score:

𝑆𝑎𝑡𝑖𝑠𝑓𝑎𝑐𝑡𝑖𝑜𝑛 = 0.6 × 𝑅𝑎𝑡𝑖𝑛𝑔 𝑛𝑜𝑟𝑚 + 0.4 × 𝑆𝑒𝑛𝑡𝑖𝑚𝑒𝑛𝑡 𝑆𝑐𝑜𝑟𝑒

Wilson Lower Bound
Calculated Wilson score to account for variations in review volume and reliability:
Lenovo: 0.90
Dell: 0.86
ASUS: 0.85
Acer: 0.79

Power BI Dashboard

Includes charts for: Average Ratings, Sentiment Scores, Wilson Score Comparison, Satisfaction Score, Brand Insights

Final Results (Summary)
Metric	Winner
⭐ Average Rating	Lenovo (4.7)
😀 Sentiment Score	Lenovo (0.62)
📉 Wilson Score	Lenovo (0.90)
📊 Satisfaction Score	Lenovo (0.808)
🏆 Composite Score (Rating+Sentiment+Reliability+Volume)	Dell (0.82)

Overall, Lenovo consistently performs the best across most major indicators, while Dell ranks second, supported by strong reliability and review volume.
ASUS and Acer lag behind both in sentiment and satisfaction metrics.
