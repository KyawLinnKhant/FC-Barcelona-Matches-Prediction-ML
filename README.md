This repository contains the Machine Learning Mini Project for Predicting Match Outcomes in Football, focusing on the Spanish La Liga.

---

## 1. Project Overview

The objective of this project is to explore Spanish La Liga match data from 2019 to 2025 to uncover performance patterns and build predictive models. The study aims to identify which factors contribute most to winning, drawing, or losing a match.

### Key Goals:

* Develop a machine learning pipeline to predict football match results.


* Perform thorough Exploratory Data Analysis (EDA) to identify team statistics and seasonal trends.


* Implement extensive feature engineering for variables like form streaks and efficiency ratios.


* Compare algorithms including Logistic Regression, Ensemble methods, and Neural Networks.



---

## 2. Dataset Description

The dataset was obtained from Kaggle and covers six seasons (2019/20 to 2024/25).

* 
**Records**: 4,318 team-match records (2,159 unique fixtures).


* 
**Teams**: 27 different La Liga teams.


* 
**Features**: Goals (gf/ga), expected goals (xG/xGA), possession, shots, venue, referee, and attendance.



---

## 3. Key Findings & Insights

* 
**Home Advantage**: Match outcomes are highly influenced by venue, with a 44.6% win rate at home versus 27.9% away.


* 
**Top Team Performance**: Real Madrid maintained the highest win rate (67.6%) during the study period, followed by Barcelona (65.7%).


* 
**Goal Correlation**: Expected Goals (xG) show a positive relationship () with actual goals scored.


* 
**Attendance Trends**: Sunday matches recorded the highest average attendance at approximately 32,400.


* 
**Possession**: Winning teams averaged 51.2% possession, while losing teams averaged 48.8%, suggesting that pure possession is not the sole driver of victory.



---

## 4. Analysis Methodology

1. 
**Data Quality**: Addressed missing values in attendance (22.6%) and removed empty columns like 'notes'.


2. 
**EDA**: Analyzed temporal trends, win rates by day of the week, and team efficiency.


3. 
**Modeling**: Applied a randomized 80-20 split on historical data for training and evaluation.



---

## 5. Author Information

* 
**Name**: Kyaw Linn Khant 


* **Student ID**: UH kk23acu | PSB 9935nqpt 


* 
**Institution**: University of Hertfordshire 


* 
**Course**: BEng Honours in Robotics and Artificial Intelligence 



---

Would you like me to generate a specific `requirements.txt` file or a Python script to help organize your `scripts/` folder?
