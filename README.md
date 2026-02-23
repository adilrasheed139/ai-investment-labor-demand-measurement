# Text-Based Measurement of AI Investment and Labor Demand  
## Evidence from Large-Scale Online Job Postings Data

---

## 📌 Overview

This project develops scalable, text-based measures of Artificial Intelligence (AI) exposure using 120,000+ LinkedIn job postings (2023–2024).  

By combining structured labor market data with unstructured text embeddings, the study examines whether AI-related job signals are associated with:

- 💰 Higher advertised wages  
- 👀 Greater job seeker engagement (views)  

The project integrates Natural Language Processing (NLP) with econometric modeling to contribute to real-time measurement of AI investment and labor demand dynamics.

---

## 🎯 Research Questions

1. Do job postings with stronger AI semantic relevance offer higher wages?
2. Do AI-related job postings attract greater engagement from job seekers?

---

## 🧠 AI Measurement Framework

We construct two complementary AI exposure measures:

### 1️⃣ Keyword-Based AI Score
- Counts occurrences of AI-related terms (e.g., machine learning, NLP, GPT).

### 2️⃣ Embedding-Based AI Score
- Uses Sentence Transformer embeddings
- Computes cosine similarity between job description vectors and an AI reference vector
- Captures semantic AI intensity beyond simple keywords

This allows scalable and flexible AI exposure measurement in unstructured labor market text.

---

## 📊 Data

- **Source:** LinkedIn Job Postings (2023–2024)
- **Total postings:** 123,849
- **Final regression sample (with salary data):** ~6,200 observations
- **Variables include:**
  - Job title & description
  - Median salary (where available)
  - Experience level
  - Work type (Full-time, Part-time, etc.)
  - Remote status
  - Job views (engagement)

---

## 📈 Econometric Strategy

### Wage Model (OLS)

\[
\ln(MedianSalary) = \beta_0 + \beta_1 AI\_Score + Controls + \varepsilon
\]

- Robust (HC3) standard errors
- Controls: Remote status, experience level, work type

---

### Engagement Model (Negative Binomial)

\[
E(Views|X) = \exp(X\beta)
\]

- Appropriate for overdispersed count data
- Models job views as engagement outcome

---

### Additional Analysis
- Subgroup regression (Mid-Senior roles)
- Quantile regression (median engagement)
- Residual diagnostics

---

## 🔍 Key Findings

### 💰 Wages
- AI semantic relevance does **not robustly predict higher wages** after controls.
- Remote jobs exhibit strong positive wage premiums.
- Experience level strongly predicts salary differences.

### 👀 Engagement
- AI embedding score significantly increases expected job views.
- AI signals appear to function as *attention mechanisms* rather than wage determinants.

---

## 📊 Figures & Visualizations

### Distribution & Descriptive Analysis

Embedding-Based AI Similarity Score  
![](https://github.com/adilrasheed139/ai-investment-labor-demand-measurement/blob/main/Distribution%20of%20Embedding%E2%80%91Based%20AI%20Similarity%20Score.png)

Raw AI Text Score Distribution  
![](https://github.com/adilrasheed139/ai-investment-labor-demand-measurement/blob/main/Distribution%20of%20Raw%20AI%20Text%20Score.png)

Distribution of Median Salaries  
![](https://github.com/adilrasheed139/ai-investment-labor-demand-measurement/blob/main/Distribution%20of%20Median%20Salaries%20(Available%20Data%20Only).png)

Distribution of log(Views + 1)  
![](https://github.com/adilrasheed139/ai-investment-labor-demand-measurement/blob/main/Distribution%20of%20log(views%2B1).png)

Counts of Experience Levels  
![](https://github.com/adilrasheed139/ai-investment-labor-demand-measurement/blob/main/Counts%20of%20Experience%20Levels.png)

Experience Levels by AI Signal Presence  
![](https://github.com/adilrasheed139/ai-investment-labor-demand-measurement/blob/main/Experience%20Levels%20by%20AI%20Signal%20Presence.png)

Count of Job Postings With vs Without AI Keywords  
![](https://github.com/adilrasheed139/ai-investment-labor-demand-measurement/blob/main/Count%20of%20Job%20Postings%20With%20vs%20Without%20AI%20Keywords.png)

Top 20 Most Frequent Skills  
![](https://github.com/adilrasheed139/ai-investment-labor-demand-measurement/blob/main/Top%2020%20Most%20Frequent%20Skills%20in%20LinkedIn%20Job%20Postings.png)

---

### Wage Analysis

AI Semantic Relevance vs Log Median Salary  
![](https://github.com/adilrasheed139/ai-investment-labor-demand-measurement/blob/main/AI%20Semantic%20Relevance%20vs%20Log%20Median%20Salary.png)

Remote vs On-Site Log Median Salary  
![](https://github.com/adilrasheed139/ai-investment-labor-demand-measurement/blob/main/Remote%20vs%20On%E2%80%91Site%20Log%20Median%20Salary.png)

Median Salary by Remote Allowed  
![](https://github.com/adilrasheed139/ai-investment-labor-demand-measurement/blob/main/Median%20Salary%20by%20Remote%20Allowed.png)

Regression Diagnostic: Residual vs Fitted  
![](https://github.com/adilrasheed139/ai-investment-labor-demand-measurement/blob/main/Residual%20vs%20Fitted.png)

---

## 🛠 Technical Stack

- Python
- Pandas / NumPy
- Sentence Transformers
- Scikit-learn
- Statsmodels
- Negative Binomial MLE
- Quantile Regression

---

---

## 🚀 Future Work

- Extend AI exposure measurement to firm-level aggregation
- Incorporate industry and geographic fixed effects
- Panel analysis across time
- Link AI exposure to firm performance and financial outcomes
- Compare embedding models (OpenAI, SBERT, domain-adapted transformers)
- Develop real-time AI investment index

---

## 👤 Authorship

**Adil Rasheed**  
Independent Researcher  
Focus: AI Measurement, Labor Economics, Econometrics, NLP  

---

## 📚 Research Contribution

This project contributes to the growing literature on:

- AI and labor market dynamics  
- Text-based economic measurement  
- Real-time innovation exposure  
- Computational social science  

It demonstrates a scalable framework for measuring AI investment signals using unstructured data and evaluating their economic implications.

---

## 📌 License

This repository is intended for academic and research purposes.
