# 🎲 Discrete Probability Distributions in R: Empirical, Poisson, and Binomial Models

[![R](https://img.shields.io/badge/R-276DC3?style=flat&logo=r&logoColor=white)](https://www.r-project.org/)
[![ggplot2](https://img.shields.io/badge/ggplot2-Data_Visualization-green?style=flat)](#)
[![Statistics](https://img.shields.io/badge/Statistics-Probability_Theory-blue?style=flat)](#)

## 📖 Project Overview
This repository contains a comprehensive statistical analysis demonstrating the practical application of discrete probability distributions using **R**. The project is divided into three distinct real-world case studies, showcasing how to model uncertainty, calculate expected values, and determine the likelihood of specific events using Empirical, Poisson, and Binomial distributions.

**Author:** Oluwafemi Gabriel James  
**Domain:** Applied Statistics & Quality Control

## ⚙️ Case Studies & Methodology

### 1. Empirical Probability Distribution (Manufacturing Defects)
**Context:** Monitoring the number of defects per 1000 parts in an automated manufacturing process over a series of random time intervals.
* **Techniques Applied:**
  * Constructed frequency and probability distribution tables from raw numeric vectors.
  * Validated the fundamental rule of probability (sum equals 1).
  * Visualized the Probability Mass Function (PMF) using `ggplot2`.
  * Calculated the Expected Value (Mean = 7.94), Variance (2.156), and Standard Deviation (1.468).
* **Specific Probabilities Calculated:**
  * $P(6 \le X \le 9)$ = 77.5%
  * $P(X \ge 9)$ = 31.5%

### 2. Poisson Distribution (Weather Events Modeling)
**Context:** Analyzing documented weather events in Montana to predict the frequency of property-damaging hail storms, given an established historical average ($\mu = 3.3$ storms/year).
* **Techniques Applied:**
  * Utilized `dpois` and `ppois` to calculate point and cumulative probabilities.
  * Adapted the lambda/mean parameter for extended time horizons.
* **Specific Probabilities Calculated:**
  * Likelihood of 2 to 4 storms in a single year: $P(2 \le X \le 4)$ = 60.4%
  * Likelihood of at least one storm in a single year: $P(X \ge 1)$ = 96.3%
  * Likelihood of 5 to 7 storms over a two-year period ($\mu = 6.6$): $P(5 \le X \le 7)$ = 44.5%

### 3. Binomial Distribution (Quality Control Testing)
**Context:** Evaluating a lot-testing protocol for electronic switches where a sample of 50 parts is tested ($n = 50$), and the overall shipment defect rate is known to be 8.3% ($p = 0.083$).
* **Techniques Applied:**
  * Applied the complement rule with `pbinom` (`lower.tail = FALSE`) to calculate upper-tail probabilities for batch rejections.
  * Calculated the expected value and standard deviation for the *success* condition (parts passing the test, where $q = 1 - p$).
* **Specific Probabilities Calculated:**
  * Likelihood of 2 or more parts failing the test: $P(X \ge 2)$ = 92.74%
  * Expected number of parts to *pass* the test: 45.9 parts (with a standard deviation of 2.0).

## 🛠️ Technology Stack
* **Language:** R
* **Libraries:** `ggplot2` (for data visualization)
* **Statistical Functions:** `dpois()`, `ppois()`, `pbinom()`, `table()`, `mean()`, `sd()`
